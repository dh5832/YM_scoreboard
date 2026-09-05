# 팀별 점수판 — 100% 무료 GitHub Pages 버전

이 버전은 **유료 서비스 없이** 사용하도록 구성되어 있습니다.

## 사용 비용

- GitHub Free 계정: 무료
- 공개(Public) GitHub 저장소: 무료
- GitHub Pages: 무료
- `github.io` 기본 주소: 무료
- 점수/이전기록 저장(localStorage): 무료
- PDF 저장: 브라우저 기본 인쇄 기능 사용, 무료
- JSON 기록 백업/복원: 무료
- 외부 데이터베이스/API: 사용하지 않음
- GitHub Actions: 사용하지 않음

즉, 별도의 결제수단이나 서버가 필요하지 않습니다.

## GitHub에 올리는 방법

1. GitHub에서 새 저장소를 만듭니다.
2. 저장소는 반드시 **Public**으로 만듭니다.
   - GitHub Free에서 GitHub Pages를 무료로 쓰기 위한 구성입니다.
3. 이 폴더의 아래 파일을 저장소 최상위(root)에 올립니다.
   - `index.html`
   - `.nojekyll`
4. GitHub 저장소에서 **Settings → Pages**로 이동합니다.
5. **Build and deployment**
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/(root)`
6. Save를 누릅니다.
7. 잠시 뒤 표시되는 주소로 접속합니다.
   - 예: `https://사용자이름.github.io/저장소이름/`

GitHub Actions 워크플로는 만들 필요가 없습니다.

## 기록은 어디에 저장되나요?

점수와 이전 게임 기록은 GitHub 서버가 아니라 **접속한 브라우저의 localStorage**에 저장됩니다.

### 유지되는 경우
- 같은 PC
- 같은 브라우저
- 같은 GitHub Pages 주소
- 새로고침
- 브라우저 종료 후 다시 접속

### 자동 공유되지 않는 경우
- 다른 PC
- 다른 휴대폰
- 다른 브라우저

다른 기기로 기록을 옮길 때는 점수판의:

- `💾 기록 백업`
- `📥 백업 복원`

기능을 사용하세요.

## 꼭 알아둘 점

GitHub Free에서 GitHub Pages를 무료로 사용하는 이 구성은 **Public 저장소**를 사용합니다.
따라서 `index.html` 소스 코드는 다른 사람이 볼 수 있습니다.

하지만 **실제 점수 기록과 이전 게임 기록은 GitHub에 업로드되지 않습니다.**
기록 데이터는 각 브라우저의 localStorage에만 저장됩니다.

## 완전 무료로 유지하려면

아래 서비스는 필요하지 않습니다.

- Firebase
- Supabase
- 유료 서버
- 유료 도메인
- 유료 데이터베이스
- GitHub Pro
- GitHub Actions 기반 별도 배포

이 프로젝트는 `index.html + .nojekyll`만으로 운영하면 됩니다.
