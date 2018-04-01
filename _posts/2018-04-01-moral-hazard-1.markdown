---
layout: post
title: "Contract Examples"
date: "2018-04-01 23:49:43 +0900"
excerpt: "무엇을 공부할까요?"
tags: [Moral Hazard]
comments: true
---
<h4 style="text-align:left"> <a href="/blog/moral-hazard-0"> 이전 포스트 : Moral Hazard</a></h4>
<br/>

본 포스트는 서울대학교 경제학부 김선구 교수님의 "계약 경제학" 수업을 기본으로 만들어졌습니다. 그 외에 다양한 논문들의 이론이나 해석들이 포함되어 있으나 필기를 세세히 하지 못하여 인용을 표시하지 못하는 점 미리 양해 부탁드립니다.
{: .notice}

## Previously
지난 포스트에서는 도덕적 해이가 경제적 현상이며, 어떤 조건을 의미하는지 설명하였습니다.
1. 주인(Principal)이 대리인(Agent)에게 행동(Action)을 위임한다(**Action Delegation**)
2. 주인은 대리인의 행동 선택을 직접적으로 관찰할 수 없다.(**Information Asymmetry**)
- 다만 그 선택과 불완전하게 연관된 다른 몇몇 변수들은 관찰할 수 있다.
3. 주인은 대리인이, 자신(주인)의 이익을 위해 행동하기를 원한다. 하지만 대리인은 대리인 자신의 이익을 위해서 행동한다.(**Conflict of Interest**)

# Contract Examples
저번 시간에, 도덕적 해이라는 '경제적 문제'를 계약을 통해 해결할 수 있다고 말씀드렸습니다. 그렇다면 계약이라는 것은 어떻게 표현할 수 있을까요? 오늘은 실생활에서 자주 나타나는 6개의 계약들을 약간의 수학적 표현과 함께 소개해드리겠습니다.

# Notations
앞으로 수학 혹은 경제학적인 표현에 있어서 사용할 Notations를 정리하도록 하겠습니다.

\\[P = Principal, \quad A = Agent \quad a = action \quad x = outcome \quad s(x) = salary\\]

경제학적으로 계약은, Principal이 Agent에게 salary를 어떻게 지불할 것인지를 정의한 것이며, 이는 주로 관측할 수 있는 변수인 outcome \\(x\\)를 통해 결정됩니다.

