# Public Advanced(중급반)
중급반 학생을 위한 프로젝트 폴더

## JavaScript Libraries

### ie9
<https://code.google.com/archive/p/ie7-js/>
- IE5.5 ~ IE8 (IE: Microsoft Internet Explorer) 버전을 IE9 버전처럼 표현(style)할 수 있는 JavaScript Library.
- 조건부 주석(Conditional Comments)과 함께 사용

```html
<!--[if lt ie 9]>
<script src="js/lib/ie9.js"></script>
<![endif]-->
```

### respond
<https://github.com/scottjehl/Respond>
- CSS @media 를 IE6 ~ IE8 버전에서 사용 가능하게 만들어주는 JavaScript Library.
- 조건부 주석(Conditional Comments)과 함께 사용

```html
<!--[if lt ie 9]>
<script src="js/lib/respond.min.js"></script>
<![endif]-->
```

### modernizr
<https://modernizr.com/>
- HTML5 와 CSS3 에 정의된 요소(HTML Elements), 속성(CSS Property)들에 대한 지원 여부를 점검하는 JavaScript Library.

```html
<script src="js/lib/modernizr-2.8.3.min.js"></script>
```

CSS 사용법 예시
```css
header {
    background: linear-gradient(to right, red, orange);
}
.no-cssgradients header {
    background: url(/images/bg-gradient.jpg);
}
```

JavaScript 사용법 예시
```js
if (Modernizr.svg) console.log('svg: Available');

if (!Modernizr.input.placeholder) {
    var script = document.createElement('script');
    script.src = 'https://cdnjs.cloudflare.com/ajax/libs/placeholders/4.0.1/placeholders.min.js';
    document.head.appendChild(script);
};
```

### prefixfree
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
  - DOM 선택(CSS 선택자 활용)
  - Event
  - CSS 조작
  - 특수효과 및 애니메이션
  - Ajax
  - 확장성 등...

```html
<script src="js/lib/jquery-1.10.1.min.js"></script>
```

### jQuery.easing
<https://github.com/gdsmith/jquery.easing>
<http://gsgd.co.uk/sandbox/jquery/easing/>
- jQuery 에서 Easing functions(equation, 애니메이션 진행 그래프) 사용할 수 있는 jQuery Plugin.

```html
<script src="js/lib/jquery.easing.min.js"></script>
```