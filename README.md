# swift
참고서적 : 꼼꼼한 재은씨의 swift:기본편

## 화면 구성 객체
- UIScreen : 기기에 연결되는 물리적인 화면을 정의하는 객체
- UIWindow : 화면 그리기 자원 도구를 제공하는 객체
- UIView : 그리기를 수행할 객체 세트
  
화면을 구성할때 Window에 뷰 객체를 바로 할당하지 않고 뷰 컨트롤러에 할당하는 컨트롤러의 역할이 보강된 mvc 패턴
  
Screen < Window > View controller > UIView

## single view application 구성
xcode를 이용해 swift single view application 프로젝트를 생성하면 AppDelegate.swift, ViewController.swift, Main.storyboard, LaunchScreen.storyboard, Assets.xcassets, Info.plist 파일로 구성 된다. 
- AppDelegate.swift : 앱 생명주기 관리, 앱 실행 종료 활성 비활성 백그라운드 등 상태 변화시 처리 클래스
- ViewController.swift : 뷰 컨트롤러로 일반적으로 화면 개수 만큼 필요하며, 첫번째 화면의 뷰 컨트롤러
- *.storyboard : 유저 인터페이스 구현
  
## 버튼 눌러 인사하기
- 라이브러리 영역에서 라벨과 버튼 객체를 드래그하여 뷰 컨트롤러에 추가하고 추가된 객체들을 editor에 드래그 하면 해당 view 개체에 대한 소스 연결 작업이 완료 된다. 매우 명시적이다. 드래그 하며 자동 생성되는 소스 코드에 대한 확인은 필요하다. 보통 인스펙터 창의 Connections Inspector 탭을 열면 드래그하여 발생된 연결 관계등을 알수 있다.
