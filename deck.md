---
marp: true
theme: warp-apple
size: 16:9
paginate: false
lang: ko
title: "[무료 세미나] Claude Code Skills 뽀개기"
description: "검색 자동화부터 에이전트 팀 구축까지 — 클코대장 지피타쿠 직강"
author: 이철로 (지피타쿠)
---

<!-- _class: banner -->

<div class="tag">[ 무료 세미나 ]</div>

# Claude Code Skills 뽀개기 :<br/>검색 자동화부터 에이전트 팀 구축까지

<div class="by">By. <strong>지피타쿠</strong></div>

<!--
Speaker note (O1 · 00:00~01:00):
강의 때 이 배너 띄워놓고 이렇게 말씀해주세요 ↓

"안녕하십니까 지피타쿠입니다.
먼저 패스트캠퍼스 무료 세미나 'Claude Code Skills 뽀개기'에 참여해주셔서 감사합니다.

오늘은 Claude Code 이론을 길게 설명드리는 시간이라기보다,
Claude Code의 꽃이라고 불리는 Skills를 실제로 어떻게 쓰는지 같이 보는 시간이라고 생각해주시면 좋겠습니다.

흐름은 간단합니다.
먼저 제가 만들고 배포 중인 GPTaku Plugin이 어떤 플러그인인지 짧게 소개드리고,
그 안에 들어있는 스킬 두 가지를 실습으로 보여드리고,
마지막은 Q&A로 마무리하겠습니다.

오늘 끝나고 나면
클로드코드를 단순히 코딩할 때만 쓰는 게 아니라
이렇게도 쓸 수 있구나 하는 감은 가져가실 수 있을 거예요.

바로 시작하겠습니다."

(35~45초. 오프닝은 설명보다 기대감만 짧게 잡고 바로 넘기기.)
-->

---

<!-- _class: hero -->

<div class="profile-img">
  <img src="assets/threads-profile.png" alt="Threads @gptaku_ai — 2.9만 팔로워" />
</div>

<div class="bio">

# 클코대장<br/>**지피타쿠** — 이철로

- 현) **AX with** — AX 컨설팅 & AI 교육
- 현) **1인 개발자** — AI 기반 서비스
- 전) **R&D 기계 엔지니어 10년**<br/>GENTLE MONSTER · LG INNOTEK

<div class="bio-extra">

**CC101** (cc101.axwith.com)<br/>
가이드 제작·배포로 일반인·비개발 직무의 Claude Code 활용 지원

</div>

</div>

<!--
Speaker note (O2 · 01:00~02:00):
강의 때 이 슬라이드에서 이렇게 말씀해주세요 ↓

"먼저 제 소개를 간단히 드리자면
스레드에서 클코대장으로 활동하고 있는 지피타쿠, 이철로입니다.

저는 원래 10년 동안 기계 엔지니어로서 연구개발을 해왔어요.
스마트 아이웨어나 스마트폰 카메라 같은 쪽에서 일을 했습니다.

그러다가 AI를 접하고
이쪽으로 완전히 방향을 틀게 됐고,
지금은 Claude Code 기업 강의와 컨설팅을 하고 있습니다.

SNS에서는 Claude Code 입문하신 분들 대상으로
조금 더 쉽게 시작할 수 있게 돕는 콘텐츠나
CC101 같은 자료도 같이 배포하고 있어요."

(40~50초. 이력은 필요한 것만. '전문가라서가 아니라 겪어본 사람' 톤 유지.)
-->

---

<!-- _class: screenshot -->

<div class="screen">
  <div class="screen-bar">
    <span class="dot red"></span>
    <span class="dot yellow"></span>
    <span class="dot green"></span>
    <span class="screen-title">~ /  —  claude-code</span>
  </div>
  <div class="screen-body">
    <div class="line muted">Welcome to Claude Code</div>
    <div class="line muted">Type a message, or type / for commands.</div>
    <div class="line">&nbsp;</div>
    <div class="line muted">────────────────────────────────────────────────────────────</div>
    <div class="line">&nbsp;</div>
    <div class="line"><span class="prompt">&gt;</span> <span class="cursor"></span></div>
    <div class="line">&nbsp;</div>
    <div class="line muted">&nbsp;</div>
    <div class="line muted">? for shortcuts     ctrl+c to exit     shift+tab to switch mode</div>
  </div>
