# XQUARE 프로젝트를 시작하기전

## 목차

* [개발 프로세스](https://github.com/TEAM-XQUARE/README.md#개발-프로세스)
* [이슈규칙](https://github.com/TEAM-XQUARE/README.md#이슈-규칙)
* [커밋규칙](https://github.com/TEAM-XQUARE/README.md#커밋-규칙)
* [브랜치규칙](https://github.com/TEAM-XQUARE/README.md#브랜치-규칙)
* [버전규칙](https://github.com/TEAM-XQUARE/README.md#버전-규칙)



## 개발 프로세스

> 1. issue 생성
> 2. issue 기반 branch 생성
> 3. issue와 관련된 feature 개발 완료
> 4. PR 혹은 merge commit 생성시에도 커밋 메세지 규칙에 맞춰 작성
> 5. PR이 주요 branch로 merge되기 위한 조건
>    - 최소 1명의 review의 approve
>    - CI로 인한 build success
>    - test case 작성 - optional
> 6. merge 후 feature branch 제거
> 7. issue close



## 이슈 규칙

> 한 기능 당 하나의 issue 생성을 원칙으로 합니다.

### 이슈메시지

>  다음은 이슈메시지의 형식입니다.

* ```[   ]``` 안에 작성한다.
* 작업한 부분의 도메인을 기입한다.

``` [Domain] Subject

	[Domain] Subject

```

### Labels

>  새 리포지토리를 생성하면 issue label을 위같이 설정한다.

| Label     | Description                                | Color Code | 의미                                                         |
| --------- | ------------------------------------------ | ---------- | ------------------------------------------------------------ |
| 버그      | Something isn't working                    | #d73a4a    | 예기치 않은 문제 또는 의도하지 않은 동작(버그)을 나타냅니다. |
| 기능 추가 | New feature or request                     | #a2eeef    | 새로운 기능 요청을 나타냅니다.                               |
| DOCS      | Improvements or additions to documentation | #cfd3d7    | 문서를 개선하거나 추가 할 필요가 있음을 나타냅니다.          |
| UI 작업   |                                            | #0075ca    | UI작업이 필요함을 나타냅니다.                                |
| 리펙토링  | Refactoring is needed                      | #008672    | 리펙토링이 필요함을 나타냅니다.                              |



## 커밋 규칙

### 커밋메세지

> 다음은 커밋메세지의 형식입니다.
``` 

  CommitType :: (#issue number)[Domain] Subject
  
```

### Commit Type

 > 다음은 커밋타입 형식입니다.

|CommitType|설명|
|------|----------------------|
|📑 ::|파일 생성 및 구조 변경|
|⚡️ ::|기능 업데이트|
|⚰️ ::|기능 삭제|
|🐛 ::|버그 수정|
|♻️ ::|코드 리펙토링|
|📝 ::|문서 작성 및 수정|
|⚙️ ::|프로젝트 세팅|
|🧪 ::|테스트 코드 추가|
|🚀 ::|새 버전 릴리즈 ( 커밋은 아니지만😏|
|🔀 ::|Merge or PR|

### Domain

> 커밋메세지 형식의 Domain 부분에 기재

* ```[   ]``` 안에 작성한다.
* 작업한 부분의 도메인을 기입한다
* 도메인과 관련이 없거나 굳이 작성할 필요가 없을땐 작성 하지 않아도 된다.

```bash

[MainPage]

```

### issue number

위에 #issue number 이라고 기재한 부분:

- merge commit이나 PR을 날릴때에만 사용한다.
- `(  )` 안에 작성한다.
- `#`뒤에 개발한 브런치가 기반을둔 issue number을 기입한다.

```
(#12)
```

### Subject

> 커밋메세지 형식의 Subject 부분에 기재

* 50자를 넘기지 않게 명령형으로 작성한다.
* 한국어로 작성한다.
* ```어떻게``` 보단 ```무엇을```, ```왜``` 에 초점을 두고 작성한다.

```bash

"~수정 했다" → "~수정"

"Add~" → "~추가"

```

### Example

```
🐛 :: [MainPage] 헤더가 안보이는 버그 수정
```
```
🐛 :: (#19)[FeedServiceImpl] 피드 버그 로직 수정
```
```
🚀 :: v1.0.0
```
```
📝 :: README 파일 수정
```



### 브랜치 규칙

> 기본적으로 GitFlow를 따릅니다

### Feature Branch

```markdown

Feature/{issue number}_{todo}

```



### 버전 규칙

![소프트웨어 버전 규칙 - Semantic Versioning : 네이버 블로그](https://lh3.googleusercontent.com/proxy/X4MxQui0Qxx-1CPcLNUDuGgmiEEShXlyIArFG6rEuI8lR_0FQoVbHYpPsWG8PlsWO6tluZIj3VO-er9p7yH9g_HbMvotXV46pSaSBO8mzK5SydyRM0myr_4mX57xX0oT9d-wjjY7r9Cq1dGUl4TBXv5a13y96sPt-S09LR4jx1ll1XL8_3ZzenyGceM_RZq7yUn3_rvDrTvcg8xm3eNFkkdHA8onLYrL1KQ8OHUW_ruNO0rc4-brttRsxlIFAGGXSB-aEKpda518lKQIkxw8DAcIjOh8TXFjwAze)

>  모든 버전은 01.00.00에서 시작한다.

```jsx

"01.01.09" 생략시 "1.1.9"

"01.01.10" 생략시 "1.1.10"

```

### Major Version

- 1로 시작한다.
- 증가 시 나머지 버전 정보 초기화
- 전체를 뒤엎었을때 변화한다.

### Minor Version

- 00으로 시작한다 
- 없던 기능의 추가나 기존 기능의 수정 등의 변화가 발생했을때 이 수치를 올린다.

### Patches

+ 00으로 시작한다.

- 자잘한 버그나 내부적 코드 보완 등의 변화가 발생했을때 이 수치를 올린다.