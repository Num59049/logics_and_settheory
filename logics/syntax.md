# 1차 논리의 구문론(Syntax of First Order Logic)

이번 글에서는 대략 아래의 내용들을 다룰 것이다.

>## 목차
>
> - ### [1. 1차 논리 언어](#1-1차-논리-언어-1)
>
> - ### [2. 1차 논리 언어의 기호](#2-1차-논리-언어의-기호-1)
>
> - ### [3. 항과 논리식](#3-항과-논리식-1)
>
> - ### [4. 독해의 유일성](#4-독해의-유일성-1)
>
> - ### [5. 부분식](#5-부분식-1)
>
> - ### [6. 자유변항과 종속변항](#6-자유변항과-종속변항-1)
>
> - ### [7. 치환](#7-치환-1)
>
> - ### [8. 예제](#8-예제-1)
>
> - ### [9. 마무리](#9-마무리-1)

사실 조금 더 많은 내용이 있긴 하나 그렇게까지 중요하지 않다고 생각해서 생략했다. 그리고 이것만 해도 굉장히 외워야 할 게 많기 때문이다. 이번 글에는 정리라고 할만한게 하나뿐이 없고 전부 정의로만 이루어져있다. 중요한 것들만 외워두고 나머지는 필요할 때 찾아보면서 메꾸도록 하자.

## 1. 1차 논리 언어

1차 논리 언어란 1차 논리를 표현하기 위한 언어이다. 아무래도 논리를 표현하기 위한 언어이다 보니 굉장히 엄격한 규칙에 의해 그 표현들이 형성된다. 개념적으로는 1차 논리 언어라는 것이 어떠한 하나의 언어를 가리키는 것이 아니라 자연어라는 단어와 같이 언어의 종류를 가리키는 것이긴 하다. 다만 보통은 모든 언어들을 다 포괄할 수 있는 표준 1차 논리 언어를 기본으로 하고 필요에 따라 표준 1차 논리 언어보다 제한된 언어를 사용한다.

1차 논리 언어에서 1차의 의미는 1차 논리 언어는 표현력이 0차 논리보다는 좋고 2차 논리보다는 나쁘다는 것이다. 그렇다면 그 중에서 왜 1차 논리를 배우냐 하면 우선 0차 논리와 2차 논리도 1차 논리와 기본적인 골자가 비슷하기 때문이다. 따라서 1차 논리를 공부한 후에 0차, 2차 논리를 보면 금방 공부할 수 있다. 또한 1차 논리가 그중에서 가장 좋기 때문이기도 하다. 0차 논리는 너무 표현력이 약하고 2차 논리 언어는 성질이 안 좋다. 이에 대한 이야기는 1차 논리를 설명한 후에 하도록 하겠다.

## 2. 1차 논리 언어의 기호

> * 논리 기호 (logical symbols)
>
>   * 논리적 연결사 (logical connectives)
>
>       $\neg, \lor, \wedge, \rightarrow, \forall, \exists$
>
>   * 논리적 모순 기호 (falsity)
>       
>       $\bot$
>
>   * 등호 (identity predicate)
>
>       $=$
>
>   * 변항 (variables)
>
>       $v_0,v_1,...$
>
> * 비논리 기호 (non logical symbols)
>
>   * $n$항 술어 기호 (n-place predicate symbols)
>
>       $P_0^n,P_1^n,...$
>
>   * 상수 기호 (constant symbols)
>
>       $c_0,c_1,...$
>
>   * $n$항 함수 기호 (n-place functional symbol)
>
>       $f_0^n,f_1^n,...$
>
> * 문장 부호 (punctuation)
> 
>   $(,),comma$

비논리 기호는 1차 논리 언어에 따라 다른 것을 사용할 수 있다. 즉 표준 1차 논리 언어는 모든 술어 기호, 상수 기호, 함수 기호를 모두 사용하는 1차 논리 언어를 의미한다.

1차 논리 언어는 어떤 기호로 구성되는 지에 관계없이 항상 그 언어의 형성 규칙이 동일하다. 즉 1차 논리 언어는 그것이 어떤 기호를 사용하는지에 완전히 의존한다. 따라서 1차 논리 언어는 아래와 같이 표기한다.

