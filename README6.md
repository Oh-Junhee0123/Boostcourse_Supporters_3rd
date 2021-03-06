<h1 align = "center">Boostcourse_Supporters_3rd[부스트코스 서포터즈 3기]</h1>
<h2 align = "center">쉽게 배우는 자바</h2>
<br>

>## STUDY DAY 8
<h3 align = "center">입력과 출력</h3>
<br>

프로그램의 입력과 출력
프로그램을 입력정보를 받아서 출력하는 것이라고 할 수 있다.

입력 정보는 문자열, 숫자 등의 아규먼트가 될 수도 있고, 파일, 네트워크를 통해 박은 정보, 소리, 다른 프로그램에서 출력된 정보 등이 될 수도 있다.
출력 정보는 화면에 출력하는 형태가 될 수 있고, 파일에 쓸 수도 있고, 소리로 내보낼 수도 있다.

JOptionPane 객체를 이용하기 위해서는 import 구문을 이용하여 불러온다.

JOptionPane의 showInputDialog를 이용해서 입력한 정보는 String 데이터로 받아들여진다.
이번에는 다이어로그를 이용해서 입력 값을 받는 방법이 아닌 아규먼트를 통해 입력 값을 받는 방법에 대해서 공부한다.

아규먼트를 입력하게 되면 main 메소드의 args 파라미터는 아규먼트 값을 받아서 동작하게 된다.
args는 문자열 배열로 여러 개의 String 데이터가 들어있을 수 있다.
인덱스를 통해 배열의 데이터를 꺼내 쓸 수 있고 인덱스는 0번부터 시작한다.

<br>

<h3 align = "center">직접 컴파일 하기</h3>
<br>

이클립스 없이 자바로 프로그래밍을 하려먼 우선 자바 파일을 스스로 컴파일 할 수 있어야 한다.

그리고 컴파일한 클래스 파일을 실행하는 과저을 거쳐야 한다.

직접 컴파일을 하기 위해서는 자바의 설치 경로를 알고 있어야 한다.

1. 터미널 열기

윈도우 키 + R을 눌러 실행 창을 열고, cmd를 입력해 명령 프롬프트를 실행한다.

2. javac 확인하기

터미널에 javac를 입력하고 실행하면 명령어의 사용 방법이 출력된다.

3. 환경 변수 경로 확인하기

윈도우 탐색기에서 내 PC 항목을 오른쪽 버튼으로 클릭해 나오는 팝업창에 속성을 클릭한다.
고급 시스템 설정을 클릭한다.
환경 변수를 클릭하면 환경 변수 목록을 확인할 수 있다.
Path를 더블클릭하면 수정이 가능하다.

4. 프로젝트 디렉토리로 이동하기

명렁 프롬프트에서 cd 명령어를 통해 프로젝트 디렉토리로 이동한다.
dir 명령어로 프로젝트 디렉토리 내부의 구조를 확인할 수 있다.

5. 자바 파일 컴파일하기

터미널에 javac를 입력하면 javac 명령어의 사용 방법을 보여준다.
ls 명령어를 입력하면 Program.class가 생성된 것을 확인할 수 있다.

6. 실행하기

컴파일된 클래스 파일을 실행하기 위해서는 java 명령어를 이용한다.
java 명령어로 컴파일된 파일을 가상 머신에서 실행하는 작업을 한다.
실행할 때는 .class를 붙이지 않는다.

7. 외부 라이브러리도 포함해서 컴파일하기

외부 라이브러리를 포함해서 컴파일하기 위해서는 javac 명령어의 옵션 중 --class-path(-cp) 옵션을 이용해서 외부 라이브러리도 함께 지정해야 한다.
외부 라이브러리의 클래스들도 함께 사용하는 프로그램을 실행하기 위해서는 컴파일했을 때와 마찬가지로 --class-path 옵션에 외부 라이브러리도 포함해서 실행해야 한다.

<br>

>## STUDY DAY 9
<h3 align = "center">API vs UI</h3>
<br>

