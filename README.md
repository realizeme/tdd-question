## TDD에 관한 중요 질문


1. 어떻게 해야 테스트 주도 개발을 잘 적용할 수 있을까?


2. 어디서 시작해야 할까?
Usecase(Acceptance Critieria)에서 시작해야 한다. 보통은 백엔드 개발자는 API라고 생각해서 Controller가 대상이 되기도 한다. 하지만 실제로는 UseCase가 대상이 되어야 한다.
또 한 가지 시작이 아닌, 종료 시점을 이해하기 위해서는 사용자 케이스에 따른 처리가 필요하고 ATDD에서는 AC가 `언제 코드 작성을 멈춰야 하는가?`에 대한 답을 할 수 있다. 
![스크린샷 2021-05-03 오전 5 59 53](https://user-images.githubusercontent.com/10345220/116827601-cf0bb700-abd4-11eb-8c92-8c8e0923efd7.png)



3. 단위테스트와 전구간(End-2-End) 테스트 모두 작성해야 할까?

4. 테스트 개발을 주도한다는 뜻은 무엇일까?

5. 복잡한 기능을 어떻게 테스트 할 수 있을까?


그 외에 갖춰야 하는 것들..

더 높은 수준의 절차가 필요함(절차)
디자인 원칙(OOP)
사용한 도구(Tool)


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

## Links
[StandUp Meeting](https://martinfowler.com/articles/itsNotJustStandingUp.html)
[programming methods](https://medium.com/@filzahafidzahf5/sdlc-waterfall-agile-extreme-programming-methods-88eda4de6858)
[XP advantage](https://www.altexsoft.com/blog/business/extreme-programming-values-principles-and-practices/)
