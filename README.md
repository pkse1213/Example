# 9. iOS 아키텍처

### 좋은 아키텍처란?
* 각각의 객체들은 구체적이고 명확한 역할을 가져야 함
* 테스트 가능성
* 사용의 용이성, 낮은 유지 보수 비용
* 단순한 데이터 흐름. 쉬운 디버깅
* 관심사의 분리

# 9-1. MVC (Model-View-Controller)

>`MVC`는  프로그램을 짜는 대표적인 디자인 패턴 중 하나
>
>Model과 View, 그리고 Controller 세가지 요소로 구성 되어 있음

![](/images/Architecture/MVC.png)

## Model
 앱의 비즈니스 로직과 데이터를 관장하는 영역

## View
 유저에게 데이터를 보여주거나, UI를 담당하는 영역

> View는 *'어떻게'* 보여질지에 대해서만 관장하고 *'어떤 것'*을 보여줄 지에 대해서는 알지 못함

## Controller
 View와 Model을 이어주는 역할

 앱 전체의 로직과 인터페이스를 관장하는 영역

> UI에서 일어나는 일을 판단하고 Model을 업데이트, Model에 변동이 생기면 UI에도 변화가 생김

## MVC의 단점
* View Controller의 코드가 비대해짐
* View는 아무일도 하지 않음
* Model은 그저 단순한 Data 구조일 뿐
* View Controller는 View의 라이프 사이클과 강하게 역여 있어, 재사용이 불가능
* View와 Controller의 상호작용 (user action과 그에 따른 로직)은 unit test에서 테스트할 수 없음

# 9-2. MVVM (Model-View-ViewModel)

>`MVVM`은 Model과, View, 그리고 View Model 로 구성된 소트트웨어 아키텍처 패턴

![](/images/Architecture/MVVM.png)










