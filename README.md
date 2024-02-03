# TeamProject1
프로젝트 소개 <br>
강의 이후 처음으로 제작하는 java프로그램이며, 팀프로젝트.<br>
DB class에 저장되어 있는 데이터를 원하는 조건의 맞춰 출력하는 프로젝트.<br>

제작 기간<br>
2023-12-6 ~ 2023-12-7 2DAY<br>

프로젝트 요약<br>
이클립스를 사용하여  학생의 관련 테이블과 데이터베이스를 만들어 각각의 메소드를 통해  <br>
(뷰-> 컨트롤러 -> 서버 -> 데이터베이스 ->서버 ->컨트롤러 -> 엔드뷰) 와같은 순서로 테이를 호출하고 출력하는 기능을가진 프로젝트입니다.<br>



패키지 목록<br>
1 .model.domain<br>

1-1. Studentmodel<br>
    학생 데이터를 저장할 테이블기능을 가진 class 입니다.<br>
    (String name,int age, int studentid, String grade, String hobby) 다섯가지 변수를 가지고있으면 테이블 필드를 생성합니다.<br>
    인스턴스 초기화를 위한 생성자, 특정 속성 값으로 인스턴스를 생성할수있는 매개변수화된 생성자 생성합니다.<br>
    Getter, Setter 를 생성하여 다른 클래스에서 속성값을 검색하거나 변경을 할수있는 메서드 생성합니다.<br>
    toSting 을 생성하고 @Override 어노테이션을 사용해서 메서드를 재정의하고 , toString 메서드는 속성값을 표시하는 문자열 표현을 생성합니다. <br>

2. studentview<br>

2-1. Startview<br>
    컨트롤러 class 에 있는 메소드를 실행시키는 기능을 가진 class입니다.<br>
    메인 메소드를 통해 호출한 기능을 수행하고 출력하도록 합니다.<br>
    StudentController 타입의 controller변수를 생성하고 StudentController.getInstance(); <br>
    을 사용해서 컨트롤러에 포함된 기능을 controller라는 변수만을 사용하여 쉽게 호출할수있도록합니다.<br>

2-2. EndView<br>
    스타트 뷰에서 시작된 메소드 호출이 데이터베이스에서 해당하는 값들을 가지고와 콘솔창에 출력하기위한 class 입니다.<br>
    *포인트* <br>
    ArrayList<제네릭> 으로 받아온 학새들의 정보를 모두 출력하도록 조건문을 사용했습니다.<br>

2-3. FailView<br>
    -StartView 에서 시작해 EndView까지 데이터를 반환하며 오류가 발생하면 실행되는 클래스입니다.<br>

3. studentcontroller<br>

3-1. StudentController<br>
    StartView로부터 메서드를 호출받아 실행되며 직접 DB에서 데이터를 가져오는것이아닌 Service를 통해 데이터를 <br>
    받아와 EndView로 전달하는 기능을 수행합니다.<br>

    <!-- *Exception 처리*<br>
    Servie에서 DB로부터 데이터를 받아올때 예외가 발생하며 이때 서비스에서 예외를 컨트롤에게 넘깁니다.
    넘어온 예외를 Try/Catch 문으로 처리하며 예외가발생하면 FailView를 실행하도록 설정했습니다. -->


4. student.service<br>

4-1. Studentservice<br>
    Controller 로 부터 호출받아 실행되며 DB에 저장되어있는 정보를 받아옵니다.<br>

    <!-- *Exception 처리*
    DB로부터 필요한 정보를 받아오며 예외가 발생하면 throws 를 사용하여 해당하는 예외를 Controller로 넘겨줍니다.

    *포인트*<br>
    특정 학생을 검색하는 기능에는 먼저 AraayList<제네릭>을 사용해 받아온 모든 학생의 정보를
    for문을 사용해 모든학생의 정보와 특정학생의 정보를 if문으로 정해서 호출합니다.
    이때, 특정 학생의 정보와 일치하지않는다면 예외가 발생하도록 설정되었습니다. -->


5. studentDB<br>

5-1. StudentDB<br>
    MySQL을 사용하기 이전에 제작하는 프로젝트로 Eclips프로그램 안에서 사용하도록 제작되어<br>
    DB를 java내부에 만들었습니다.<br>
    제네릭 을 사용해 변수를 생성하고 변수안에 임의에 학생들정보를 저장하여 Service로부터 호출되는 기능에 맞춰 데이터를 반환 합니다.<br>