</div>

<div class="caption">— 처음 Claude Code 실행했을 때 딱 이 화면이에요.</div>

<!--
Speaker note (O3 · 02:00~02:45):
강의 때 이 화면 띄워놓고 이렇게 말씀해주세요 ↓

(2~3초 정적, 화면 먼저 보여주기)

"세미나를 진행하기에 앞서
많은 분들이 Claude Code에 대해 두려움을 갖고 계실 것 같아서
제 경험을 먼저 말씀드리려 합니다.

클로드코드를 처음 켜면
낯선 검은 창이 뜨잖아요.
저도 처음에는 이게 굉장히 무서웠습니다.
뭘 입력해야 될지도 모르겠고요.

강사가 이런 말 해도 되나 싶지만
저도 솔직히 말씀드리면
이 화면 처음 봤을 때 발작부터 했어요."

(35~45초. 공감 슬라이드. 너무 설명하지 말고 감정만 짚고 다음으로.)
-->

---

<!-- _class: beforeafter -->

<div class="before"><s>정석</s></div>

<div class="after">치트키</div>

<div class="caption">

평생 '정석' 말고 <strong>'치트키'</strong>만 찾던 사람이에요.<br/>
근데 <strong>AI 앞에선, 그 전략이 안 먹히더라고요.</strong>

</div>

<!--
Speaker note (O4 · 02:45~03:45):
강의 때 이 슬라이드에서 이렇게 풀어주세요 ↓

"제가 살아온 걸 되돌아보면
저는 항상 정공법으로만 가는 사람은 아니었던 것 같아요.
어떻게 하면 더 빠르게 핵심만 잡을 수 있을까,
어떻게 하면 바로 써먹을 수 있을까를 더 많이 봤던 것 같습니다.

제가 아는 분야에서는 그게 통했는데
아예 모르는 AI 분야에서는 그게 잘 안 되더라고요.

프롬프트 하나 잘 쓰는 걸로 끝나는 게 아니라
구조를 알아야 하고,
도구를 어떻게 묶어서 써야 하는지도 알아야 했어요."

(45~55초. '치트키'라는 단어를 내 성향 설명으로만 쓰고 길게 끌지 않기.)
-->

---

<!-- _class: wandering -->

<div class="logos">
  <div class="logo-pill"><img src="logos/replit-fav.png" alt="replit" /><span>replit</span></div>
  <div class="logo-pill"><img src="logos/lovable-fav.png" alt="lovable" /><span>lovable</span></div>
  <div class="logo-pill"><img src="logos/v0-fav.png" alt="v0" /><span>v0</span></div>
  <div class="logo-pill"><img src="logos/readdy-fav.png" alt="readdy" /><span>readdy</span></div>
  <div class="logo-pill"><img src="logos/cursor-fav.png" alt="cursor" /><span>cursor</span></div>
  <div class="logo-pill empty"><span>그 외 전부</span></div>
</div>

<div class="narration">

### 터미널은 **딴 세상**<br/>이거면 충분하다 싶었어요

</div>

<div class="footnote">저 <strong>평생 Windows만</strong> 쓰던 사람이라, 검은 창에 뭐 친다? 그게 아예 상상 밖이었거든요.</div>

<!--
Speaker note (O5 · 03:45~05:00):
강의 때 이 슬라이드 보면서 이렇게 풀어주세요 ↓

"AI로 작업하기 시작하면서 처음에는 정말 재밌었어요.
그런데 바이브코딩 단계로 넘어가려니까
이건 정말 접해보지 않은 영역이다 보니
내가 이걸 하는 게 맞나 싶더라고요.

그래서 찾은 게 이런 AI Builder들이에요.
Replit, Lovable, v0, Readdy 같은 툴들이요.

이게 틀렸다는 얘기는 아닙니다.
처음에는 오히려 진입장벽이 낮으니까요.
그런데 어느 순간부터는
내가 직접 제어할 수 있는 범위가 생각보다 좁다는 느낌이 왔어요.

그럼에도 Claude Code로는 못 넘어갔습니다.
이유는 단순했어요.
터미널이 너무 무서웠거든요."

(55~65초. Builder를 깎아내리지 말고 '왜 거기서 오래 머무는지'만 전달.)
-->

---

