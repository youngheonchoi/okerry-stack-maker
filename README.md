# okerry-stack-maker

앱인토스 출시를 위한 React + TypeScript + Vite 기반 웹 미니앱 프로젝트입니다.

## 개발

Node.js 24 이상과 npm을 사용합니다.

```bash
npm ci
npm run dev
```

브라우저 하단 AIT 버튼에서 개발 도구를 열고 Viewport 탭에서 모바일 화면 크기를 선택하세요. 출시 전에는 실제 토스 앱에서도 확인하세요.

## 검증과 번들 생성

```bash
npm run lint
npm run build
```

build는 TypeScript 검사, Vite 빌드, 앱인토스 번들 생성을 순서대로 실행합니다. 생성된 dist/와 *.ait는 Git에서 제외됩니다.

## 앱인토스 설정과 출시

- 앱 식별자, 브랜드 색상, 권한: apps-in-toss.config.ts
- 화면 구현 기준: AGENTS.md, docs/design-guide.md
- 스타일 토큰과 기본 스타일: src/styles/
- 개발 도구 설정: vite.config.ts

기능과 화면을 구현한 뒤 콘솔 앱 등록, 실기기 테스트, 검수 요청 절차를 진행하세요. 프로젝트 생성만으로 콘솔 등록이나 출시가 완료되지는 않습니다.

Tossface 서체는 CDN으로 연결됩니다. 오프라인에서는 시스템 이모지로 대체되며, 오프라인 서체가 필요하면 번들에 포함하도록 변경할 수 있습니다.

## Git 관리

원격 저장소: https://github.com/youngheonchoi/okerry-stack-maker.git

의존성, 빌드 산출물, 로그, 환경 변수, 인증서와 개인키는 .gitignore로 제외합니다. 환경 변수 예시는 실제 비밀값 없이 .env.example에 작성하세요. package-lock.json은 커밋합니다.
