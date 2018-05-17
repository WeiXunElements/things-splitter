things-splitter
=============

1.화면에서 내부 구분선으로 화면의 싸이즈를 조정하는 용도다.

`things-splitter`는 화면에서 분할선을 제공하여 화면의 크리를 분할 시키는 용도로 사용한다.
많은 direction이라는 속성으로 분리를 시키고 있는데 화면을 자동으로 크지고 작아지게 하려면 direction의 
반대 element가 자동으로 사이즈를 맞출 수 있게 Class를 설정한 후 많이 사용한다.

Example:

```html
    <div class="layout horizontal">
      <div>left</div>
      <things-splitter direction="left"></things-splitter>
      <div class="layout flex">right</div>
    </div>
```

위 예제에서는 왼쪽의 화면 싸이즈를 조정하지만 왼쪽의 화면 싸이즈가 작아지면서 flex layout으로 자동으로 오른쪽을 체워준다.

Example:

```html
    <div class="layout horizontal">
      <div>top</div>
      <things-splitter direction="up"></things-splitter>
      <div class="layout flex">bottom</div>
    </div>
```

따라서 상하 분할 layout은 up이나 down을 사용하고 좌우 분할은 left/right를 사용한다.

단, things-grid는 그리드에서는 화면싸이즈의 변화를 window size변화만 감지할 수 밖에 없어서 size변화가 완료 되면
grid의 화면을 fit시켜 줘야 한다.