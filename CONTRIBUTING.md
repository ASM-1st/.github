# 협업 규칙

1ST 팀 GitHub 작업 규칙. **ASM-1st 조직의 모든 저장소**에 적용된다.
3인 · 6개월 규모에 맞춘 가볞은 **GitHub Flow**.

## 브랜치 모델 — GitHub Flow

- **`main`** — 항상 동작하는 안정 브랜치. 직접 push 금지, PR로만 머지된다.
- 모든 작업은 `main`에서 분기한 **짧은 수명의 작업 브랜치**에서. (별도 `develop` 브랜치 없음 — 이 규모에는 과함)
- 브랜치는 오래 끌지 않는다. 작게 쪼개 자주 머지.

## 기본 흐름: 이슈 → 브랜치 → PR → 머지

1. **이슈 먼저** — 할 일을 이슈로 등록. 라벨·담당자 지정.
2. **이슈별 브랜치** — 이슈 번호로 `main`에서 분기.
3. **작업 & 커밋** — 작은 단위로 자주 커밋. 커밋 메시지에 이슈 `#번호` 참조.
4. **PR** — 작업 끝나면 PR. 본문에 `Closes #번호`. 셀프 리뷰 먼저.
5. **리뷰 → 머지** — 팀원 1명 승인 후 **Squash merge**. 머지되면 브랜치 자동 삭제.

## 브랜치 네이밍

`<type>/<이슈번호>-<짧은-설명>`

| type | 용도 |
|------|------|
| `feat` | 기능 추가 |
| `fix` | 버그 수정 |
| `docs` | 문서 |
| `refactor` | 리팩터링 |
| `test` | 테스트 |
| `chore` | 설정·잡일 |

예: `feat/12-multi-persona-flow`, `fix/8-login-error`

## 커밋 메시지 — Conventional Commits

`<type>: <한 줄 요약>` 형태.

- `feat: 페르소나별 토론 턴 분기 추가`
- `fix: 빈 도서 입력 시 크래시 수정`
- `docs: README POC 목표 갱신`

type은 브랜치와 동일 집합(feat/fix/docs/refactor/test/chore).

## PR 규칙

- **작게.** 리뷰 가능한 크기로. 큰 작업은 이슈·PR을 쪼개다.
- 제목은 무엇을 했는지 한 줄. 본문에 `Closes #번호`로 이슈 연결.
- **팀원 1명 리뷰·승인** 후 머지. 본인 PR은 본인이 승인하지 않는다.
- 머지 방식은 **Squash merge** 통일 — main 히스토리를 깔끈하게.
- 리뷰 코멘트(대화)는 해결(resolve) 후 머지.

## 라벨

`feat` · `fix` · `docs` · `refactor` · `test` · `chore` · `question` · `blocked`
