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

## 라이프 사이클
not running > inactive > active > inactive background > suspended > not running
- application(_:willFinishLaunchingWithOptions:) : 앱이 구동되어 필요한 초기 실행 과정이 완료되기 직전에 호출되는 메소드
- application(_:didFinishLaunchingWithOptions:) : 앱이 사용자에게 화면으로 표기되기 직전에 호툴되는 메소드.
- applicationDidBecomeActive(_:) : 실행된 앱이 포그라운드 즉 화면 전면에 표시될때 호출되는 메소드 입니다. inactive상태에서 active로
- applicationDidEnterBackground(_:) : 앱이 백그라운드 상태에 진입했을때 호출
- applicationWillTerminate(_:) : 앱이 종료되기 직전에 호출되는 메소드

## 코코아 터치 프레임워크
- ios에 코코아 터치가 내장되어 있고 코코아 터치 프레임워크를 통해 해당 기능을 사용하도록 구현 한다.

## UI구조 
- 윈도우 : 루트 뷰 컨트롤러만 관리한다.
- 뷰 컨트롤러
- 뷰
- 씬
- 컨텐츠 뷰 컨트롤러 : 씬 담당 콘텐츠 표시
- 컨테이너 뷰 컨트롤러 : 탭 바, 페이지
- 루트 뷰 컨트롤러 : 
- 뷰 계층 구조 : 슈퍼 뷰, 서브 뷰
- 루트 뷰(=컨텐츠 뷰)

