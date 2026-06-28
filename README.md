# 안정호 포트폴리오 웹사이트

다크 옐로 톤의 단일 페이지 스크롤 포트폴리오. 17년 차 디지털·그로스·커머스 마케팅 리더 안정호의 마스터 포트폴리오(2차 웹).

태그라인: **광고를 넘어, 사업을 키웁니다.**

## 시작하기

먼저 다음 두 문서를 읽으세요.

- `CLAUDE.md` — 절대 규칙, 디자인 토큰, 사이트 로드맵 (Claude Code가 자동 로드)
- `HANDOFF.md` — 작업 히스토리, 결정 배경, 다음 할 일
- `content/career-source.md` — 섹션 제작용 콘텐츠 원본(브랜드·케이스·수치)

## 로컬에서 보기

빌드 없는 정적 사이트. 아무 정적 서버로 열면 됩니다.

```bash
# 파이썬
python3 -m http.server 5173
# 또는 npx
npx serve .
```

브라우저에서 `http://localhost:5173` 접속. 현재는 `index.html`(히어로)만 있습니다.

## 구조

```
ahn-portfolio/
  index.html              # 히어로 (완성). 여기에 섹션을 이어 붙여 한 페이지로 확장
  CLAUDE.md               # 운영 브리프 (규칙 + 디자인 토큰 + 로드맵)
  HANDOFF.md              # 작업 히스토리 + 핸드오프
  README.md
  content/
    career-source.md      # 콘텐츠 원본 (재료)
  assets/                 # 실제 이미지/소재 (현재 비어 있음, placehold.co로 대체 중)
```

## 배포

빌드가 없어 GitHub Pages가 가장 간단합니다.

```bash
git init && git add -A && git commit -m "hero"
# GitHub repo 생성 후
git remote add origin <REPO_URL>
git push -u origin main
# GitHub > Settings > Pages > Branch: main / root 로 게시
```

또는 Vercel: 레포 임포트 → 프레임워크 None(Static) → 그대로 배포.

## 폰트

Google Fonts(Big Shoulders Display, Space Mono, Noto Sans KR) + Pretendard(jsdelivr CDN). 한글은 Pretendard, CDN 차단 시 Noto Sans KR 백업. **한글을 영문 전용 폰트에 태우지 말 것**(`CLAUDE.md` 규칙 참고).