<!-- _class: peak -->

<div class="setup">커서로 끝까지 버티다가요.</div>

# 넘어오자마자<br/>후회했어요.

<div class="tail">이거 하나 안 쓰겠다고,<br/>몇 달을 <strong>그냥 날렸더라고요.</strong></div>

<!--
Speaker note (O6 · 05:00~06:15) ★ 감정 피크:
강의 때 이 슬라이드에선 속도를 확 낮춰주세요 ↓

"그런데 막상 Claude Code로 넘어오고 나니까
오히려 든 생각은 하나였어요.
왜 이걸 이렇게 늦게 시작했지.

Claude Code가 더 어려운 도구여서가 아니었습니다.
처음 10분이 낯설 뿐이지,
그 뒤에는 제가 원하는 걸 훨씬 더 정확하게 시킬 수 있었거든요.

그래서 제가 후회한 건
툴 하나를 안 쓴 게 아니라
제 작업 방식의 레버리지를 몇 달 늦춘 거였어요.

오늘 제가 이 얘기를 먼저 꺼내는 이유도
여러분이 저처럼 초반에 괜히 겁먹고 오래 미루지 않으셨으면 해서입니다."

(60~70초. 느리게. 문장 사이 쉬어주기.)
-->

---

<!-- _class: compare -->

<div class="cards-row">

<div class="col-a">

### 처음 입문

**혼자 찾기**

기능 하나씩<br/>
검색하면서 시작

</div>

<div class="arrow-between">→</div>

<div class="col-b">

### GPTaku Plugin

**바로 적용**

많이 쓰는 흐름부터<br/>
바로 시작

</div>

</div>

<div class="caption">

처음부터 다 알 필요 없습니다.<br/>
<strong>많이 쓰는 기능부터 붙이면 됩니다.</strong>

</div>

<!--
Speaker note (O7 · 06:15~07:30):
강의 때 이 슬라이드에서는 회복 톤으로 이렇게 말씀해주세요 ↓

"그렇다고 처음부터 Claude Code의 기능을 전부 다 알 필요는 없습니다.

오히려 처음 입문할 때는
하나씩 검색하면서 혼자 익히는 방식보다
많이 쓰는 기능부터 바로 붙여보는 게 훨씬 중요하다고 생각해요.

그래서 만든 게 GPTaku Plugin입니다.
이건 거창하게 새로운 걸 더 얹는 플러그인이라기보다,
입문자가 자주 막히는 구간과 자주 쓰는 흐름부터
바로 적용할 수 있게 묶어둔 쪽에 가깝습니다.

오늘은 그 감을 좀 빠르게 잡아가시면 됩니다."

(50~60초. 회복 구간. '혼자 찾기'보다 '바로 적용'으로 관점 전환.)
-->

---

<!-- _class: roadmap -->

# <span class="em-box">오늘 세미나는 이렇게 갑니다</span>

<div class="track">
  <div class="step">
    <div class="idx">SESSION 1</div>
    <div class="title">GPTaku Plugin</div>
    <div class="desc">플러그인 소개</div>
    <div class="time">10 min</div>
  </div>
  <div class="step">
    <div class="idx">SESSION 2</div>
    <div class="title">insane-search</div>
    <div class="desc">검색 자동화 실습</div>
    <div class="time">15 min</div>
  </div>
  <div class="step">
    <div class="idx">SESSION 3</div>
    <div class="title">kkirikkiri</div>
    <div class="desc">에이전트 팀 실습</div>
    <div class="time">15 min</div>
  </div>
</div>

<div class="bridge">소개 하나, 실습 둘, 그리고 Q&amp;A →</div>

<!--
Speaker note (O8 · 07:30~10:00):
강의 때 이 슬라이드에서 오늘 흐름을 명확하게 정리해주세요 ↓

"오늘 흐름은 아주 단순합니다.
먼저 GPTaku Plugin이 어떤 플러그인인지 소개드리고,
그다음 그 안에 들어있는 스킬 두 가지를 실습으로 보여드리겠습니다.

하나는 `insane-search`입니다.
검색 자동화를 할 때 막히는 웹사이트를 어떻게 다루는지 보실 거고요.

다른 하나는 `kkirikkiri`입니다.
자연어 한 줄로 에이전트 팀을 붙이는 과정을 같이 보실 겁니다.

