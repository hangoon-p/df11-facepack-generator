# FM 페이스팩 생성기

브라우저에서 선수 사진을 편집해 DF11, 건조, 컷아웃 형식의 PNG 페이스팩을 만드는 정적 웹 앱입니다.

## 주요 기능

- 파일 선택, 드래그 앤 드롭, Ctrl+V로 사진 업로드
- 사진 이동, Shift 고정 이동, 슬라이더 및 마우스 휠 확대·축소
- DF11 260×310, 건조 350×350, 컷아웃 250×250 출력
- 건조 제작기 기반 필터 3종과 개별 적용 강도
- IMG.LY 브라우저 배경 제거
- 건조폼 선수 이름 및 글자 크기 설정
- 선수 ID를 파일명으로 사용한 PNG 다운로드

사진 처리는 브라우저 안에서 진행됩니다. 배경 제거를 처음 사용할 때 약 80MB의 AI 모델을 내려받을 수 있습니다.

## 로컬 실행

ES 모듈과 외부 배경 제거 모듈을 사용하므로 index.html을 파일로 직접 열기보다 로컬 웹 서버로 실행하는 편이 안전합니다.

    python -m http.server 8000

그다음 브라우저에서 http://localhost:8000 을 여세요.

## GitHub Pages 게시

1. GitHub에서 새 공개 저장소를 만듭니다.
2. 이 폴더 안의 index.html, assets, README.md, .nojekyll을 저장소 최상위에 업로드합니다.
3. 저장소의 Settings → Pages로 이동합니다.
4. Build and deployment에서 Deploy from a branch를 선택합니다.
5. 브랜치는 main, 폴더는 /(root)를 선택하고 저장합니다.
6. 잠시 후 표시되는 GitHub Pages 주소로 접속합니다.

## 폴더 구조

    .
    ├── index.html
    ├── assets/
    │   ├── frame.png
    │   ├── frame-mask.png
    │   ├── og4.png
    │   ├── filter2.png
    │   ├── filter3.png
    │   ├── filter4.png
    │   ├── BebasNeue.otf
    │   └── koverwatch.ttf
    ├── README.md
    └── .nojekyll

## 배포 전 확인

- 배경 제거 기능은 jsDelivr에서 @imgly/background-removal 1.7.0 모듈을 불러옵니다.
- 프레임, 필터 및 폰트 자산은 기존 DF11·건조 제작기 자료를 바탕으로 구성되었습니다.
- 공개 배포 전에 포함된 이미지와 폰트의 사용·재배포 조건을 직접 확인하세요.

