# Public Advanced(중급반)
중급반 학생을 위한 프로젝트 폴더


## HTML5 Boiler Plate
- HTML5 보일러플레이트
  - HTML5 의 새로운 요소 사용에 도움
  - 안정적인 하위호환성 제공
  - Polyfill(폴리필)
  - 점진적인 기능 향상을 염두(새로운 코드에 대한 최적화된 구조)
  - 최적화 버전 유지

### Polyfill
(shim, fallback)
웹브라우저에서 설치되어 있지 않은(동작하지 못하는) 기능을 제공하는 행위나 기술

Modernizr 에서 제공하는 [폴리필 목록](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills)

- Polyfill 예시
  - html5shiv: HTML5 의 Sectioning Elements(<header>, <footer>, <section> 등) 를 지원하지 않는 브라우저를 위한 라이브러리
  - respond: CSS `@media` 를 IE6 ~ IE8 버전에서 사용 가능하게 만들어주는 라이브러리
  - selectivizr: CSS `border-radius` 와 `box-shadow`, `liner-gradient`를 IE6 ~ IE9 버전에서 지원하기 위한 라이브러리


### 인코딩 방식 설정
문자가 인코딩되는 방식을 설정

```html
<meta charset="UTF-8"/>
```

`UTF-8`
:  초성, 중성, 종성으로 구분하여 문자를 작성(권장)

`EUC-KR`
:  하나의 완성된 글자를 인식

### 웹페이지 설명
웹페이지에 대한 설명을 입력

```html
<meta name="description" content="페이지 설명"/>
```

`name`
:  메타 데이터의 이름(종류)를 지정하는 속성

`content`
:  `name`, `http-equiv` 속성의 값을 입력하는 속성

### IE 렌더링 방식 설정
Internet Explorer 브라우저에서 렌더링(Rendering)되는 방식을 설정

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge"/>
```

`http-equiv` (equivalent)
:  HTML 문서를 읽기 전에 브라우저에게 전달한 정보의 종류를 입력하는 속성

`content`
:  `name`, `http-equiv` 속성의 값을 입력하는 속성
- `IE=5`
- `IE=7`
- `IE=EmulateIE7`
- `IE=8`
- `IE=EmulateIE8`
- `IE=edge` (권장, IE8 이상 버전에서 항상 최신 표준 모드로 렌더링)
> 마이크로소프트는 실험적인 프로젝트가 아니면 `IE=edge` 모드를 권장함.

## JavaScript Libraries(Plugins)

### ie9
<https://code.google.com/archive/p/ie7-js/>
- IE5.5 ~ IE8 (IE: Microsoft Internet Explorer) 버전을 IE9 버전처럼 표현(style)할 수 있는 JavaScript Library.
- 조건부 주석(Conditional Comments)과 함께 사용

```html
<!--[if lt ie 9]>
<script src="js/lib/ie9.js"></script>
<![endif]-->
```

### Respond
<https://github.com/scottjehl/Respond>
- CSS @media 를 IE6 ~ IE8 버전에서 사용 가능하게 만들어주는 JavaScript Library.
- 조건부 주석(Conditional Comments)과 함께 사용

```html
<!--[if lt ie 9]>
<script src="js/lib/respond.min.js"></script>
<![endif]-->
```

### Modernizr
<https://modernizr.com/>
- HTML5 와 CSS3 에 정의된 요소(HTML Elements), 속성(CSS Property)들에 대한 지원 여부를 점검하는 JavaScript Library.

```html
<script src="js/lib/modernizr-2.8.3.min.js"></script>
```

#### 기본 설정
```html
<html class="no-js">
```

#### CSS 사용법 예시
```css
header {
    background: linear-gradient(to right, red, orange);
}
.no-cssgradients header {
    background: url("/images/bg-gradient.jpg");
}
```

#### JavaScript 사용법 예시
```js
if (Modernizr.svg) console.log('svg: Available');

if (!Modernizr.input.placeholder) {
    var script = document.createElement('script');
    script.src = 'https://cdnjs.cloudflare.com/ajax/libs/placeholders/4.0.1/placeholders.min.js';
    document.head.appendChild(script);
};
```

### Prefixfree
<https://github.com/LeaVerou/prefixfree>
- `-ms-`, `-webkit-` 등의 공급 업체 접두사(Vendir Prefix)를 사용하지 않아도 크로스브라우징이 가능한 JavaScript Plugin.

#### 공급업체 접두어
| 접두어 | 공급업체 |
|---|---|
| -webkit- | 크롬, 사파리, 오페라의 최신 버전 |
| -mos- | 파이어폭스 |
| -o- | 오페라의 이전 버전 |
| -ms- | 인터넷 익스플로러 |

```html
<script src="js/lib/prefixfree.min.js"></script>
```

### jQuery
<http://jquery.com/>
- HTML 과 JavaScript 사이의 상호 작용을 강조한 경량화된 JavaScript Library.
- jQuery 의 장점
  - 쉬운 DOM 선택(CSS 선택자 활용)
  - 편리한 Event 활용
  - 특수효과 및 애니메이션
  - Ajax
  - 확장성 등...

```html
<script src="js/lib/jquery-1.10.1.min.js"></script>
```

### jQuery Easing
<https://github.com/gdsmith/jquery.easing>
<http://gsgd.co.uk/sandbox/jquery/easing/>
- jQuery 에서 Easing functions(equation, 애니메이션 진행 그래프) 사용할 수 있는 jQuery Plugin.

```html
<script src="js/lib/jquery.easing.min.js"></script>
```