그리고 마지막은 Q&A로 마무리할게요.
오늘은 기능 설명을 많이 듣는 시간보다
바로 적용되는 흐름을 보는 시간이라고 생각하시면 됩니다."

(1분 안팎. 소개 1개, 실습 2개, Q&A 구조를 선명하게 고정.)
-->

---

<!-- _class: title -->

# Session 1<br/>**GPTaku Plugin 소개**

## 클코대장의 치트키 상자, 지금 열어드려요

<!--
Speaker note (S1-1 · 20:10~20:10:30):
강의 때 이렇게 짧게 브릿지해주세요 ↓

"이제부터는 스토리보다 도구 얘기를 해보겠습니다.
방금까지는 왜 초반에 많이 막히는지를 말씀드렸다면,
지금부터는 그 첫 진입을 어떻게 쉽게 만드는지 보여드릴게요.

그 역할을 하는 게 GPTaku Plugin입니다."

(20~30초. 자연스럽게 Session 1로 진입.)
-->

---

<h1 class="wall-title">Claude Code 쓸 때, <span class="em-soft">부딪히는 벽</span></h1>

<div class="wall-grid">
  <div class="wall">
    <div class="icon">🚧</div>
    <div class="word">세팅</div>
    <div class="quote">"뭐부터<br/>쳐야 하지?"</div>
  </div>
  <div class="wall">
    <div class="icon">🚧</div>
    <div class="word">용어</div>
    <div class="quote">"에이전트? MCP?<br/>훅? 서브에이전트?"</div>
  </div>
  <div class="wall">
    <div class="icon">🚧</div>
    <div class="word">레시피</div>
    <div class="quote">"만들고 싶은 건 있는데,<br/>어떻게 만들지 모르겠어."</div>
  </div>
</div>

<div class="footer-note">저도 이 순서대로, 다 겪었어요.</div>

<!--
Speaker note (S1-2 · 20:10:30~20:12):
강의 때 슬라이드 보면서 이렇게 풀어주세요 ↓

"Claude Code 처음 쓰시는 분들 보면
거의 비슷한 순서로 막힙니다.

첫 번째는 세팅입니다.
설치는 했는데 그 다음에 뭘 해야 할지 모르겠는 거예요.
텅 빈 터미널 앞에서 바로 멈추죠.

두 번째는 용어입니다.
에이전트, MCP, 스킬, 훅, 서브에이전트.
하나하나 다 중요한 것 같긴 한데
처음에는 뭐가 뭔지 감이 잘 안 옵니다.

세 번째는 레시피입니다.
기능이 있다는 건 알겠는데
언제 뭘 꺼내 써야 할지가 안 보여요.

저도 이거 다 겪었습니다.
그리고 오늘 Plugin을 소개하는 이유도
이 세 벽을 한 번에 낮춰주기 때문입니다."

(1분 안팎. 벽 3개를 선명하게 찍고 바로 해결책으로 연결.)
-->

---

<!-- _class: peak -->

<div class="setup">GPTaku Plugin</div>

# 방금 본 벽 3개,<br/><strong>플러그인이 뚫어드려요.</strong>

<div class="tail">설치 한 줄 →<br/>입문자 벽 바로 건너뜁니다.</div>

<!--
Speaker note (S1-3 · 20:12~20:14):
강의 때 이 피크 보여주고 이렇게 풀어주세요 ↓

"Plugin이라고 하면
뭔가 엄청 복잡하고 대단한 걸 생각하실 수도 있는데
GPTaku Plugin은 그런 느낌은 아닙니다.

Claude Code를 대신 써주는 마법이라기보다,
입문자가 자주 막히는 부분을
미리 정리해둔 시작 패키지에 더 가깝습니다.

기본 세팅,
자주 쓰는 스킬,
그리고 언제 어떤 흐름을 타면 되는지에 대한 레시피가
한 묶음으로 들어 있다고 보시면 됩니다.

그래서 혼자 몇 달 걸려 익힐 시행착오를
설치 한 번으로 훨씬 빠르게 건너뛸 수 있는 거예요."

(1분 안팎. 핵심은 '대단한 기능'보다 '시작 패키지'라는 정의.)
-->

---

<!-- _class: radial -->

<div class="hub-label">GPTaku Plugin</div>

