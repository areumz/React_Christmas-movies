# :pushpin: (리액트) 크리스마스 영화 추천
>리액트로 만든 크리스마스 영화 추천 페이지

>https://irrpl-ar.github.io/React_Christmas-movies/

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
- 싱글 페이지 어플리케이션 구현을 위해 Router를 사용하였습니다
- 각 영화 포스터 또는 제목을 클릭하면 해당 페이지로 연결되도록 하였습니다

### 나의 평점 매기기
- useState를 사용하여 간단히 영화에 대한 개인적인 평점을 매겨볼 수 있도록 했습니다

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

* 리액트를 배운지 일주일정도라 대략 기능은 익혔지만, 아직 상세히 모르는게 많았음
* 특히나 HTML/CSS와 Javascript에 비해서 오류가 정확히 어디서 났는지 파악하기가 더 어려웠음
* 이것 전에 간단한 프로젝트를 만들려 할 때도 계속 위와 같은 오류가 났었고, 본격 작업 전에 code sandbox로   
먼저 작업해보기로함. 이번에도 역시 그런 오류가 났는데, 처음엔 잘 뜨다가 Router를 사용하는 순간 다시   
저 오류 메세지가 뜸
* 구글링을 통해 import, export 체크, function 및 변수명 체크 등 등 다양하게 시도해봤지만 계속 해결이 안됨
* 알고보니 React-router-dom의 버전에서 문제가 생길 수도 있다는 글을 발견하여 버전을 5.1.2 로 다운그레이드하니   
바로 화면이 뜨고 Router도 잘 작동함. 버전 6가 문제가 더러 있다고 함

</br>


### 4-2. 각종 디버깅
<details>
<summary>useState 사용시 문제</summary>
<div markdown="1">
- 맨 처음에 return 부분에 평점을 임의로 0으로 두고, useState를 사용했더니 작동 안함
- 초기값 0을 줬으니 0 대신 {num} 을 넣자 숫자가 변하며 작동함

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

</div>
</details>

</br>

## 5. 회고 / 느낀점
> 리액트를 배우기 시작하면서 처음으로 만들고, 작지만 오류도 해결해서 왠지 모르게 뿌듯하다   
버전 문제로 해결이 되서 허탈하기도했지만 해결을 위해서 공식 문서도 보고 구글링도 하면서   
리액트에 대해 좀 더 공부한 것 같다

