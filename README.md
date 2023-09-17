# 인하공업전문대학 홈페이지 프로젝트

## 프로젝트 개요
이 프로젝트는 인하공업전문대학의 홈페이지를 개발한 웹 개발자의 포트폴리오입니다. 이 홈페이지는 JSP를 기반으로 만들어져 있으며, 회원 관리, 게시판, Kakao 맵을 포함한 다양한 기능을 제공합니다.
## 환경세팅 및 기술 스택
- 사용 언어 : java (jdk 12.0.2), JavaScript, css, html
- 사용 툴 : Eclipse
- 데이터베이스 : Mysql8
- 서버 : Tomcat
- 테스트 브라우저 : Chrome, Edge
- - - 
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
 
- 깨달은 점:
1. 효율적인 데이터베이스 설계는 S/W의 성능과 유지보수성에 큰 영향을 미칩니다.
2. 데이터베이스 분할 및 분리는 성능 최적화와 데이터 관리를 용이하게 만듭니다.



