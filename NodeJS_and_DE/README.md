# Node.JS와 개발환경

## 프로그래밍 언어와 JavaScript
-  Compiled와 interpretered의 차이점은?
  <br>
  Compiler와 Interpreter 둘 다 C언어나 Java같은 고레벨언어로 작성된 프로그래밍 언어를 기계어로 변환하는 것은 맞지만 그 과정에 있어서 차이를 보인다.
  ![컴파일러와 인터프리터의 차이 이미지](compile_interpret.png)
> <b>Compile</b> : <br>원시코드(프로그래머가 작성한 소스코드)를 런타임 이전에 기계어로 해석하는 작업 방식. 이 때 원시코드를 목적 코드(Object Code)로 바꿔준다. <br>
런타임 이전에 Assembly 언어로 변환하기 때문에 구동 시간이 오래걸리지만, 구동된 이후는 하나의 패키지로 매우 빠르게 작동하게 된다. 구동시에 코드와 함께 시스템으로부터 메모리를 할당받으며 할당받은 메모리를 사용하게 된다. <br>
런타임 이전에 이미 해석을 마치고 대게 컴파일 결과물이 바로 기계어로 전환되기 때문에 OS 및 빌드 환경에 종속적이다. 그러므로 OS환경에 맞게 호환되는 라이브러리와 빌드환경을 구분해서 구축해줘야 한다. <br>
Compile 언어로 C/C++을 들 수 있으며, Java 역시 컴파일러가 Java파일을 컴파일해서 Byte Code를 만든다(그리고 Byte Code를 런타임에서 인터프리터가 해석한다).

> <b>Interpret</b> : <br>
원시코드(프로그래머가 작성한 소스코드)를 기계어로 변환하는 과정없이 한줄 한줄 해석하여 바로 명령어를 실행하는 방식. <br>
프로그래밍 언어를 기계어로 바로 바꾸지 않고, 중간 단계를 거친 뒤, 런타임에서 즉시 해석하기 때문에 컴팩트한 패키지 형태로 Binary파일을 뽑아낼 수 있는 Compile 방식에 비해 낮은 퍼포먼스를 보인다.<br>
런타임에 직접 코드를 구동시키는 특징이 있기 때문에 실제 실행시간은 느리며, 대신 런타임에 실시간 Debugging 및 코드 수정이 가능하다. 또한 메모리를 별도로 할당받아 수행되지 않으며, 필요할 때 할당하여 사용한다. <br>
대표적인 Interpreter언어로는 JavaScript와 같은 스크립팅 언어들이 있다. 하지만 이뿐만 아니라 컴파일 이후의 동작에서 Interpret을 수행하는 언어들도 많이 존재한다.<br>
많은 언어들이 해석을 위한 Virtual Machine을 두고, Machine위해서 Interpret을 수행하게 되는데, 이 때 해석의 기반이 되는 머신들이 OS환경들을 지원해줌으로써 OS 및 플랫폼에 종속되지 않는 프로그램 구동이 가능하다(이런 inpterpreter에는 Java의 JVM과 Python의 Analyzer가 있다 - 둘 다 Byte Code를 사용하기 때문에 Virtual Machine이 필요하다).

<br>
출처: <br>
<a href="https://m.blog.naver.com/ehcibear314/221228200531" target="_blank">컴파일러와 인터프리터의 차이</a><br>
<a href="https://jins-dev.tistory.com/entry/Compiler-%EC%99%80-Interpreter-%EC%9D%98-%EA%B0%9C%EB%85%90%EA%B3%BC-%EC%B0%A8%EC%9D%B4%EC%A0%90" target="_blank">컴파일러와 인터프리터의 개념과 차이점</a>
