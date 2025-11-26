# 프로젝트 구성 및 환경설정
<details>
<summary>접기/펼치기</summary>
<br>

## 프로젝트 clone degit
깃 리포지토리에서 파일만 복사해오는 도구인 degit 옵션을 사용한다.
- [indiecoder-svelte3-template.git](https://github.com/YooHyeok/indiecoder-svelte3-template.git)

### npx 방식
설치 없이 실행 가능한 npm CLI 이다. 아래 명령을 통해 degit 패키지를 즉시 실행하여 GitHub 레포지토리를 다운로드한다.
- `npx degit YooHyeok/indiecoder-svelte3-template#main ./`
  - `./`: 현재 경로를 프로젝트로 지정  
    (`-/`가 아닌 프로젝트명을 기입할경우 디렉토리가 생성되고, 하위로 설치된다.)

### npm 방식
degit을 로컬 또는 전역에 설치한 뒤 degit 명령을 통해 GitHub 레포지토리를 다운로드한다.
- `npm install -g degit`
- `degit YooHyeok/indiecoder-svelte3-template#main ./`
  - `./`: 현재 경로를 프로젝트로 지정  
    (`-/`가 아닌 프로젝트명을 기입할경우 디렉토리가 생성되고, 하위로 설치된다.)

### 설치 및 기동
- `npm install`
- `npm run dev`
</details>
<br>

# Svelte 기본 문법

<details>
<summary>접기/펼치기</summary>
<br>

## Svelte의 특징
svelte의 가장 큰 특징중 하나는 바로 write less code 이다.  
다른 프레임워크보다 적은 코드로 결과를 만들 수 있는 간결함이다.  

### 1. state 상태값
모든 프론트엔드 프레임워크의 구동방식은 비슷하다.  
자바스크립트로 state라고 하는 상태에 해당하는 어떤 변수를 두고  
해당 상태값의 상태에 따라 html과 css로 화면을 만들어간다.  
#### 코드 분석 
```html
<script>
let count = 0;

function handleClick() {
  // 이벤트 코드
  count += 1;
}
</script>
<button on:click={handleClick}>
  클릭수 { count }
</button>
```
`let count = 0;` 부분이 바로 상태를 나타내는 상태값인 state이다.  
상태값은 html 영역에서 `{ count }`와 같은 형태로 표현할 수 있다.  
또한 함수 `handleClick`은 상태값인 count에 1을 더하는 역할을 한다.  
handleClick함수는 마크업 영역에서 onClick 이벤트에 연동하여 실제 마우스 클릭 이벤트에 바인딩하여 
실제 마우스 클릭 이벤트를 감지하고 작동하게 된다.  
결국 변경된 상태값은 바로 적용되어 해당 상태값이 사용하는곳에 반영되게 된다.  


svelte 공식 사이트 > REPL 

별다른 설치 없이 스벨트 코드를 입력하고 바로 결과를 확인할 수 있다.  

#### 예제
```svelte
<script>
  let count = 0;
  function handleClick() {
    count += 1;
  }
</script>

<button on:click={handleClick}>
  클릭수 {count}
</button>
```


상태값의 경우 기본이 되는 변수는 물론 배열, 객체 그리고 객체의 배열 형태 등 자바스크립트에서 사용할 수 있는 대부분의 데이터 형태를 사용할 수 있다.  

```js
let count = 1; // 기본
let array = [1, 2, 3, 4, 5] // 배열
let objectState = { // 객체
  name: 'john',
  age: 20,
  location: 'seoul'
}
let objectArray = [ // 객체의 배열
  { 
    name: 'john',
    age: 20,
    location: 'seoul'
  },
  { 
    name: 'kim',
    age: 12,
    location: 'busan'
  },
  { 
    name: 'sun',
    age: 30,
    location: 'jeju'
  },
]
```

</details>
<br>


# Template
<details>
<summary>접기/펼치기</summary>
<br>

</details>
<br>