> $\mathcal{L} = \{P_0,P_1,...,c_0,c_1,...,f_0,f_1,...\}$

논리 기호와 문장 부호는 언어에 무관하게 항상 필요하기 때문에 위와 같이 비논리 기호들의 집합으로 1차 논리 언어를 표현한다.

## 3. 항과 논리식

항과 논리식은 귀납적으로 정의된다. 참고로 이것이 항과 논리식의 유일한 정의는 아니며 여러 정의들 중 하나에 불과함을 알고 있자.

> ### 항(term)의 정의
> 
> 1차 논리 언어 $\mathcal{L}$의 항은 아래와 같이 귀납적으로 정의된다.
>
> 1. 모든 변항은 항이다.
> 
> 2. 언어 $\mathcal{L}$의 모든 상수 기호는 항이다.
> 
> 3. $f$가 $n$항 함수 기호이고 $t_1,...,t_n$이 항일 때, $f(t_1,...,t_n)$도 항이다.
> 
> 4. 이외의 어떤 것도 항이 아니다.
>
> 모든 항들의 집합을 $Trm(\mathcal{L})$이라고 한다.
>

변항이 나타나지 않는 항을 닫힌 항이라고 한다.

> ### 논리식(formula)의 정의
>
> 1차 논리 언어 $\mathcal{L}$의 논리식은 아래와 같이 귀납적으로 정의된다.
>
> 1. $\bot$은 원자 논리식(atomic formula)이다.
>
> 2. $P$가 $\mathcal{L}$의 $n$항 술어 기호이고 $t_1,...,t_n$이 $\mathcal{L}$의 항일 때 $P(t_1,...,t_n)$은 원자 논리식이다.
>
> 3. $t_1,t_2$가 $\mathcal{L}$의 항일 때 $=(t_1,t_2)$는 논리식이다.
>
> 4. $\varphi$가 논리식이면 $\neg\varphi$도 논리식이다.
> 
> 5. $\varphi, \psi$가 논리식이면 $(\varphi\wedge\psi)$도 논리식이다. 
>
> 6. $\varphi, \psi$가 논리식이면 $(\varphi\vee\psi)$도 논리식이다.
>
> 7. $\varphi, \psi$가 논리식이면 $(\varphi\rightarrow\psi)$도 논리식이다.
>
> 8. $x$가 변항이고 $\varphi$가 논리식이면 $\forall x\varphi$도 논리식이다.
>
> 9. $x$가 변항이고 $\varphi$가 논리식이면 $\exists x\varphi$도 논리식이다.
>
> 10. 이외 어떤 것도 논리식이 아니다.
>
> 모든 논리식의 집합을 $Frm(\mathcal{L})$이라 한다.

원자 논리식은 말 그대로 더 작은 논리식으로 분해되지 않는 논리식을 의미한다.

다만 관용적으로 $=(t_1,t_2)$를 $t_1=t_2$로 쓰고 $\neg=(t_1,t_2)$를 $t_1\neq t_2$로 쓴다.

이외 몇 가지 필수적이지 않으나 편의를 위하여 정의되는 기호들을 명시한다.

- $\top$은 $\neg\bot$의 약어이다.

- $\varphi \leftrightarrow \psi$는 $(\varphi \rightarrow \psi) \wedge (\psi\rightarrow \varphi)$의 약어이다.


> ### 구문론적 동등성(syntactic identity)
>
> 기호 $\equiv$는 두 문자열이 같은 위치에 같은 문자가 있는 동등한 문자열임을 의미한다. 즉 $\varphi \equiv \psi$는 두 논리식 $\varphi, \psi$가 글자 하나하나 빠지지 않고 동일한 문자열이라는 뜻이다.

### 예시

1차 논리 언어 $\mathcal{L} = \{R,P,a,b,c,f,g\}$에서 $R$은 1항 술어, $P$는 2항 술어, $f$는 1항 함수, $g$는 2항 함수라고 하자.

