# Simple NESTJS learning

> with nomad coders...



## 배운 것들 

+ typescript

  타입스크립트는 javascript기반으로 자바스크립트에서 정적 타입을 명시 할 수 있다. 이를 통해 변수나 함수 등의 목적을 더욱 명확하게 전달하고, 각종 에러 알림과 같은 피드백도 미리 받을 수 있다.

  

+ DTO

  DTO는 data transfer object의 약자로써, 기본적으로 프로그래머가 코드를 더 간결하게 만들 수 있도록 해준다. 또한, nestjs가 들어오는 쿼리에 대해 유효성을 검사할 수 있게 해준다.

  

+ Validation Pipe(app.useGlobalPipes(new ValidationPipe({})))

  Validation Pipe는 데이터나 새로운 접근에 대하여 미리 검증함과 동시에 적절한 처리를 해주는 일종의 미들웨어를 설정하는 것이다. 

  + whitelist
    whitelist: true로 적용하면 아무 decorator도 없는 어떠한 property의 object도 받지 않는다. validator가 validate자체를 스킵한다. 리퀘스트를 막는 것은 아니다.
  + forbidNonWhitelisted
    whitelist와 기본적으로 같은데 아예 리퀘스트를 막아버린다.
  + transform
    transform: true오 적용할 경우 NestJs는 타입을 받아서 넘겨줄 때 자동으로 타입도 변환해 주게 된다.(Entity타입에 맞게 변환된다.)



+ Module
  NestJs는app.module의 @module에 여러 가지를 import하고 NestJS가 앱을 구동하면 모든 걸 하나의 모듈로 생성해준다. 
  + providers
    여기다가  service와 같은 파일을 넣어주면 자동으로 NestJS가 movieservice를 import하고 controller에 inject한다.(DI)



+ JEST
  Jest는 자바스크립트 테스팅 프레임워크로써, 명료함,간단함에 초점을 맞춘 테스트 프레임워크이다. 대부분의 자바스크립트 프로젝트에서 쓰일 수 있다.



### 삽질한 것들

+ 대부분의 노드 모듈 패키지에서 문제가 터진다. ts-compiler가 호환이 안된다고 뜬다. 그럴경우 관련된 package를 호환 된 버전을 찾거나 정 모르겠으면 최신걸로 다시 내려받자.