<div class="satellites">
  <div class="sat today">
    <div class="name">insane-search</div>
    <div class="desc">차단된 사이트도 자동 우회</div>
  </div>
  <div class="sat today">
    <div class="name">kkirikkiri</div>
    <div class="desc">자연어 한 마디로 AI 팀</div>
  </div>
  <div class="sat">
    <div class="name">deep-research</div>
    <div class="desc">멀티 에이전트 딥리서치</div>
  </div>
  <div class="sat">
    <div class="name">skillers-suda</div>
    <div class="desc">스킬 만드는 스킬</div>
  </div>
  <div class="sat">
    <div class="name">vibe-sunsang</div>
    <div class="desc">내 AI 활용 점검</div>
  </div>
  <div class="sat">
    <div class="name">git-teacher</div>
    <div class="desc">Git 자동화</div>
  </div>
  <div class="sat">
    <div class="name">insane-design</div>
    <div class="desc">디자인 시스템 분석·적용</div>
  </div>
  <div class="sat">
    <div class="name">show-me-the-prd</div>
    <div class="desc">한 문장 → PRD</div>
  </div>
  <div class="sat">
    <div class="name">pumasi</div>
    <div class="desc">Codex 병렬 외주 개발</div>
  </div>
  <div class="sat">
    <div class="name">nopal</div>
    <div class="desc">Google Workspace 오케스트레이션</div>
  </div>
  <div class="sat">
    <div class="name">docs-guide</div>
    <div class="desc">공식 문서 자동 탐색</div>
  </div>
  <div class="sat empty">
    <div class="name">+ 계속 추가 중</div>
  </div>
</div>

<div class="bridge-note">★ 표시 두 개, 오늘 세미나에서 같이 써봅니다 →</div>

<!--
Speaker note (S1-4 · 20:14~20:18):
강의 때 이 허브 보여주면서 이렇게 말씀해주세요 ↓

"여기 들어 있는 스킬은 계속 늘어나고 있지만,
오늘 이 자리에서 다 설명하진 않겠습니다.

오늘 중요한 건 두 개예요.
`insane-search`,
그리고 `kkirikkiri`.

`insane-search`는 막히는 웹을 자동으로 우회하면서 데이터를 가져오는 스킬이고,
`kkirikkiri`는 자연어 한 줄로 팀 구성을 시작하게 해주는 스킬입니다.

조금 뒤에 바로 이 두 개를 실습으로 보실 거예요.
그래서 오늘은 플러그인 전체 소개보다
왜 하필 이 두 개를 먼저 보여드리는지에만 집중하시면 됩니다.

이제 설명은 여기까지 하고,
첫 번째 실습으로 넘어가보겠습니다."

(1분 안팎. 두 스킬이 오늘 실습의 주인공이라는 점만 선명하게.)
-->

---

<!-- _class: grid -->

# 오늘 1시간, <span class="em-soft">우리가 한 것</span>

<div class="cards">
  <div class="card">
    <div class="num">①</div>
    <div class="title">GPTaku Plugin</div>
    <div class="desc">플러그인 소개</div>
  </div>
  <div class="card">
    <div class="num">②</div>
    <div class="title">insane-search</div>
    <div class="desc">검색 자동화 실습</div>
  </div>
  <div class="card">
    <div class="num">③</div>
    <div class="title">kkirikkiri</div>
    <div class="desc">에이전트 팀 실습</div>
  </div>
</div>

<div class="caption">소개 하나, 실습 둘. <span class="em-box">오늘은 여기까지.</span></div>

<!--
Speaker note (C1 · 21:00~21:01):
강의 때 차분하게 이렇게 정리해주세요 ↓

"정리하면 오늘은 세 가지였습니다.
GPTaku Plugin이 어떤 플러그인인지 먼저 봤고,
그 안에서 검색 자동화와 에이전트 팀이라는
대표적인 두 가지 활용을 같이 보셨습니다.

오늘 제가 드리고 싶었던 건
Claude Code를 기능별로 다 외우라는 얘기가 아닙니다.
이런 식으로 붙이면 되는구나,
이 감을 잡으셨으면 저는 충분합니다."

(40~50초. 요약은 짧고, 오늘 전달하려던 메시지를 다시 한 번 묶기.)
-->

---

<!-- _class: peak -->

