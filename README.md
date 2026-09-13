# DF11 페이스팩 생성기

투명 배경의 선수 사진을 DF11 프레임에 배치하고 `선수ID.png`로 저장하는 정적 웹 도구입니다.

## GitHub Pages 배포

1. GitHub에서 새 저장소를 만듭니다.
2. 이 ZIP 파일의 내용물을 압축 해제하여 저장소 최상위 경로에 업로드합니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Build and deployment**에서 Source를 **Deploy from a branch**로 선택합니다.
5. Branch를 `main`, 폴더를 `/(root)`로 선택하고 **Save**를 누릅니다.
6. 배포가 완료되면 `https://계정명.github.io/저장소명/`으로 접속합니다.

## 로컬 실행

별도의 설치나 빌드 과정이 없습니다. `index.html`을 브라우저에서 직접 열어도 동작합니다.

## 파일 구성

- `index.html` — 화면, 스타일, 이미지 편집 기능
- `assets/frame.png` — DF11 배경 및 프레임
- `assets/frame-mask.png` — 선수 사진 표시 영역 마스크
- `.nojekyll` — GitHub Pages의 Jekyll 처리를 비활성화

사진 합성은 사용자의 브라우저 안에서만 처리되며, 업로드한 사진은 서버로 전송되지 않습니다.

