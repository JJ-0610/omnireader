# OmniReader (GitHub Pages PWA 이북리더)

아이폰(iOS), 안드로이드(Android), 윈도우(Windows) 브라우저에서 설치 및 오프라인 실행이 가능한 PWA 기반 이북리더입니다.

## 포함된 파일
- `index.html`: 메인 앱 (TXT · EPUB · PDF 뷰어, TTS 스마트 필터, 폰트·여백 커스터마이징, E-Ink 고대비 테마, 하이라이트/메모 및 마크다운 내보내기, GitHub Gist 동기화)
- `manifest.json`: PWA 앱 설치 매니페스트 (GitHub Pages 하위 경로 호환용 상대 경로 적용)
- `sw.js`: 오프라인 캐싱용 Service Worker
- `icon.svg`: 앱 아이콘

## GitHub Pages 배포 방법
1. GitHub에서 새 저장소(Repository)를 생성합니다. (무료 계정의 경우 **Public** 설정 필요)
2. 압축을 푼 5개 파일(`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md`)을 저장소 최상위(루트)에 업로드합니다.
3. 저장소 상단 **Settings** → 좌측 메뉴 **Pages**로 이동합니다.
4. **Build and deployment > Source**를 `Deploy from a branch`로 두고, 브랜치를 `main`, 폴더를 `/ (root)`로 선택한 뒤 **Save**를 누릅니다.
5. 1~2분 후 생성되는 `https://<본인아이디>.github.io/<저장소이름>/` 주소로 접속합니다.

## 기기별 PWA 설치 방법
- **아이폰(Safari):** 주소 접속 → 하단 공유 버튼 → **홈 화면에 추가**
- **안드로이드(Chrome):** 주소 접속 → 우측 상단 메뉴(⋮) → **앱 설치** 또는 **홈 화면에 추가**
- **윈도우(Chrome/Edge):** 주소창 우측의 **앱 설치(아이콘)** 또는 앱 상단의 **앱 설치** 버튼 클릭

## 기기 간 동기화(GitHub Gist) 사용법
GitHub Pages는 정적 호스팅이므로 자체 데이터베이스가 없습니다. 앱 상단의 **동기화 / 백업** 메뉴에서 다음 두 가지를 지원합니다.
1. **GitHub Gist 동기화:** GitHub `Settings > Developer settings > Personal access tokens`에서 `gist` 권한만 부여한 토큰을 발급받아 입력하면, 읽기 진행률·하이라이트·메모·설정을 비공개 Gist로 기기 간 동기화할 수 있습니다. (단, 대용량 책 원본 파일 자체는 각 기기 로컬 `IndexedDB`에 저장됩니다.)
2. **JSON 백업/복원:** 설정 및 독서 데이터를 `.json` 파일로 내보내고 다른 기기에서 불러올 수 있습니다.
