#haeun

> flex-direction방향으로 자식 속성 배치

```css
justify-content: space-between;
justify-content: space-around;
justify-content: flex-start;
```

> flex-direction의 수직방향 으로 자식 속성 배치

```css
align-items: strech;
align-items: base-line;
align-items: center;
```

> 속성 계산이 필요한 경우

곱셈과 나눗셈의 좌우에는 공백이 없어도 됩니다. 하지만, 덧셈과 뺄셈의 좌우에는 공백이 있어야 합니다

```css
font-size: calc(10px + 10px);
```

> 한 페이지의 특정 위치로 스크롤 이동하기

id가 infobtn인 요소에 클릭 이벤트 → 이동할 특정요소(info)의 위치 반환 후 → animate 로 부드럽게 이동

```jsx
$(document).ready(function () {
  $("#infobtn").click(function () {
    var offset = $("#info").offset();

    $("html").animate({ scrollTop: offset.top - 81 }, 400);
    //선택한 위치로 부터 header높이를 제외한위치로 이동
  });
});
```
