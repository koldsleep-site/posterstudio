# textbox / Poster Studio

독립형 포스터 제작 도구. KR/EG 편집, QR 코드 생성, PDF·JPG·SVG·EPS 내보내기.

## 최종 레이아웃 · 2026-10-09

- 정보 박스 안쪽 구분선 제거
- QR 코드 주변 흰 여백 4모듈
- 구분선이 사라진 날짜 아래 세로 간격 10(포스터 내부 좌표)
- QR 코드 아래 URL 텍스트 오른쪽 정렬

## GitHub Pages

GitHub 저장소: https://github.com/koldsleep-site/posterstudio

`index.html`, `poster-studio.js`, `poster-studio.css`, `assets/`, `vendor/` 등 파일을 저장소 루트에 그대로 업로드한 뒤 Settings → Pages → Deploy from a branch → `main` / `/(root)` 로 설정합니다.

배포 예상 주소: https://koldsleep-site.github.io/posterstudio/

## 구성

- `index.html`: 배포 페이지
- `poster-study.html`: 동일 제작 화면
- `poster-studio.js`, `poster-studio.css`: 제작 기능 및 UI
- `assets/`, `vendor/`: 서체·라이브러리, 라이선스 포함
- `backend/translator-worker.js`: 번역 Cloudflare Worker 소스; 별도 배포 필요

## 유의 사항

자동 영문 번역용 Cloudflare Worker는 현재 별도 허용 출처를 사용합니다. GitHub Pages 도메인에서도 번역을 사용하려면 Worker의 허용 출처에 `https://koldsleep-site.github.io`를 추가하고 배포해야 합니다. 포스터 편집과 파일 출력은 이 번역 기능과 별개입니다.
