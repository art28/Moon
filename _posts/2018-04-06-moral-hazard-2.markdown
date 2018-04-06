---
layout: post
title: "The Standard Principal-Agent Model"
date: "2018-04-06 17:11:40 +0900"
excerpt: "기본적인 모델링"
tags: [Moral Hazard]
comments: true
---
<h4 style="text-align:left"> <a href="/blog/moral-hazard-1"> 이전 포스트 : Contract Examples</a></h4>
<br/>

본 포스트는 서울대학교 경제학부 김선구 교수님의 "계약 경제학" 수업을 기본으로 만들어졌습니다. 그 외에 다양한 논문들의 이론이나 해석들이 포함되어 있으나 필기를 세세히 하지 못하여 인용을 표시하지 못하는 점 미리 양해 부탁드립니다.
{: .notice}

## Previously
지난 시간에는 실제 현실에서 나타나는 주요 (주인-대리인 관계가 존재하는)계약들을 몇 개 살펴보았습니다.

## The Basic Model
<figure>
  <img src="/assets/lecture_asset/moral_hazard/2_1.png">
	<figcaption style="text-align:center">Basic P-A model</figcaption>
</figure>
이번 시간부터는 주인과 대리인의 관계를 경제학적으로 설명하도록 하겠습니다. 경제학의 기본은 "가정"이고, 이 가정을 통해 단순화된 모형 안에서 함의를 찾아내는 것이라고 (개인적으로) 생각합니다.
현실에 맞는 가정을 세워야 현실에 맞는 함의가 나올 수 있겠죠? 하지만 계산의 복잡성이나 표현의 난해함 때문에 가정이 엄밀하게 적용하지 못하는 경우도 많습니다. 이런 느낌을 받을 때마다 "이건 뭐 어쩔 수 없지..."하며 넘어가시지 마시고 어떻게 개선할 수 있을지 생각하면 학문적으로도, 실용적으로도 도움이 될 것입니다.

### Variables
- Agents(여기서 에이전트는 대리인이 아니라 이 경제적 게임 모델의 행위자라는 뜻입니다.)
\\[P : Principal \quad A: Agent\\]
  - 주인과 대리인이 이 모델의 행위자입니다.