- $g(f(g(x,y)),c)$는 항이다.
  
- $f(g(a,f(b)))$는 닫힌 항이다.
  
- $P(x,f(a))$는 원자 논리식이다.

- $(P(a,b)\vee R(x))$는 논리식이다.
  
- $\forall x (R(x)\rightarrow P(a,f(z)))$는 논리식이다.

- $R(x)\wedge R(y)$는 논리식이 아니다. 괄호가 없기 때문이다.



또한 항과 논리식은 귀납적으로 정의되기 때문에 귀납법이 있다.


> ### 항의 귀납법(Induction Principle of Terms)
>
> 어떤 성질이 다음을 모두 만족하면
>
> 1. 모든 변항이 그 성질을 가진다.
> 
> 2. 언어 $\mathcal{L}$의 모든 상수 기호가 그 성질을 가진다.
> 
> 3. $f$가 $n$항 함수 기호이고 항 $t_1,...,t_n$이 그 성질을 가짐을 가정하면 $f(t_1,...,t_n)$도 그 성질을 가진다.
>
> 모든 항은 그 성질을 가진다.


> ### 논리식의 귀납법(Induction Principle of Formulas)
>
> 어떤 성질이 다음을 모두 만족하면
>
> 1. $\bot$이 그 성질을 가진다.
>
> 2. $P$가 $\mathcal{L}$의 $n$항 술어 기호이고 $t_1,...,t_n$이 $\mathcal{L}$의 항일 때 $P(t_1,...,t_n)$이 그 성질을 가진다.
>
> 3. $t_1,t_2$가 $\mathcal{L}$의 항일 때 $=(t_1,t_2)$가 그 성질을 가진다.
>
> 4. $\varphi$가 그 성질을 가지면 $\neg\varphi$도 그 성질을 가진다.
> 
> 5. $\varphi, \psi$가 그 성질을 가지면 $(\varphi\wedge\psi)$도 그 성질을 가진다. 
>
> 6. $\varphi, \psi$가 그 성질을 가지면 $(\varphi\vee\psi)$도 그 성질을 가진다.
>
> 7. $\varphi, \psi$가 그 성질을 가지면 $(\varphi\rightarrow\psi)$도 그 성질을 가진다.
>
> 8. $x$가 변항이고 $\varphi$가 그 성질을 가지면 $\forall x\varphi$도 그 성질을 가진다.
>
> 9. $x$가 변항이고 $\varphi$가 그 성질을 가지면 $\exists x\varphi$도 그 성질을 가진다.
>
> 모든 논리식은 그 성질을 가진다.

이것으로 증명하는 것이 바로 다음 주제인 독해의 유일성이다.

## 4. 독해의 유일성

만약 내가 $\varphi \rightarrow \psi \wedge \chi$라고 쓰고 이 식의 뜻을 묻는다면 대답하기 곤란할 것이다. 위 문장은 $(\varphi \rightarrow \psi) \wedge \chi$로 읽을 수도 있고 $\varphi \rightarrow (\psi \wedge \chi)$로 읽을 수도 있기 때문이다. 요지는 읽는 방법이 유일하다는 것이 그렇게 자명하지는 않다는 것이다. 그렇기에 논리식을 정의할 때 괄호에 굉장히 엄격한 것이다.


이제 우리가 정의한 논리식이 실제로 항상 유일하게 읽히는지를 증명하도록 하자.

> ### **Lemma.** 논리식에서 왼쪽 괄호와 오른쪽 괄호의 개수는 같다.
>
> **pf.** 항의 대한 귀납법으로 항의 왼쪽 괄호 개수와 오른쪽 괄호 개수가 같음을 증명하고 이를 이용해 논리식에 대한 귀납법으로 증명한다. 그냥 문자열 $s$에 대해 $l(s)$를 왼쪽 괄호의 개수, $r(s)$를 오른쪽 괄호의 개수로 두고 형식적으로 따라가면 된다. 직접 해보자. $_\blacksquare$

> ### 진접두사 (proper prefix)
>
> 문자열의 진접두사는 그것의 앞부분이되 빈 문자열도 그 문자열 자체도 아닌 것이다.

