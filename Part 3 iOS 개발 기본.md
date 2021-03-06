# Part 3. IOS 개발 기본

### 개발 하면서 준비해야 할 것

- 앱이 포그라운드 들어갈 때
  - 이니셜 UI 준비
  - 사용자와의 인터랙션 준비
- 포그라운드를 떠날 때
  - 데이터 저장
  - 앱의 작업을 최소화할 준비
- 백그라운드 들어갔을 때
  - 앱의 작업을 중단
  - 메모리 비우기
  - 현재 상태를 저장해놓고 다음을 준비

<hr>

### Ios 앱에서 뷰의 역할

- 앱에서 가지고 있는 데이터를 사용자에게 보여줌
- 사용자의 인터랙션을 받아서 앱에 알려줌

<br>

### UIKit (storyboard)

- 장점
  - 뷰를 위한 코드를 적게 작성 가능
  - 직관적으로 이해하기 쉬움
  - 작업 속도가 빠름
- 단점
  - 작업 내용을 보기가 어려움 → 충돌 발생 시, xml 수정하기 어렵다
  - 재사용성이 낮음
  - 동적 변화에 제약

<br>

### UIKit (code)

- 장점
  - 작업 내용을 보기가 쉬움
  - 재사용성 높음
  - 동적 변화에 제약이 적다
- 단점
  - 뷰를 위한 코드 많이 필요
  - 직관적인 이해 어려움
  - 작업 속도가 느림
    - 재사용성이 높아짐에 따라, 속도는 향상 가능

<br>

### SwiftUI

- 장점
  - 작업 내용을 보기가 쉬움
  - 재사용성 높음
  - 코드 적게 작성 가능
  - 직관적인 이해 가능
  - 작업 속도 빠름
- 단점
  - 대부분 프젝은 UIKit 기반이 많다
  - 버젼 별로 되는 UI가 있어, 분기를 태워 버전별로 관리 해야함

<hr>

### model, view 사이의 관계

- Model
  - 데이터
- View
  - 데이터 표현 객체
- model과 view 사이의 매개체를 통해 통신

<br>

- 기본적으로 MVC (model - view - controller) 패턴을 가이드 함
- 더 좋은 구조, 지속가능한 방법
  - 디자인 패턴들 MVVM, MVP, VIPER, Ribs,…
  - 아키텍처에 대한 고민 → 클린 아키텍처
  - 멀티 모듈 아키텍처

<hr>

### SF Symbols

- 애플에서 기본적으로 제공하는 아이콘 모음집
- 원하는 아이콘 클릭하여 ctrl + shift + c, imageview의 image에 붙여넣기

<hr>

### 오토레이아웃

Why?

- 프레임 기반 레이아웃의 문제
  - 동적으로 뷰를 위치 시킬 수 없음
  - 스크린별로 일일이 계산해줘야 함

What?

- 자동으로 의도를 정해주면, 알아서 위치하게 되는 기술

How?

- Constraint(제약사항)를 통해 오토레이아웃을 적용
- 적용 시, 뷰는 아래의 두 개 기준을 충족해야 함
  - 위치를 알 수 있어야 함
  - 크기를 알 수 있어야 함

<hr>

### 프로젝트 : 심볼 롤러

- viewDidLoad()
  - 페이지가 스크린에 보일 때, 필요한 내용들이 로드됨
- @IBOutlet
  - interfacebuilder에 있는 요소와 코드를 연결
- @IBAction
  - 요소의 action 설정
- DRY
  - Do not repeat yourself
  - 코드가 중복되는 부분을 최소화해라