- Agent's concern
\\[a \in [0,\infty] : action \quad c(a)(c'>0, c^{\prime \prime}>0) : cost\\]
  - 대리인은 \\(a\\)를 조정할 수 있습니다. 도덕적해이 특성 상 \\(a\\)는 '노력'으로 보시면 편합니다.
  - \\(c\\)는 \\(a\\)를 늘릴 수록 증가하는, 비용함수입니다. 노력을 더 투입할 수록 얼마나 효용이 감소하는 지 생각하시면 됩니다.

- Principal's concern
\\[x(a): output \quad : s(x) : salary \\]
  - \\(x\\)는 Agent가 투입한 \\(a\\)에 따라 결정되는 기업의 생산 함수입니다. 기업의 목표는, 주로 이 \\(x\\)를 극대화하는 것입니다.  \\(x\\)는 이른바 Commonly Observable 합니다. 이게 무슨 뜻이냐 하면은, 단순히 Principal과 Agent가 \\(x\\)의 값을 관측할 수 있을 뿐 아니라, 이 사실(상대방이 관측할 수 있다는 사실)을 서로 알고, 이를 또 서로 알고... 가 무한히 반복된다는 뜻입니다. 쓸모 없어 보이지만, 엄밀한 게임이론적 토대를 세우기 위해서는 필요하다고 합니다. 저희는 \\(x\\)가 공개되는 변수라는 데 집중하면 됩니다. 이게 왜 중요하냐면, 우리가 앞으로 추가할 가정들에서 대부분 \\(a\\)는 Principal 이 정확히 확인할 수 없고, \\(x\\)만을 관측할 수 없다고 전제하기 때문입니다. 그리고 이 것이 도덕적 해이의 원인이죠.
  \\[x'>0,\ x^{\prime \prime}<0\ \\]
  - \\(x\\)는 \\(a\\)가 증가할 수록 증가합니다. 다만 그 한계(marginal) 증가량은 감소합니다.
  - \\(s\\)는 우리가 지난 시간에 설명한 계약의 함축적 표현입니다. 주로, 관측할 수 있는 변수인 \\(x\\)에 의해 사전에 결정됩니다.

- Additional Common Assumption
\\[P\ cannot\ directly\ observe\ "a"\\]
  - 위에서 언급하였듯이, Principal이 \\(a\\)를 직접 관찰할 수 없다는 것이 도덕적해이 문제의 핵심입니다.
\\[A\ can\ get\ \overline{u}\ if\ works\ at\ another\ company\\]
  - \\(\overline{u}\\)는 **reservation utility level**라고 합니다. 이 상수의 목적은 노예경제를 배제하는 것입니다. 어떤 계약이 Principal로부터 Agent에게 제의되었을 때, Agent가 적어도 일정 수준의 임금을 다른 곳에서 받을 수 있는 인력이라는 사실이 고려되어야 합니다. 내가 다른 곳에서 같은 노력으로 적어도 만 원을 받을 수 있는 사람이라면, 오천 원 짜리 계약서에 서명하지는 않을 것입니다. \\(\overline{u}\\)의 필요성은 바로 다음 케이스에 다시 나올 것입니다.

---
## From Now on..
- 위의 Basic Model을 기반으로, 이제 우리는 조금씩 가정을 더해가며 행위자들의 최적 선택을 관찰할 것입니다. 가정은 계산적 편의를 위해 도입된 것도 있고, 현실에 대한 표현력을 높이고, 기존 모델과의 차이를 대조하기 위해서 적용되는 것도 있습니다.
- 수학적 내용이 다수 포함되어 있습니다. 원래는 경제학적 모델링 -> 수학적 풀이 -> 함의 도출이 기본적인 학습 방법이지만, light한 독자들을 위해서 기본적인 모델링 이후 함의를 바로 이야기 하고 경제학-수학적 증명은 뒤에 붙이도록 하겠습니다.
- 우리가 주로 살펴볼 것은 3 가지 측면입니다.
  - 첫 번째는 Principal이 어떤 계약을 제시하는 가 입니다. Principal의 목적은 \\(x\\)를 극대화하기 위한 것이고, 이를 위한 특정 \\(a^\star\\)를 Agent가 선택하도록 유도(induce)하고자 합니다. 사실 이 \\(a^\star\\)를 찾는 것도 필요한 일이지만, 편의를 위해 최적의 \\(a^\star\\)가 있다고 생각하고 이 \\(a^\star\\)를 induce하기 위한 계약의 형태에만 집중할 것입니다.
  - 두 번재는 Agent가 이 계약 상에서 어떤 선택을 하는가 입니다. 실제로 Agent가 이 계약을 받아들이는지(위에서 언급한 \\(\overline{u}\\)가 여기에서 중요합니다.), 이 계약 상에서 어떤 \\(a\\)를 선택하는 지, 그 행동이 \\(a^\star\\)와 같은지가 중요합니다.
  - 마지막으로, Social Welfare, 사회 후생의 합을 고려합니다. 만약 사회를 컨트롤하는 신이 있어서 사회 후생을 최대화 하기 위해 계약의 형태(\\(s\\))와 Agent의 행동(\\(a\\))를 정해준다면, 이것이 위의 두 관점에서 본 실제 현상과 얼마나 괴리가 있는지를 살펴봅니다.

## For Convenience of Calculation..
\\[P\ is\ risk\ neutral\\]
- Principal이 위험중립적임을 가정합니다. risk neutral이라는 말은, 확실하게 50원을 받을 수 있는 상황(zero-risk)과 50%확률로 0원, 50%확률로 100원을 받는 상황을 동일한 효용으로 받아들인다는 뜻입니다. 즉 이 때 Principal의 효용은 간단하게, \\(x - s(x)\\)로 나타낼 수 있습니다.
- 여기서 , Agent는 위험중립성을 공통적으로 가정하지 않습니다. 실제로 Principal은 대체로 주주(stockholders) 등, 다수인 경우가 많아 리스크가 분산화 된 경우가 많은 데 반해, Agent는 개개인(CEO)인 케이스가 많습니다. 따라서 주로 Risk-Averse하다고 가정됩니다. (하지만..)

## Certainty Case
드디어 첫 케이스입니다. Certainty Case는, 만약 \\(a\\)가 관측 가능할 때는 어떤 현상이 벌어지는 가를 관측하고자 합니다. 따라서 다음 가정이 추가됩니다.
- Principal이 \\(a\\)를 관측하는 것이 가능하다.(정확히는, Observable할 뿐 아니라 Verifiable합니다. 중요한 부분이 아니므로 설명은 생략하겠습니다.)
- Agent가 Risk-Neutral합니다. 이는 Certainty Case에서는 Risk-Averse 가정이 계산을 복잡하게 하는 효과외에 큰 함의를 가지지 않기 때문에 적용됩니다. 즉, \\(u(s,a) = u(s) -c(a)\\)입니다.(u는 Agent의 효용함수입니다.)

### Certainty Case의 결과
만약 \\(a\\)를 Principal이 관측 가능하다면, Principal은 간단하게 \\(a^{\star}\\)를 induce할 수 있습니다. Agent가 \\(a^\star\\)를 선택하면, 고정된 일정 액수를 주고 선택하지 않는 경우에는 돈을 주지 않고 해고하겠다는 계약을 맺으면 됩니다. 이 때, '고정된 액수'는 \\(\overline{u}+c(a^\star)\\) 보다 조금만 더 높으면 됩니다. 즉, Agent는 다른 곳에서 받을 수 있는 효용인 \\(\overline{u}\\) 보다 높은 효용을 얻기 위해 \\(a^\star\\)를 선택하게 됩니다. 즉, 이 케이스는 fixed-wage contract로 쉽게 해결이 가능합니다. 이 계약을 Forcing contract라고 하고 경우에 따라 boiling-in-oil contract라고도 합니다. 뒤의 이름은 Agent가 \\(a \noteq a^\star\\)를 선택하는 경우 솥에 끓여 죽이는 것으로 계약서를 써도 된다는 의미라고 합니다. 어차피 Agent는 무조건 \\(a^\star\\)를 선택하는 것이 이익이기 때문입니다.. 그래도 잔인하군요..

## Certainty Case 2
물론, \\(a\\)를 관측하는 것은 불가능합니다. 조금 더 가정을 바꿔보도록 합시다.
- Principal은 \\(a\\)를 관측할 수 없습니다. 그가 관측할 수 있는 것은 \\(x\\)뿐입니다.
- \\(x\\)는 \\(a\\)만의 함수입니다. 즉 \\(x = x(a)\\)입니다.
두 번째 가정 때문에, 이 세팅 역시도 Certainty Case로 분류합니다. 이는 , \\(a\\)가 아닌 다른 변수에는 \\(x\\)가 영향을 받지 않는다는 사실입니다.

### Certainty Case 2의 결과
놀랍게도, 이 경우도 Certainty Case 1과 결과가 같습니다.(그래서 이름이 같겠죠..) Principal은 여전히 Forcing Contract를 제시할 수 있습니다. 다만 이제 조건을 \\(a = a^\star \\)가 아니라, \\(a=x(a^\star))\\)로 두면 됩니다. 이는 Agent가 \\(a^\star\\)를 선택했을 때 나오는 결과가 정해져 있다는 간단한 사실 덕분에 가능합니다.

## Uncertatinty Case
Certainty Case 대로라면, 현실에 Moral Hazard는 존재하지 않아야 합니다. 고정임금 계약만으로도 모든 것을 해결할 수 있죠. 하지만 실제로는 그렇지 않습니다. 그 이유는 \\(x\\)와 \\(a\\)의 관계가 uncertain하기 때문입니다. 즉, Agent가 선택한 \\(a\\)가 같아도,그에 따라 생산량 \\(x\\)가 하나의 값으로 정해지지 않으며, 다른 통제와 관측이 불가능한 변수에 영향을 받습니다.(이를 통틀어서 지금부터 \\(\theta\\))라고 합시다.)즉, \\(x = x(a, \theta)\\)로 표현할 수 있습니다. 이 상황에서 "특정 \\(x\\)를 선택하면 고정된 급여를 주겠다!" 라는 계약을 제시하는 것은 무리가 있을 것 같습니다.

### 그러나...
이 케이스에서 Principal이 Forcing Contract를 제시하는 것은 불가능합니다. Principal이 Agent가 어떤 행동을 했는 지 \\(x\\)만 가지고 판단할 수 없기 때문에 Agent는 \\(a=0\\)을 선택하고 유리한 \\(\theta\\)가 나오기만 기도할 것입니다. 다만 이 때도 모두가 만족할 만한 솔루션이 있습니다. 바로 Principal이 \\(a=a^\star\\)일 때, Certainty Case에서 Agent가 받게 되는 고정 임금을 챙기고 나머지 이익을 다 Agent가 가지도록 하는 것입니다.이는 앞 장에서 배운 fixed-rent 계약과 같습니다. 즉, a에 대한 정보를 가지고 있는 Agent가 생산에 대한 인센티브를 전적으로 컨트롤하게 하는 것입니다. Principal은 자신이 유도하고자하는 \\(a=a^\star\\)를 달성할 수 있고, Agent는 \\(\overline{u}) 이상을 벌 수 있다면 자신의 효용함수를 최적화 하는 선에서 \\(a=a^\star\\)를 선택할 것이며 이는 사회적으로 바람직합니다. 그렇다면 Moral Hazard는 왜 발생하는 걸까요?

## Risk Averseness of Agent
위에서, Agent의 Risk-neutral 가정은 계산상 편의를 위해서 적용되며, Certainty Case에서는 문제가 없다고 말씀드렸습니다. 하지만, Uncertatinty Case에서는 Agent의 Risk에 대한 선호가 매우 중요합니다. 그리고 이것이 도덕적 해이가 발생하는 큰 이유입니다. Principal이 계약을 \\(\theta\\)에 대한 \\(x(a^\star)\\)의 평균 값을 자신이 챙기고 나머지 수익을 Agent에게 준다면(risk를 Agent에게 전가하는 것과 같습니다.), Agent는 이를 받아들이지 않거나, \\(a^\star\\)가 아닌 다른 \\(a\\)를 선택합니다. 왜냐하면, \\(a\\)를 증가함에 따라 Agent가 느끼는 비효용은 급격하게 상승하는데,(\\(c^{\prime \prime} > 0\\)) \\(a\\)를 증가시켜서 \\(x(a, \theta)\\)의 값이 상승해서 얻게 되는 효용의 증가분은 급격하게 감소하기 때문입니다. 이것이 위와 같은 fixed-rent solution 등이 실패하는 원인이 됩니다.

- Risk Averseness 와 임금 증가에 따른 효용 증가분의 관계가 잘 와닿지 않으실 수 있을 것 같습니다. 위에서 언급한 사례를 다시 사용해봅시다.
  - 상황 A : 100% 확률로 50원을 획득함
  - 상황 B : 50%확률로 100원, 50%확률로 0원을 획득함
  - 이 때 얻는 금액 \\(s\\)에 따른 효용이 \\(u(s)=s\\)라고 합시다. 그렇다면 A와 B의 효용은 \\(50 \cdot 1 = 100 \cdot 0.5 + 0 \cdot 0.5 \\)으로 같습니다.
  - 만약, 0원일 때 얻는 효용이 0, 50원일 때 얻는 효용이 40, 100원일 때 얻는 효용이 60이라고 해 봅시다. (좀 더 continuous한 효용함수를 원한다면 \\(u(s) = s^{0.5}\\) 등을 사용하면 됩니다.) 그렇다면 A의 효용은 40인 데 반해, B의 효용은 30이 됩니다. 즉 평균 기대 수익이 같음에도 불구하고, 상황 A를 선호하게 됩니다. 즉 이것이 Risk Averseness의 정의와 부합합니다.

---
## 수학적 해석
### Certainty Case, Forcing Contract
Forcing Contract의 수학적 표현은 다음과 같습니다.
\\[s = s(a)(or s(x)) = \overline{u} + c(a^\star) \qquad if a = a^\star(or\ x=x(a^\star))\\]
\\[s = s(a)(or s(x)) = \underline{u} \qquad \qquad if a \neq a^\star(or\ x \neq x(a^\star))\\]

### Uncertatinty Case
#### When A is Risk Neutral
\\[u(s,a) = u(s)-c(a)=S-c(a) \\]
Principal이 다음과 같은 fixed-rent Contract를 제시한다고 생각합시다.
\\[s(x) = x(a, \theta) - E_\theta[x(a^\star, \theta)] -\overline{u}-c(a^\star) \\]
Agent는 전체 생산량 \\(x\\)에서 뒷 부분을 Principal에게 떼어주고 남은 부분을 가집니다. 그리고 여기서 비용함수인 \\(c(a)\\)를 제외한 부분이 Agent의 효용이며 이를 최대화하고자 합니다.
\\[\max\limits_{a} E_\theta[x(a^\star, \theta)] -\overline{u}\\]
이 때, 이는 고정 임금 계약에서 Principal의 maximization 식과 같습니다..! 즉, Agent도 \\(a^\star\\)를 선택하게 됩니다.

#### When A is Not Risk Neutral
위의 식은 엄밀히 말하면 이렇게 고쳐져야 합니다.(편의상 \\(overline{u}\\)는 분석하지 않습니다)
\\[\max\limits_{a}E_\theta[u(x(a^\star, \theta))])\\]
Risk Neutral인 경우 \\(E(u) = u(E)\\) 이지만, Risk Averse한 경우는 성립하지 않으며, \\(E(u) < u(E)\\) 입니다.
따라서 같은 식임에도 Principal의 optimization 과 Agent의 Optimization 이 달라지고, 다른 \\(a \neq a^\star\\) 를 선택하게 됩니다.

## 마무리
이번 포스트에서는 기본적인 Principal Agent 모델링과 Certainty Case를 위주로 살펴보았습니다. 그리고 \\(x\\)가 \\(a\\)에만 의존하지 않는, Uncertatinty Case를 도입하고 Risk Averseness 와 같은 모럴 해저드의 원인이 되는 개념까지 살펴보았습니다. 다음 시간에는 Risk Averse Agent 모델에서 최적화가 어떻게 진행되는 지 확인해보고, 그 문제점까지 살펴보겠습니다.
