Tilt Dot - 안드로이드 앱(APK) 만들기

[방법 A] GitHub로 만들기 (내 컴퓨터에 Android Studio 불필요)
1. github.com 에 가입/로그인한 뒤 New repository 로 새 저장소를 만듭니다.
2. 이 폴더 안의 모든 파일과 폴더(.github 폴더 포함)를 저장소에 업로드합니다.
   (Add file > Upload files 에 폴더째 끌어다 놓기)
3. 저장소의 Actions 탭 > "Build Android APK" > Run workflow 를 누릅니다. (업로드하면 자동 실행되기도 합니다.)
4. 5~10분 뒤 실행 결과 화면 맨 아래 Artifacts 의 TiltDot-apk 를 내려받아 압축을 풀면 app-debug.apk 가 있습니다.
5. APK 를 안드로이드 폰으로 옮겨 열고, "출처를 알 수 없는 앱 설치"를 허용하면 설치됩니다.

[방법 B] 내 컴퓨터에서 만들기
1. Node.js 와 Android Studio 를 설치합니다.
2. 이 폴더에서 아래 명령을 차례로 실행합니다.
     npm install
     npx cap add android
     npx cap sync android
     npx cap open android
3. Android Studio 에서 Build > Build Bundle(s) / APK(s) > Build APK(s) 를 누르면 APK 가 만들어집니다.

참고
- 게임 파일은 www/index.html 입니다. 수정하면 다시 빌드해야 반영됩니다.
- 이 APK 는 디버그 서명 버전이라 직접 설치용입니다. 플레이스토어 등록에는 별도의 릴리스 서명이 필요합니다.
