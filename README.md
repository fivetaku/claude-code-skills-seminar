# Claude Code Skills 뽀개기 — 세미나 슬라이드

**2026년 4월 22일 (수) 20:00 Zoom LIVE 세미나** 슬라이드 덱입니다.

- **연사**: 클코대장 [지피타쿠](https://www.threads.com/@gptaku_ai) (이철로)
- **주최**: 패스트캠퍼스 무료 세미나
- **주제**: Claude Code Skills 뽀개기 — 검색 자동화부터 에이전트 팀 구축까지

## 🎬 슬라이드 보기

브라우저에서 [index.html](./index.html) 열기 → `F` 키로 전체화면 → 방향키로 슬라이드 이동.

(GitHub Pages 배포 URL은 Settings → Pages에서 활성화 후 제공됩니다.)

## 📦 파일 구성

| 파일 | 용도 |
|---|---|
| `index.html` | 브라우저 발표용 (Marp 생성 HTML) |
| `deck-editable.pptx` | PowerPoint/Keynote/Google Slides 편집용 |
| `deck.md` | Marp 소스 (편집 시 이거 수정 후 재빌드) |
| `theme.css` | Warp + Apple 하이브리드 커스텀 테마 |
| `assets/` | Threads 프로필, Threads QR 이미지 |
| `logos/` | AI Builder 브랜드 로고 (replit/lovable/v0/readdy/cursor) |

## 🔄 재빌드 방법

```bash
# HTML 재생성
npx --yes @marp-team/marp-cli@latest deck.md --theme theme.css --allow-local-files --html -o index.html

# 편집 PPTX 재생성
npx --yes @marp-team/marp-cli@latest deck.md --theme theme.css --allow-local-files --pptx-editable -o deck-editable.pptx
```

## 🎨 디자인 레퍼런스

- **Warp** 마케팅 사이트 — 크림 아이보리 베이스, Inter 폰트
- **Apple** 공식 사이트 — Peak 슬라이드의 큰 타이포, 타이트 letter-spacing
- **Claude 오렌지** `#D97757` — 유일한 포인트 컬러

## 📱 함께 봐주세요

- Threads: [@gptaku_ai](https://www.threads.com/@gptaku_ai) — 스레드 클코대장 지피타쿠
- X: [@GPTaku](https://x.com/GPTaku)
- cc101: [cc101.axwith.com](https://cc101.axwith.com/ko) — 한국어 Claude Code 가이드
- 본강의: [클로드코드 뽀개기 (패스트캠퍼스)](https://fastcampus.co.kr/biz_online_claudecode)

---

MIT License. Slides may be reused with attribution.
