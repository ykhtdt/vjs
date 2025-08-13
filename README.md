# VJS

## 실행 가이드

아래 명령만 순서대로 실행하면 로컬에서 프로젝트를 바로 확인할 수 있습니다.

### 1. 요구사항 설치/확인
PowerShell에서 Node.js와 npm이 있는지 확인합니다. 없다면 Node.js를 설치하세요.
```bash
node -v
npm -v
```

### 2. 프로젝트 루트에서 서버 실행
현재 디렉터리(`vjs`)를 5500 포트로 서빙합니다.
```bash
npx serve -l 5500
```
브라우저에서 `http://localhost:5500` 접속.

### 3. 특정 폴더(`example/`)만 서빙
프로젝트 루트에서 `example` 폴더만 루트로 지정해 서빙합니다.
```bash
npx serve -l 5500 example
```
또는 폴더로 이동 후 실행합니다.
```bash
cd example
npx serve -l 5500
```

### 4. 포트가 사용 중일 때
다른 포트를 지정해 실행합니다.
```bash
npx serve -l 5501
```

### 참고
`npx serve -l 5500`은 Node.js/npm 기반 도구(`npx`, `serve`)를 사용해 정적 파일을 제공합니다. 추가 설치 없이 일회성으로 실행할 수 있으며, 자주 사용한다면 다음과 같이 글로벌 설치 후 사용할 수 있습니다.
```bash
npm i -g serve
serve -l 5500
```