<div class="setup">제가 진심으로 드리고 싶은 말.</div>

# Claude Code,<br/>꼭 한 번 써보세요.

<div class="tail">&nbsp;</div>

<!--
Speaker note (C2 · 21:01~21:03) ★ 클로징 피크:
화면 띄워놓고 이렇게 풀어주세요 (정적 한 번 깊게 → 천천히) ↓

"제가 마지막으로 꼭 드리고 싶은 말은 이것뿐입니다.

Claude Code, 꼭 한 번 직접 써보세요.

설명을 들을 때와
내가 한 번 실행해보는 건 완전히 다릅니다.

첫 화면이 낯설어도
딱 두세 번만 넘어가면
아 왜 다들 Claude Code 얘기하는지 알겠다 하는 지점이 옵니다.

오늘 보신 가능성이
거기까지 이어졌으면 좋겠습니다."

(1분 안팎. 정직하고 담백하게. 과하게 팔지 않기.)
-->

---

<!-- _class: offer -->

# 더 깊게 가고 싶으시면<br/><span class="em-soft">본강의에 다 있어요.</span>

<div class="parts">
  <div class="part">
    <div class="part-num">PART 04</div>
    <div class="part-title">GPTaku Plugin 체험</div>
    <div class="part-desc">설치 + 주요 스킬 4개 직접 써보기</div>
  </div>
  <div class="part">
    <div class="part-num">PART 06 ★</div>
    <div class="part-title">스킬 만들기 9개</div>
    <div class="part-desc">딥리서치·검색API·웹크롤·모닝브리핑·콘텐츠파이프라인…</div>
  </div>
  <div class="part">
    <div class="part-num">PART 07</div>
    <div class="part-title">나만의 AI Agent</div>
    <div class="part-desc">오픈클로 워크스페이스 + 콘텐츠 자동화 + 트렌드앱</div>
  </div>
</div>

<div class="benefits">
  <div class="line">🔥 당일 라이브 접속자 한정 · <strong>3만원 특별 할인</strong></div>
</div>

<!--
Speaker note (C3 · 21:03~21:04:30):
강의 때 이렇게 연결해주세요 ↓

"그리고 더 깊게 가고 싶으신 분들을 위해
본강의에서는 오늘 보여드린 것들을 훨씬 더 자세히 다룹니다.

GPTaku Plugin을 직접 설치하고 써보는 구간도 있고,
스킬을 여러 개 직접 만들어보는 파트도 있고,
나만의 AI Agent 구조를 만드는 부분도 있습니다.

오늘 세미나가 감을 잡는 시간이었다면
본강의는 그걸 내 일에 붙이는 단계라고 생각하시면 됩니다.

오늘 라이브 참석자 혜택도 준비돼 있으니
관심 있으신 분들은 끝나고 꼭 확인해보시면 좋겠습니다."

(1분 안팎. 혜택과 본강의 연결은 자연스럽게, 그러나 분명하게.)
-->

---

<!-- _class: thanks -->

<div class="msg">

# 감사합니다.

<div class="sub">궁금한 거 있으면 언제든 스레드로.</div>

</div>

<div class="foot">
  <div class="qr-block">
    <div class="qr"><img src="assets/qr-threads.png" alt="Threads QR"/></div>
    <div class="qr-label">📱 스캔 → 스레드</div>
  </div>
  <div class="handles">
    <span class="em-box">@gptaku_ai</span> <span class="label">Threads</span><br/>
    <span class="em-box">@GPTaku</span> <span class="label">X</span>
  </div>
  <div class="signoff">
    스레드 클코대장 지피타쿠<br/>
    — 앞으로도 잘 부탁해
  </div>
</div>

<!--
Speaker note (C4 · 21:04:30~21:05):
강의 종료 멘트로 이렇게 마무리해주세요 ↓

"늦은 시간까지 함께해주셔서 정말 감사합니다.

질문이 더 생기시면
스레드나 X에서 지피타쿠로 찾아오셔도 되고,
오늘 자료에서 보신 이름 그대로 오시면 됩니다.

저는 앞으로도 Claude Code를 더 쉽게 쓰는 방법을 계속 공유할 예정이니까
연결만 되어 있어도 도움이 되실 거예요.

감사합니다."

(25~30초. 가볍고 따뜻하게 끝내기.)
-->
