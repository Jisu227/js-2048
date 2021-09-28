# *2048 게임*



#### 🎯 *실행 화면*


![Sep-29-2021 01-51-02](https://user-images.githubusercontent.com/86669143/135131145-32a6f331-49e1-4ef6-aaad-6e570ff91cc8.gif)



---
#### 🧩 *배운 내용 정리하기*

    1. documentFragment
    => 실무에서는 화면에 태그를 추가할 때 createElement로 만들어서 태그에 바로 추가(append)하는
       방식을 잘 사용하지 않는다. 그 대신 document.createDocumentFragment 메서드로 메모리
       안에서만 존재하는 documentFragment를 만들고, documentFragment 안에 필요한 태그를 추가
       (append)한 뒤 마지막으로 $table에 한 번에 documentFragment를 추가하는 방식을 사용한다.

    2. 키보드 이벤트
    => 대표적인 키보드 이벤트에는 keydown과 keyup이 있다. 키보드를 누를 때와 눌렀다 뗄 때 각각 호출된다.
       어떤 키를 눌렀는지는 event.key 속성에 나온다. 왼쪽은 ArrowLeft, 오른쪽은 ArrowRight ,
       위쪽은 ArrowUp, 아래쪽은 ArrowDown이다. 이를 통해 방향을 확인할 수 있다.
       event.ctrlKey(Ctrl 키) , event.altKey(Alt 키) , event.shiftKey(Shift 키),
       event.metaKey(윈도우 키) 속성도 제공해 다른 키와 동시에 누르는 것도 알아낼 수 있다.
    
    3. 마우스 이벤트
    => 대표적인 마우스 이벤트에는 mousedown, mouseup, mousemove 가 있다.
       각각 마우스를 클릭할 때와 클릭했다가 뗄 때, 마우스를 이동할 때 호출된다.

       마우스 이벤트의 속성에서 x,y 좌표를 얻을 수 있으며 이를 이용해 마우스 위치의 변화를 잡아 낼 수 있다.
       좌표에는 당므과 같은 종류가 있다.

    - clientX, clientY 는 현재 브라우저 페이지 내에서의 x,y 좌표를 가리킨다(픽셀 단위).
    
    - pageX 와 pageY 도 브라우저 페이지 내에서의 x,y 좌표를 가리키지만, 스크롤이 있는 경우 
      스크롤한 픽셀 값까지 포함한다.
    
    - offsetX 와 offsetY 는 이벤트를 연결한 대상을 기준으로 마우스의 x,y 좌표를 가져온다.

    - screenX 와 screenY 는 모니터를 기준으로 모니터의 왼쪽 모서리가 0이 된다.

    - movementX 와 movementY 는 지난 mousemove 이벤트와 비교해 얼마나 마우스를 움직였는지 
      표시하므로 mousemove 이벤트인 경우에만 실제 값이 잡힌다.