# CLAUDE.md

> 제1원칙: 본인이 설명할 수 없는 코드는 커밋하지 않는다. AI가 쓴 코드도 머지하면 내 코드다.

## 코드

- 타입 침묵 금지: `any` / `as` / `!`(non-null) / `@ts-ignore` / `eslint-disable` 쓰지 말 것. 타입으로 설명하라.
- 파생 가능한 값은 계산한다. `useState` + `useEffect`로 동기화하지 말 것.
- 기존 유틸·컴포넌트를 재사용한다. 비슷한 것을 새로 만들지 말 것.
- 에러는 명시적으로 처리한다. 빈 `catch {}` 금지.
- hook은 모든 호출을 마친 뒤 early return (조건부·early return 뒤 hook 금지).

## 커밋

- `--no-verify` 금지. lint/format 게이트를 통과한 뒤에만 커밋한다.

## 환경

- 패키지 매니저: **pnpm** (npm/yarn 쓰지 말 것).
- Lint: ESLint flat config — typescript-eslint `strict-type-checked` + `react-hooks` (핵심 규칙 `error`).
- Format: **Prettier 전담** (`semi: false`, `singleQuote`). ESLint에 포맷 룰을 넣지 말 것.