## 1. Fixed-Wage Contract
\\[s(x) = k,\qquad k:constant\\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_1.png">
	<figcaption style="text-align:center">fixed-wage contract</figcaption>
</figure>
고정 급여 계약은 가장 간단한 형태로, 생산량에 관계 없이 동일한 임금을 약속합니다. 주로 저임금 노동자들이나 파트타임 계약 등에 나타납니다.

## 2. Fixed-Rent Contract
\\[s(x)= x - k(const)\\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_2.png">
	<figcaption style="text-align:center">fixed-rent contract</figcaption>
</figure>
고정 임대 계약은 고정 급여 계약과 정반대의 성질을 지닙니다. 고정 급여 계약이 Principal이 Agent에게 고정된 임금을 지불하고 나머지를 모두 챙겨가는 반면에, 고정 임대 계약은 Agent가 Principal에게 일정 금액을 지불하고 모든 수익을 가져갑니다. 계약금을 지불하고 라이센스를 얻어가는 프랜차이즈나, 택시기사 등의 계약이 이에 해당합니다.

## 3. Linear Contract
\\[s(x)=\alpha x + \beta \\qquad 0 <\alpha < 1\\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_3.png">
	<figcaption style="text-align:center">linear contract</figcaption>
</figure>

선형 계약은 고정 급여 계약과 고정 임대 계약의 혼합입니다. \\(\alpha\\)는  Agent가 생산량에서 어느 비율 만큼을 가져갈 지를 의미하고, \\(\beta\\)는 양수일 경우 Principal이 Agent에게 지불하는 고정 급여가 되고, 음수일 경우는 Agent가 Principal에게 지불하는 고정 계약금이 됩니다. 이는 많은 영업직군과 프랜차이즈 산업에서 발견됩니다. 그리고 저번 포스팅에서 소개한 지주-소작농 관계나 Joint Venture, Partnership Firms 등 역시 Linear Contract를 기반으로 하는 경우가 많습니다. \\(\alpha\\)와 \\(\beta\\)의 값에 따라 다양한 모습을 보일 수 있죠.

## 4. Bonus Contract
\\[s(x) = w \qquad (if x<x_c)\\]
\\[s(x) = w + \beta \qquad (if x \geq x_c)\\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_4.png">
	<figcaption style="text-align:center">bonus contract</figcaption>
</figure>

보너스 계약은 직관적입니다. 고정 급여 계약을 기본으로, 특정 목표 생산량 \\(x_c\\)을 초과한 경우 보너스 \\(\beta\\)를 얹어주는 형식입니다. 경우에 따라 이는 여러개의 목표 생산량을 가지거나, 선형 보너스 계약이 될 수도 있습니다.

<figure class='half'>
  <img src="/assets/lecture_asset/moral_hazard/1_5.png">
  <img src="/assets/lecture_asset/moral_hazard/1_6.png">
	<figcaption style="text-align:center">other bonus contracts</figcaption>
</figure>

## 5. Debt Contract
\\[s(x) = 0(Bankruptcy) \\qquad if x<(1+r)D\\]
\\[s(x) = x - (1+r)D \\qquad if x\geq (1+r)D \\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_7.png">
	<figcaption style="text-align:center">debt contract</figcaption>
</figure>
Debt 계약은 금융 대출 상품들에 많이 적용됩니다. Agent가 유한한 책임을 지는 것이 핵심입니다. 쉽게 말하면, Agent가 빚을 내서 빚을 갚는 경우는 제외해 주는 것입니다. 만약 Agent가 모든 채무를 다할 수 있는 경우라면 그 채무를 제외한 생산량을 가지게 되며, 이는 fixed-rent 계약과 같습니다.

## 6. Tournament Contract
\\[s(x_i, x_j) = w \qquad (if x_i<x_j)\\]
\\[s(x_i, x_j) = w + \beta \qquad (if x_i \geq x_j)\\]
<figure>
  <img src="/assets/lecture_asset/moral_hazard/1_8.png">
	<figcaption style="text-align:center">tournament contract</figcaption>
</figure>
토너먼트 계약은 상대평가가 적용되는 계약입니다. 형태는 보너스 계약과 유사하지만 목표가 생산량이 아니라, 경쟁자의 성과입니다. 즉, 상대방보다 잘 하면 높은 급여를, 그렇지 않으면 적은 급여를 받는 계약으로, 승진제도와 스포츠 선수들의 계약이 이에 해당합니다.

## 마무리
이번 포스트에서는 실생활에서 나타나는 계약을 간단한 수식으로 정의해보았습니다. 재밌는 것은 위에서 든 계약과 사례의 매칭의 이유가 증명되지 않은 경우가 많다는 것입니다. 예를 들어, Tournament Contract는 다양한 회사에서 승진제도로서 나타나는데, 왜 하필 이 계약 형태가 주류가 되었는지는 제대로 설명되지 않고 있으며 이를 증명하는 것만으로도 하나의 연구주제입니다.

다음 포스팅에서는 이제 Principal과 Agent의 상호 작용을 모델링하고, 본격적으로 경제적인 최적선택들을 탐구해볼 것입니다. 이 분야는 수학적인, Technical Problem Solving이 많이 등장하는데, 수학적인 해석이 익숙하지 않고 꺼려지는 분들을 위해 직관적인 설명을 위주로 하고 수학적인 부분은 따로 표시하여 설명할 생각입니다.