우리는 컴퓨터에 운영체제를 설치하고 운영체제 위에 자바를 설치했다.
자바의 라이브러리에는 다양한 도구들이 있는데, 모니터에 출력했을 때 사용했던 System 객체를 비롯해 Data, Math, PrintWriter 등 다양한 도구들이 있다.

우리는 자바 프로그램을 만들 때 자바의 도구들을 응용해 우리가 원하는 작업을 시간적 순서에 따라 동작하도록 만들었다.

작업들의 시간적 순서에 주목해서 우리는 프로그램이라고 부르고 도구의 응용에 주목해서 우리는 애플리케이션이라고 부른다.

이때 자바는 자바의 도구들을 응용해서 사용하기 위해 일정한 조작 장치를 구성했는데, 이것이 자바 API이다.

자바 프로그램을 또 다른 자바 프로그램에서 사용될 수도 있고 다른 프로그램에서 사용할 수 있도록 만들어둔 장치 역시 API이다.

이렇게 만들어진 자바 프로그램은 사용자가 사용할 수 있다.

이때 사용자가 자바 프로그램을 사용할 수 있도록 만들어둔 장치들을 UI라고 한다.

<br>

<h3 align = "center">패키지, 클래스, 변수, 메소드</h3>
<br>

Java API Documentation 보는 방법
자바 프로그램을 만들기 위해서는 자바의 도구들을 사용할 수 있게 만든 장치인 자바 API를 이용해야 한다.

오라클에서는 자바 API의 설명서인 Java API Documentation을 제공하고 있다.

1. 포털 검색을 통해 Java API Documentation 페이지를 연다.
(왼쪽의 위쪽 섹션에는 패키지들에 대한 정보를 담고 있고 왼쪽의 아래 섹션에는 클래스에 대한 정보를 담고 있다.)
2. 왼쪽의 아래 섹션에서 우리가 전에 사용해 보았던 Math 클래스를 클릭해서 정보를 확인해 본다.
3. Math 클래스는 java.lang 패키지에 속해 있다는 것을 확인할 수 있다.

클래스, 변수, 메소드, 패키지
Math 클래스와 같이 클래스 안에는 PI와 같은 변수, floor, ecil과 같은 메소드들이 포함되어 있다.

패키지는 이러한 클래스들을 하나의 묶음으로 정리한 것이다.

<br>

<h3 align = "center">클래스</h3>
<br>

클래스란 서로 연관된 변수와 메소드로 구성되고 연관된 클래스를 묶어서 정리한 것이 패키지이다.

Math 클래스에는 수학과 관련된 여러 변수들과 메소드들이 있다.
PI 변수는 원주율이 적절한 정밀도로 저장되어 있는 변수이다.
floor 메소드는 특정 소수점 이하에 대해 버림한 값을 산출한다.
ceil 메소드는 특정 소수점 이하에 대해서 올림한 값을 산출한다.

<br>

<h3 align = "center">인스턴스</h3>
<br>

인스턴스를 만드는 이유
인스턴스는 객체를 다양한 상태에서 사용하고 기능을 재사용할 경우가 많은 상황에서 유용하기 때문이다.

<br>

<h3 align = "center">상속</h3>
<br>

클래스의 상속관계
클래스 간에는 서로 계층적인 관계를 갖고 있을 수 있다.

들려쓰기가 되어 표현된 각각의 클래스 간의 관계는 상속 관계를 나타낸다.

클래스 간의 상속관계의 특성
자식에 해당하는 클래스의 부모에 해당하는 클래스의 모든 변수와 메소드를 사용할 수 있다.

PrintWriter는 Writer를 확장해서 만들어진 클래스이다.
Writer는 Object를 확장해서 만들어진 클래스이다.

따라서 PrintWriter 클래스는 Writer의 write 메소드를 사용할 수 있고 Object의 toString 메소드를 사용할 수 있다.

Object 클래스는 모든 클래스의 부모로 모든 클래스는 Object의 변수와 메소드를 상속받는다.

<br>
