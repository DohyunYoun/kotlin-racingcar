# 1주차 : kotlin-racingcar
## Step3 : 자동차 경주
### 요구사항
1. 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
2. 사용자는 몇 대의 자동차로 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
3. 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
4. 자동차의 상태를 화면에 출력한다. 어느 시점에 출력할 것인지에 대한 제약은 없다.
5. 모든 로직에 단위 테스트를 구현한다. 단, UI(System.out, System.in) 로직은 제외
   - 핵심 로직을 구현하는 코드와 UI를 담당하는 로직을 구분한다.
   - UI 로직을 InputView, ResultView와 같은 클래스를 추가해 분리한다.
   
### 할 일
* 테스트 코드 작성
  * [x] 입력한 숫자 만큼 자동차가 생성된다.
  * [x] 게임결과는 입력한 숫자보다 많을 수 없다.
* [x] 사용자의 입력을 받는 InputView 생성(자동차 대수, 시도 횟수)
* [x] 결과를 출력하는 ResultView 생성
  * 자동차 대수만큼 출력된다
  * 횟수는 line으로 구분된다
  * 전진 시 "-"를 출력하며, 멈춤 시 아무것도 출력하지 않는다.
* [x] 게임 결과를 기록하는 자동차 객체 생성
* [x] 잘못된 입력(공백, 숫자가 아닐때 등)에 대한 예외처리
* [x] 입력된 자동차 대수와 시도횟수에 따라 경기 결과를 출력한다.
* 코드리뷰 반영
  * [x] Car 클래스의 책임 분리
    * run/moveOrStop
    * getRandomNumber
    * record
  * [x] 함수명 변경(자료형이 오는것은 지양하는것이 좋다. Int는 포괄적이기 때문에 구체적으로 어떤것을 의미하는지 알기 어렵다.)
  * [ ] 함수 분리 (중첩문 개선)
  * [x] RacingGame에서 멤버변수가 아닌 생성자로 처리하여 게임만 하도록 역할을 명확히 해보기
  * [x] 불필요한 코드 정리(printNextRacing)
  * [ ] 자동차 이동여부에 대한 테스트코드 작성

## Step2 : 문자열 계산기
### 요구사항
1. 사칙연산의 계산우선순위가 아닌 입력값에 따라 계산순서가 결정된다
   (예 : 2 + 3 * 4 / 2 = 10)
2. 메서드를 최대한 분리시킨다.

### 할 일
* [x] 계산 로직 테스트 코드 작성
  * 덧셈
  * 뺄셈
  * 곱셈
  * 나눗셈
  * 사칙연산을 모두 포함 하는 경우
* [x] 계산 로직 구현
* [x] 예외처리 테스트 코드 작성
  * 입력값이 null이거나 빈 공백 문자일 경우
  * 사칙연산 기호가 아닌 경우
  * 식이 올바르지 않은 경우
* [x] 예외처리 추가
* 코드리뷰 반영
  * [x] 상수는 companion object에서 const로 정의하는 것이 좋다
  * 함수의 역할 분리 (객체에 해당하는 책임을 넘긴다) 
    * [x] 계산을 위한 식을 구하는 객체 구현
    * [x] 실제 계산을 수행하는 함수 분리
    * [x] 주석이 아닌 함수로 처리
  * [x] 매직 리터럴 바꾸기
  * [x] 코틀린 함수 활용
  * [x] enum class에 인터페이스/람다 활용([💡](https://kotlinlang.org/docs/enum-classes.html#implementing-interfaces-in-enum-classes))
  * [x] 테스트 코드 kotest로 통일
  * [x] 불필요한 확장함수를 일반함수로 변경 (해당 클래스에서만 사용하기 때문에 확장함수를 구현할 필요가 없다.)
  * [x] 변수명을 명확하게 변경
  * [x] mutable일 필요가 없는 변수들을 immutable로 변경
  * [x] 계산하는 함수명 변경 및 통합 (함수명 : 행동, 동사구 / 변수명 : 명사구)
  * [x] 테스트명을 명확하게 변경

## Step1 : 코틀린 기초
- 간단한 Person 클래스 생성
- 테스트 코드 작성