> ### **Lemma.** 논리식의 진접두사는 논리식이 아니다.
>
> **pf.** 귀납법과 위의 렘마를 이용한다. $_\blacksquare$

> ### 독해의 유일성 (Unique readability)
>
> 모든 식 $\varphi$는 반드시 아래의 경우 중에 정확히 하나에만 해당한다.
>
> 1. $\varphi$는 원자식이다.
>
> 2. $\varphi$는 $\neg\psi$ 꼴이다.
>
> 3. $\varphi$는 $(\psi \wedge \chi)$ 꼴이다.
>
> 4. $\varphi$는 $(\psi \vee \chi)$ 꼴이다.
>
> 5. $\varphi$는 $(\psi \rightarrow \chi)$ 꼴이다.
>
> 6. $\varphi$는 $\forall x\psi$ 꼴이다.
>
> 7. $\varphi$는 $\exists x\psi$ 꼴이다.
>
> 나아가 그 경우 내에서 그러한 표현은 유일하다. 즉 $*$가 어떤 논리적 연결사일 때 $\varphi$가 $(\psi * \chi)$로 표현되고 $(\psi' * \chi')$로도 표현이 된다면 $\psi\equiv\psi'$이고 $\chi\equiv\chi'$이다.


**pf.** 논리식 $\varphi$에 대해 $\varphi$는 반드시 양화사, 왼쪽 괄호, 술어 기호, $\neg$로 시작한다. 왼쪽 괄호로 시작하지 않는 경우에는 자명하다. 따라서 왼쪽 괄호로 시작하는 경우만 보면 된다.

우선 그런 경우 어떤 두 논리식과 적절한 연결사 $*$이 있어 $\varphi\equiv(\psi * \chi)$라는 것은 논리식의 정의상 알 수 있다. 따라서 유일성만을 보이면 된다.

