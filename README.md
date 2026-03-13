# 예다함투어 (YedahamTour) Android App

예다함 SMG TOUR 웹사이트(https://yedahamtour.com)의 Android WebView 앱입니다.

## 주요 기능

- **WebView** 기반 웹앱 (yedahamtour.com)
- **스플래시 화면** - 앱 실행 시 예다함 SMG TOUR 로고 표시
- **당겨서 새로고침** (SwipeRefreshLayout)
- **뒤로가기** 버튼으로 웹 히스토리 탐색
- **외부 링크 연동** - 전화(tel:), 이메일(mailto:), 외부 URL은 네이티브 앱/브라우저로 처리
- **오프라인 화면** - 인터넷 미연결 시 재시도 버튼 제공
- **로딩 프로그레스바** - 페이지 로딩 상태 표시

## 개발 환경

| 항목 | 버전 |
|------|------|
| Android Studio | 2024.3.x (Meerkat) |
| AGP | 8.10.1 |
| Kotlin | 2.0.21 |
| Gradle | 8.13 |
| compileSdk | 35 |
| minSdk | 26 |
| targetSdk | 35 |

## 프로젝트 구조

```
app/src/main/
├── java/com/yedaham/tour/
│   ├── MainActivity.kt        # WebView 메인 화면
│   └── SplashActivity.kt      # 스플래시 화면
├── res/
│   ├── layout/
│   │   ├── activity_main.xml   # WebView + 오프라인 + 프로그레스바
│   │   └── activity_splash.xml # 스플래시 레이아웃
│   ├── drawable-nodpi/
│   │   └── splash_logo.png     # 스플래시 로고 이미지
│   ├── mipmap-*/
│   │   └── ic_launcher.png     # 앱 아이콘 (각 해상도)
│   ├── values/
│   │   ├── colors.xml          # 테마 색상 (골드/크림)
│   │   ├── strings.xml
│   │   └── themes.xml
│   └── xml/
│       └── network_security_config.xml
└── AndroidManifest.xml
```

## 빌드

```bash
./gradlew assembleDebug    # 디버그 빌드
./gradlew assembleRelease  # 릴리즈 빌드
```

## 설치

```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```
