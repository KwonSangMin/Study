Synchronous (동기)
  - Caller 함수가 제어권을 가질 때마다 Called 함수가 특정 값을 Caller함수에 전달하는 경우.
      
Asynchronous (비동기)
  - Caller 함수가 제어권을 가지는 것과 Called 함수가 특정 값을 Caller함수에 전달하는 것이 관련(관심)이 없는 경우.
     
Blocking
  - Caller 함수가 Called 함수가 Return 할 때 까지 대기하는 것.

Non-Blocking
  - Caller 함수가 Called 함수의 Return 값을 기다리지 않고 계속 코드를 실행하는 것.
  
ex) 
Non-Blocking & Synchronous
  -Spin Lock(=Busy Waiting)의 While(try_lock()) 함수는 Caller함수의 실행을 막지않으므로 Non-Blocking이다. 또한, 제어권을 가지고 실행할 때마다 try_lock()이 매번 값을 반환하므로 Synchronous이다.

Blocking & Synchronous
  - int add(int a, int b){
    for (int i=0;i<100000;i++)
      a+=b;
    return a;
  } 
  위와같은 일반적인 함수들은 함수 실행이 완료될 때까지 Caller함수가 Block되며 제어권을 돌려줄 때 결과값을 함께 리턴해주므로 Blocking & Synchronous이다.
  
  Non-Blocking & Asynchronous
    - Naver와 같은 웹페이지를 브라우저를 통해서 가져올 때 이미지, 텍스처와 동영상 등을 불러오게 되는데, 이때 Main함수에서는 GetImage, GetText, GetVideo를 순차적으로 Call 하지만 결과값을 기다리지 않고 바로 다음 코드를 실행하며 Main함수에서는 Return 값을 관여하지 않는다.
  
  Blocking & Asynchronous
    - 멀티 쓰레드 서버에서 Client의 요청을 처리할 때 사용하는 Thread Pool에서 사용된다고 한다.
      왜냐하면, Client로부터 연결을 담당하는 Thread는 오직 연결하고 Worker 쓰레드로 작업을 넘겨주는 것만 담당하기 때문이다.
