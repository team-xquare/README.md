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
>
> 생성한 issuedhk 성격이 맞는 label을 선택하여 추가한다.

``` [Domain] Subject

	Subject

```

위는 모든 이슈 메세지의 형식이다.

### Labels

>  새 리포지토리를 생성하면 issue label을 위같이 설정한다.

| Label         | Description                                | Color Code | 의미                                                         |
| ------------- | ------------------------------------------ | ---------- | ------------------------------------------------------------ |
| 버그          | Something isn't working                    | #d73a4a    | 예기치 않은 문제 또는 의도하지 않은 동작(버그)을 나타냅니다. |
| 기능 추가     | New feature or request                     | #a2eeef    | 새로운 기능 요청을 나타냅니다.                               |
| DOCS          | Improvements or additions to documentation | #cfd3d7    | 문서를 개선하거나 추가 할 필요가 있음을 나타냅니다.          |
| Chore         |                                            | #0075ca    | 자잘한 수정들을 나타냅니다.                                  |
| 리펙토링      | Refactoring is needed                      | #008672    | 리펙토링이 필요함을 나타냅니다.                              |
| 프로젝트 설정 | Project setting is needed                  | #555303    | 프로젝트 설정이 필요함을 나타냅니다.                         |
| 테스트 추가   | Request a new test                         | #CD7F57    | 새로운 테스트 요청을 나타냅니다.                             |



## 커밋 규칙

### 커밋메세지

> 다음은 커밋메세지의 형식입니다.
``` 

  CommitType :: (#issue number) Subject
  
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

![버전 규칙](https://user-images.githubusercontent.com/67373938/119933978-0ac15300-bfc0-11eb-99cd-0198b1ee6f2d.png)

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
