# TDD

## 용어
- [Fixture](): 테스트가 시작할 때 존재하는 고정된 상태로 테스트가 반복 가능함을 보장한다. 그리고 테스트가 시작할때(Setup)되고 종료될때(tearDown)정리 할 수 잇다.

## TDD에 관한 중요 질문


### 1. 어떻게 해야 테스트 주도 개발을 잘 적용할 수 있을까?


### 2. 어디서 시작해야 할까?
Usecase(Acceptance Critieria)에서 시작해야 한다. 보통은 백엔드 개발자는 API라고 생각해서 Controller가 대상이 되기도 한다. 하지만 실제로는 UseCase가 대상이 되어야 한다.
또 한 가지 시작이 아닌, 종료 시점을 이해하기 위해서는 사용자 케이스에 따른 처리가 필요하고 ATDD에서는 AC가 `언제 코드 작성을 멈춰야 하는가?`에 대한 답을 할 수 있다. 
![스크린샷 2021-05-03 오전 5 59 53](https://user-images.githubusercontent.com/10345220/116827601-cf0bb700-abd4-11eb-8c92-8c8e0923efd7.png)



### 3. 단위테스트와 전구간(End-2-End) 테스트 모두 작성해야 할까?

### 4. 테스트 개발을 주도한다는 뜻은 무엇일까?

### 5. 복잡한 기능을 어떻게 테스트 할 수 있을까?



그 외에 갖춰야 하는 것들..
```
더 높은 수준의 절차가 필요함(절차)
디자인 원칙(OOP)
사용한 도구(Tool)
```

> 시스템 품질을 높이려면 테스트를 기반으로 개발을 진행하고 테스트로부터 피드백을 받는 데 집중해야 한다.

`피드백`은 가장 기본적인 도구이다.
> 배포하지 않고는 피드백이 완전해지지 않는다. 피드백을 통하여 배우고 이를 개선해 가야 한다.


### 신뢰적인 시스템 성장을 위해 필요한 2가지

(1) 테스트 코드
(2) 코드를 단순하게 유지하는 방법


### TDD에 대한 잘못된 이해

(1) TDD를 `작업 결과에 대한 검증`으로 생각 하는 것 => 실제는 `테스트 설계 활동`을 변경하는 것

### 리팩토링

(1) 작은 단위로의 리팩토링이 끊임없이 이루어져야 => 구조적인 리팩토링으로 이어 질 수 있다.

<br/>

## 품질

- 외부 품질
`외부 품질`은 시스템이 고개과 사용자의 요구를 얼마나 충족하는가이다.(기능, 신뢰성, 가용성, 응답성 등) <br/>
전 구간 테스트(End-2-End Test)를 통하여 확인 가능하다. 


- 내부 품질
`내부품질`은 거듭되고 예상할 수 없는 변경에 대처하게 하는 것으로 동작방식을 안전하고 예상 가능한 상태로 바꾸는 것이다. <br/>
단위 테스트가 있다면 코드 품질을 확인가능하다.




## 객체 설계
객체 설계 시 유의하면 좋을 점을 확인하기 위하여 객체가 어떤 것인지 디자인 관계에서 살펴보자.


### 설계
고수준의 선언적 접근법을 사용해서 How가 아니라 What에 집중 할 수 있도록 한다. <br/>
이를 위하여 추상 클래스를 적극 활용한다. `도메인 모델`이 바로 이런 객체 간의 의사소통 관계를 의미한다.

- CRC(Candidate, Responsiblity, Collaboration) 방식 소개
중요한건 사용자,요구자의 의견이 어떻게 반영되었는가. 어떤 형식으로 풀고 어떻게 정의하였는가가 설계에서 가장 중요하다는걸 느꼈다.
[참고](https://uiandwe.tistory.com/465)

![스크린샷 2021-05-03 오전 6 48 07](https://user-images.githubusercontent.com/10345220/116828740-87d4f480-abdb-11eb-8f74-cb894dfa1c8e.png)


### 값과 객체
- 값: 변하지 않거ㅏ나 양이나 크기를 나타낸다.
- 객체: 시간이 지남에 따라 상태가 변할지 모르지만 식별자가 있는 계산 절차를 나타낸다.


### 결합도와 응집도
- 결합도: 한 변경이 다른 변경을 강제한다면, 요소들이 결합된 상태이다. e.g) 공통부모를 상속받은 경우 자녀들 하나를 변경하면 다른 하나를 더 변경해야 할 수 있다.
- 응집도: 비슷한 기능끼리 묶어두는 것 

### 묻지말고 답하라

`전복열차` 혹은 `디미터 법칙`을 생각하라.

- BAD
```
if (carriage.getSeats().getPercentReserved() < percentageBarrier) {
...
}
```

- GOOD
```
if ( carriage.hasSeatAvailableWithic(percentageBarrier) ) {
...
}

```

## Links
- [StandUp Meeting](https://martinfowler.com/articles/itsNotJustStandingUp.html)
- [programming methods](https://medium.com/@filzahafidzahf5/sdlc-waterfall-agile-extreme-programming-methods-88eda4de6858)
- [XP advantage](https://www.altexsoft.com/blog/business/extreme-programming-values-principles-and-practices/)
