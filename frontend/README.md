# XQUARE Frontend 커밋 규칙

```markdown
CommitType(PackageName): Subject
```

위는 모든 커밋메세지의 형식이다.

### Commit Type

위에 CommitType; 이라고 기재한 부분:
|CommitType|설명|
|------|----------------------|
|feat|새로운 기능 추가|
|fix|버그 수정|
|refactor|코드 리펙토링|
|docs|문서 작성 및 수정|
|chore|프로젝트 세팅|
|style|코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우정|

### PackageName

위에 PackageName 라고 기재한 부분:

- 패키지가 아닐시 생략이 가능
- workspace 패키지 이름을 의미함

### Subject

위에 Subject 라고 기재한 부분:

- 50자를 넘기지 않게 명령형으로 작성한다.
- 한국어로 작성한다.

### Example

```bash
fix(react-theming): Provider가 제대로 적용되지 않는 오류 수정
```

```bash
chore: publish workflow 작성
```

```bash
chore(ui): use-dark-mode 의존성 추가
```