$\varphi\equiv(\psi * \chi), \varphi\equiv(\psi' *' \chi')$라고 하자. 여기서 $*, *'$은 임의의 논리적 연결사이다. 만약 $\psi \not\equiv \psi'$이면 $\psi$가 $\psi'$의 진접두사 이거나 $\psi'$가 $\psi$의 진접두사여야 하나 보조정리에 의해 논리식의 진접두사는 논리식이 아니므로 모순이다.

따라서 $\psi\equiv\psi'$이다. 그러면 $*\equiv*'$이고 $\chi\equiv\chi'$까지 성립하게 된다.$_\blacksquare$

따라서 우리는 주연산자라는 개념을 정의할 수 있게 된다. 말그대로 $\neg\psi$꼴의 논리식의 주연산자는 $\neg$이고 $(\psi\wedge\chi)$꼴의 논리식의 주연산자는 $\wedge$, $\forall x \psi$꼴의 논리식의 주연산자는 $\forall$인 것이다. 별거 없다.

## 5. 부분식

부분식(subformula)는 논리식의 부분 문자열 중에 논리식인 것을 의미한다. 역시 귀납적으로 정의된다.

> ### 직전 부분식(immediate subformula)
>
> 1. $\varphi$가 원자식이면 직전 부분식은 없다.
>
> 2. $\varphi\equiv\neg\psi$이면 $\varphi$의 직전 부분식은 $\psi$이다.
> 
> 3. $\varphi\equiv(\psi\wedge\chi)$이면 $\varphi$의 직전 부분식은 $\psi$와 $\chi$이다.
>
> 4. $\varphi\equiv(\psi\vee\chi)$이면 $\varphi$의 직전 부분식은 $\psi$와 $\chi$이다.
>
> 5. $\varphi\equiv(\psi\rightarrow\chi)$이면 $\varphi$의 직전 부분식은 $\psi$와 $\chi$이다.
>
> 6. $\varphi\equiv\forall x\psi$이면 $\varphi$의 직전 부분식은 $\psi$이다.
>
> 7. $\varphi\equiv\exists x\psi$이면 $\varphi$의 직전 부분식은 $\psi$이다.

> ### 진 부분식 (proper subformula)
>
> 논리식 $\varphi$의 진 부분식은 그것이 원자식이라면 존재하지 않으며 그렇지 않다면 그 직전 부분식들과 직전 부분식들의 진 부분식들 전부로 귀납적으로 정의된다.

> ### 부분식 (subformula)
>
> 논리식의 부분식은 그 자체와 그것의 진 부분식들 전부로 정의된다.

## 6. 자유변항과 종속변항

구문론에서 굉장히 중요한 내용인 자유 변항과 종속 변항을 정의하자. 자유변항은 양화사에 구속되지 않은 변항이고 종속변항은 양화사에 구속된 변항을 의미한다. 다만 말은 변항이지만 사실은 변항 '출현' (variable occurance) 이라고 보는 것이 맞다. 아래와 같은 논리식에서도 잘 정의되어야 하기 때문이다.

> $(P(x)\vee\forall x Q(x))$

다음과 같은 논리식에서 $\forall x$의 $x$는 $Q(x)$의 $x$를 가리키는 것은 맞지만 $P(x)$의 $x$를 가리키는 것은 아니다. 따라서 문자열에서 나타나는 각각의 변항에 대해 그것이 자유변항인지 종속변항인지 부여해야한다. 그래서 자유 변항이 아니라 자유 변항 출현, 종속 변항이 아니라 종속 변항 출현이 더 맞는 표현이라 하는 것이다.

이제 자유변항과 종속변항을 제대로 정의하도록 하자. 이 역시 귀납적으로 정의된다.

> ### 자유변항과 종속변항 (free variable occurance and bound variable accurance)
>
> 1. $\varphi$가 원자식이면 모든 변항 출현이 자유 변항 출현이다.
>
> 2. $\varphi\equiv\neg\psi$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 출현과 같다. 
> 
> 3. $\varphi\equiv(\psi\wedge\chi)$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 츌현과 $\chi$의 자유 변항 출현 모두이다.
>
> 4. $\varphi\equiv(\psi\vee\chi)$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 츌현과 $\chi$의 자유 변항 출현 모두이다.
>
> 5. $\varphi\equiv(\psi\rightarrow\chi)$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 츌현과 $\chi$의 자유 변항 출현 모두이다.
>
> 6. $\varphi\equiv\forall x\psi$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 출현 중에 $x$가 아닌 것과 같다.
>
> 7. $\varphi\equiv\exists x\psi$이면 $\varphi$의 자유 변항 출현은 $\psi$의 자유 변항 출현 중에 $x$가 아닌 것과 같다.
>
> 자유 변항 발생이 아닌 모든 변항 발생은 종속 변항 발생이다.

> ### 양화사의 범위(scope)
>
> $\forall x\psi$가 $\varphi$의 부분식일 때, 해당하는 $\forall x$의 범위를 $\psi$라 한다. 
$\exists$의 경우도 동일하다.

> ### 문장(sentence)
>
> 문장은 자유 변항이 출현하지 않는 논리식이다.


## 7. 치환

> ### 항의 치환
>
> 항 $s$에 대해 $s[t/x]$는 $s$에 출현하는 모든 변항 $x$를 항 $t$로 치환한 식이며 아래와 같이 귀납적으로 정의된다.
>
> 1. $s\equiv c$ : $s[t/x]$는 $s$이다.
>
> 2. $s\equiv y$ : $s[t/x]$는 $y\not\equiv x$이므로 $t$이다.
>
> 3. $s\equiv x$ : $s[t/x]$는 $t$이다.
>
> 4. $s\equiv f(t_1,...,t_n)$ : $s[t/x]$는 $f(t_1[t/x],t_2[t/x],...,t_n[t/x])$이다.


> ### 논리식의 치환
>
> 논리식 $\varphi$에 대해 $\varphi[t/x]$는 $\varphi$에 출현하는 모든 변항 $x$를 항 $t$로 치환한 논리식이며 아래와 같이 귀납적으로 정의된다.
>
> 1. $\varphi\equiv\bot$ : $\varphi[t/x]$는 $\bot$이다.
>
> 2. $\varphi\equiv P(t_1,...,t_n)$ : $\varphi[t/x]$는 $P(t_1[t/x],t_2[t/x],...,t_n[t/x])$이다.
>
> 3. $\varphi\equiv\neg\psi$ : $\varphi[t/x]$는 $\neg\psi[t/x]$이다.
>
> 4. $\varphi\equiv(\psi\wedge\chi)$ : $\varphi[t/x]$는 $(\psi[t/x]\wedge\chi[t/x])$이다.
>
> 5. $\varphi\equiv(\psi\vee\chi)$ : $\varphi[t/x]$는 $(\psi[t/x]\vee\chi[t/x])$이다.
>
> 6. $\varphi\equiv(\psi\rightarrow\chi)$ : $\varphi[t/x]$는 $(\psi[t/x]\rightarrow\chi[t/x])$이다.
>
> 7. $\varphi\equiv\forall y\psi$ : $\varphi[t/x]$는 $\forall y\psi[t/x]$이다. ($y\not\equiv x$)
>
> 8. $\varphi\equiv\exists y\psi$ : $\varphi[t/x]$는 $\exists y\psi[t/x]$이다. ($y\not\equiv x$)
>
> 9. $\varphi\equiv\forall x\psi$ : $\varphi[t/x]$는 $\varphi$이다.
>
> 10. $\varphi\equiv\exists x\psi$ : $\varphi[t/x]$는 $\varphi$이다.

치환의 정의에서 주의할 점은 종속변항은 치환하면 안 된다는 것이다. 아래의 예시를 보면 의미상 그렇게 되면 안됨을 이해할 수 있을 것이다.

- $\varphi\equiv(P(x)\vee\exists xQ(x))$에서 $\varphi[t/x]$는 $(P(t)\vee\exists xQ(x))$여야 자연스럽지 $(P(x)\vee\exists xQ(t))$가 되면 굉장히 이상하다.

## 8. 예제

1. $P(a) \land Q(x)$
2. $\forall x (P(x) \rightarrow Q(x))$
3. $\exists x (P(y) \land Q(x))$
4. $f(x, y)$
5. $\forall x (P(f(x)) \rightarrow R(x, a))$
6. $\forall x (Q(x) \rightarrow \exists y R(x, g(y)))$
7. $P(x) \land \forall x Q(x)$
8. $\exists y (Q(g(y)) \land \forall x (P(x) \rightarrow R(f(x), y)))$
9. $\forall x ((P(x) \land P(y) \land R(x, y)) \rightarrow \neg R(y, x))$
10. $\forall x ((P(f(x)) \land \exists y R(x, g(y))) \rightarrow Q(x))$

각각의 문장에 대해 (1)논리식이거나 논리식이 아닌 이유를 귀납적 정의에 따라 단계적으로 설명하고 (2)자유 변항 출현과 종속 변항 출현을 구별하여 찾고 (3)각각의 양화사의 범위를 구하고 (4)주연산자를 찾도록 해라.

ㅈㄴ 대충 만들었다. 너무 감이 안 오는 사람만 해보면 될듯

## 9. 마무리

귀납적 정의고 뭐고 너무 길고 복잡해서 막막할 것이다. 다만 눈치 챘을 수도 있는데 이번 글에서 귀납적으로 정의한 대상들은 굳이 그렇게 하지 않아도 직관적으로 받아들이고 쓸 수 있다는 점이다. 누군가 어떤 문자열을 보여주고 그것이 논리식인지 묻는다면 굳이 귀납적 정의를 하나하나 따라가지 않아도 판단할 수 있을 것이다. 즉 귀납적 정의는 그냥 직관적인 대상들을 수학적인 대상화시키고 증명과 논증의 영역으로 끌고오기 위한 방법에 불과하지 이걸 다 외울 필요는 없다. 사실 계속 사용하다 보면 어느 순간 거의 외워져 있다.

또한 현재 이 글은 아직 수정 중에 있으며 부족한 부분이 많다. 예시나 연습문제는 천천히 추후 추가하도록 하겠다.