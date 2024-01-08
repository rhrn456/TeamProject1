# TeamProject1

1. Studentmodel : 학생 정보 관리 시스템에서 학생들의 정보를 저장하는 인스턴스 변수를 지정하고 Getter AND Setter AND toString() 메서드를 적용한다

2. StudentDB : 학생들의 데이터베이스로서 정보를 저장한다(당시 mySQL 을 배우지않은상태로 따로 데이터베이스를 구축하지못해 자바파일로 생성하여 사용)
                또한 SduentController 로부터 메소드를 호출받아 데이터를 조건의 맞춰 넘겨주는 기능.

3. View :  
            StartView :시작하는 메인 뷰로 StudentController파일로 원하는 기능을 호출한다.
            EndView : StudentController에서 데이터를 받아 출력해주는 기능.
            FailView : 기능이 제대로 작동하지않았을때 메시지를 출력하는 기능.

4. Studentservice : StudentController 와 StudentDB 사이에서 메서드를 호출하거나(컨트롤러)  데이터를 전달(DB로부터)