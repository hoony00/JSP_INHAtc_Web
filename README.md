# 인하공업전문대학 홈페이지 프로젝트
### <a href ="https://hooninha.tistory.com/21"> Blog 바로가기</a>  <p>
# 프로젝트 개요
이 프로젝트는 인하공업전문대학의 홈페이지를 개발한 웹 개발자의 포트폴리오입니다. 이 홈페이지는 JSP를 기반으로 만들어져 있으며, 회원 관리, 게시판, Kakao 맵을 포함한 다양한 기능을 제공합니다. <p>
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/af637a19-0c92-430e-a0a9-0e95d1f749fb.png)

-----------



## 환경세팅 및 기술 스택
- 사용 언어 : java (jdk 12.0.2), JavaScript, css, html
- 사용 툴 : Eclipse
- 데이터베이스 : Mysql8
- 서버 : Tomcat
- 테스트 브라우저 : Chrome, Edge

![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/11bbb2e1-1fdb-4c78-8aeb-752f28e22436.png)



----------
# 화면 리스트

### 로그인 회원가입
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/3f0d8128-d6c7-4d1b-ae80-20ed5078b1bc.png)

### 게시판
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/dd19104f-e849-4240-a596-130fd7ad72e8.png)

### 학점 계산기
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/70e34de6-3f80-4afa-befc-536a50010f11.png)


### 건물정보
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/db033c69-7031-4011-b171-c9bf3c40c90a.png)

#### SALT 이용 암호화 (SHA - 512)
![image](https://github.com/hoony00/JSP_INHAtc_Web/assets/86902854/0909d1fd-efd3-439c-9fbc-1543f3f964e6.png)

## 주요 기능
1. 게시판: 웹사이트 내에 다양한 게시판을 구현했습니다. 사용자는 각 게시판에서 글을 작성, 조회, 댓글 달기, 글 수정 및 삭제가 가능합니다.

2. 이미지 첨부 기능: 분실물 게시판에서는 이미지를 첨부할 수 있어 사용자가 분실물을 게시할 때 더 많은 정보를 제공할 수 있습니다.

3. 암호화: 사용자의 비밀번호를 안전하게 저장하기 위해 SHA-512 해시 알고리즘을 사용하였고, Salt를 추가하여 보안을 강화했습니다.

4. 학점 계산기: 학생들을 위한 학점 계산기를 제공하여 학점을 간편하게 계산할 수 있도록 했습니다.

5. 대외활동 포스터 게시: 학교 대외활동 정보 게시와 포스터 첨부 기능을 구현했습니다.

6. 개인 시간표 등록: 학생들은 개인 시간표를 등록하고 관리할 수 있도록 했습니다.

7. 건물 정보 및 주차 구역 확인: KakaoMap API를 활용하여 학교 건물 정보와 주차 구역을 확인할 수 있도록 했습니다.

- - -

## 어려웠던 부분과 해결 방법

- 게시판 데이터베이스 구조: 다수의 게시판을 다루고 사용자가 선택한 게시판을 불러오는 로직에서 코드 양을 최소화하고 유지보수성을 높이는 것도 고려해야 했습니다.
  JSP 특성상 매개변수를 넘겨주는 식으로 다음 페이지에 접근하므로, 테이블을 수평으로 분할하는 방법을 적용했습니다. 각 게시판을 별도의 데이터베이스 테이블로 분할하여 저장하였고,
  이로써 각 게시판에 대한 데이터가 별도의 테이블에 저장되므로 데이터의 관리와 쿼리 작성이 훨씬 효율적으로 이루어지게 되었습니다. 게시글 테이블과 댓글 테이블 등 게시판과 관련된 데이터는 각각의 게시판 번호를 참조하여 분할 저장됩니다.
 
- 깨달은 점
1. 효율적인 데이터베이스 설계는 S/W의 성능과 유지보수성에 큰 영향을 미칩니다.
2. 데이터베이스의 정규화와 반정규화를 적절히 활용하고 테이블 파티셔닝 기법을 깊이 학습하여 성능 최적화와 데이터 관리를 용이하게 만드는 데 노력해야 할 것 같습니다.


