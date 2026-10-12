# 의미론

이번 글의 내용은 대략 아래와 같다.

> ## 목차
>
> ### 1. 구조
>
> ### 2. 항의 값
>
> ### 3. 성립
>
> ### 4. 이론과 모델

3.이 제일 어렵고 내용이 많다.

## 1. 구조

1차 논리 언어의 구조, 또는 번역은 1차 논리 언어에 의미를 부여하는 역할을 한다. 구문론 글에서 다룬 1차 논리 언어는 단순한 문자들의 나열에 불과했지 실질적으로 의미를 가지지 않았다. 내가 $P(x)\wedge Q(c)$라는 논리식을 보여줬다고 하자. 그럼 당연히 $P,Q,c$가 뭘 의미하는 기호인지를 물어야 한다. 그것에 대한 답이 구조라고 보면 된다.

> ### 1차 논리 언어의 구조(structure)
>
> 1차 논리 언어 $\mathcal{L}$의 구조 $\mathfrak{M}$은 아래와 같이 구성된다.
>
> 1. 논의 영역 (Domain) : 1차 논리 언어 $\mathcal{L}$이 묘사하는 대상들의 집합이다. $|\mathfrak{M}|$로 표기한다.
>
> 2. 상수 기호의 번역 (Interpretation of constant symbols) : $\mathcal{L}$의 상수 기호 $c$에 대해 $c$가 가리키는 대상을 $c^\mathfrak{M}$이라 쓰며 $c^\mathfrak{M}\in |\mathfrak{M}|$이다.
>
> 3. 함수 기호의 번역 (Interpretation of functional symbols) : $\mathcal{L}$의 $n$항 함수 기호 $f$에 대해 $f$가 가리키는 함수를 $f^\mathfrak{M}$이라 쓰며 $f^\mathfrak{M}: |\mathfrak{M}|^n\rightarrow |\mathfrak{M}|$이다.
>
> 4. 술어 기호의 번역 (Interpretation of predicate symbols) : $\mathcal{L}$의 $=$가 아닌 $n$항 술어 기호 $R$에 대해 $R$가 가리키는 관계를 $R^\mathfrak{M}$이라 쓰며 $R^\mathfrak{M}\subset |\mathfrak{M}|^n$이다.

쉽게 말해서 어떤 1차 논리 언어가 묘사하는 세상의 의미를 가진다.

## 2. 항의 값

이제 항의 값을 알아보자.