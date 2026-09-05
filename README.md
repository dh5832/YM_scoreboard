# 팀별 점수판 - GitHub Pages 사용법

이 버전은 GitHub Pages에서 사용할 수 있도록 정리된 단일 HTML 앱입니다.

## 가장 간단한 배포 방법

1. GitHub에서 새 저장소(repository)를 만듭니다.
2. 이 폴더의 `index.html` 파일을 저장소 최상위(root)에 업로드합니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Build and deployment → Source**에서 `Deploy from a branch`를 선택합니다.
5. Branch를 `main`, Folder를 `/(root)`로 선택하고 Save 합니다.
6. 잠시 후 표시되는 `https://사용자이름.github.io/저장소이름/` 주소로 접속합니다.

## 이 버전이 GitHub Pages에 맞는 이유

- 하나의 `index.html`만 사용합니다.
- 이전 기록은 `#history` 해시 라우팅으로 열기 때문에 새로고침해도 404가 발생하지 않습니다.
- PDF 미리보기 역시 같은 페이지의 `#print=...` 모드로 열립니다.
- GitHub Pages의 같은 HTTPS origin에서 `localStorage`를 공유하므로 메인/이전기록/PDF 탭이 같은 기록을 읽습니다.
- `file://` 환경에서 필요했던 URL에 전체 기록을 넣는 방식이나 `window.name` 우회는 사용하지 않습니다.

## 데이터 저장 방식

점수와 이전 게임 기록은 GitHub 서버에 저장되는 것이 아니라 **현재 브라우저의 localStorage**에 저장됩니다.

따라서:
- 같은 브라우저에서 새로고침하거나 다시 접속하면 기록이 유지됩니다.
- 다른 PC/휴대폰에는 자동으로 기록이 나타나지 않습니다.
- 브라우저 사이트 데이터를 삭제하면 기록도 삭제될 수 있습니다.

중요한 기록은 화면의 **기록 백업** 버튼으로 JSON 파일을 저장해두세요.
다른 PC에서는 **백업 복원**으로 옮길 수 있습니다.

## 여러 기기에서 같은 기록을 공유하려면

정적 GitHub Pages + localStorage만으로는 실시간 공유가 불가능합니다.
여러 교사가 여러 기기에서 같은 기록을 같이 봐야 한다면 다음 단계로 Firebase Firestore 또는 Supabase 같은 데이터베이스를 붙이는 것을 권장합니다.
