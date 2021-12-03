# :pushpin: (리액트) 크리스마스 영화 추천
>리액트로 만든 크리스마스 영화 추천 페이지입니다

>https://irrpl-ar.github.io/React_Christmas-movies

</br>

## 1. 제작 기간 & 참여 인원
- 2021년 11월 23일 ~ 11월 24일
- 개인 프로젝트

</br>

## 2. 사용 기술
#### `Front-end`
  - React JS
  - Jsx
  - CSS

</br>

## 3. 핵심 기능

<details>
<summary><b>핵심 기능 설명 펼치기</b></summary>
<div markdown="1">

### SPA
- 싱글 페이지 어플리케이션을 구현하였습니다   
- 각 영화 포스터 또는 제목을 누르면 소개 페이지가 열리도록 구현하였습니다

### 나의 평점 매기기
- useState로 각 영화에 대한 나의 평점을 간단히 매길 수 있도록 구현하였습니다

</div>
</details>

</br>

## 4. 디버깅
### 4-1. 핵심 디버깅

```
Element type is invalid: expected a string (for built-in components) or a class/function (for composite components)   
but got: undefined. You likely forgot to export your component from the file it's defined in,   
or you might have mixed up default and named imports.   

Check the render method of App.
```

* 리액트 공부를 시작한지 일주일정도밖에 안되어서, 대략 기능은 익혔지만 아직 모르는 부분이 많았음
* 특히 이 프로젝트 전에 간단히 하나를 만들어봤을 때도 위와 같은 에러 메세지가 계속 뜸
* vscode로 작업 전에 code sandbox를 통해 작업하며 문제점을 파악해보기로함   
처음에는 이상 없이 잘 되다가, Router를 사용할 때 다시 위와 같은 메세지가 뜸
* 구글링을 통해 Router 적용방법, import export 체크, 함수 및 변수명 체크를 다 해봤으나 해결 못함
* 알고 보니 React-router-dom 버전에 문제가 있을 수 있다는 것을 알게됨. 5.1.2 버전으로 다운그레이드   
하니 바로 해결되며 화면이 뜸. 버전 6에 문제가 좀 있을 수 있다고 함   
(Routes로 감싸도 해결이 안되었음)

</br>


### 4-2. 각종 디버깅
<details>
<summary>useState</summary>
<div markdown="1">

```
  return(
  <div>
    <h2>나의 평점은?</h2>
    <h2>{num}</h2>
    <div className="btn">
        <button onClick={onUp} className="up">Up!</button>
        <button onClick={onDown}>Down!</button>
    </div>
  </div>
```

* useState 사용 전 임시로 h2에 0을 두고, useState 사용 후에도 고치지않아서   
setNum이 제대로 작동하지 않음
* h2에 0 대신 {num} 으로 바꾸니 제대로 작동함

</div>
</details>

</br>

## 5. 회고 / 느낀점
> 리액트를 배우고 처음으로 개인 프로젝트를 만들어서 뿌듯하다   
사실 정말 별거 아닌 기능이지만, Router문제도 해결하고 useState도 써보니 좋았다   
버전 문제로 인한 오류 해결에 시간을 많이 허비한게 아쉽지만, 그 과정 중에  
공식 문서나 구글링으로 공부가 된 것 같다


