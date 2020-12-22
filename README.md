# 텀프로젝트(기말고사) 

<br>

<details>
<summary>목차</summary>

- [과제 주제](#과제-주제)
- [기능 설명](#기능-설명)
- [DB 설명](#DB-설명)
- [사용 여부](#사용-여부)
- [비고 및 고찰](#비고-및-고찰)

</details>

<br>

# **과제 주제** 

텀 프로젝트 진행

<br>

# **기능 설명**

## 1. 로그인

- form 태그로 post method를 사용하여 body에 있는 입력값을 가져온다.
- 먼저 mysql select를 사용하여 해당하는 계정이 있는지, mysql error가 나는지 check한다.
- 해당하는 계정이 있을 경우 받아온 입력값을 사용하여 password를 check한다.
- 만약, 비밀번호가 틀릴 경우 alert 생성한다.
- 로그아웃은 세션에서 정보를 삭제하여 로그아웃된다.
- 게시판 페이지에 들어갈 때는 로그인 한 사람만 들어갈 수 있도록 하였습니다.


## 2. 회원가입

- form 태그로 post method를 사용하여 body에 있는 입력값을 가져왔다.
- password와 passwordchk를 확인하여 pssword가 맞는지 비교한다.
- 알맞게 채워 넣으면 회원가입이 진행된다.


## 3. 게시판 - 글 작성

- form 태그로 post method를 사용하여 body에 있는 입력값을 가져온다.
- mysql의 insert문을 사용하여 입력받은 제목, session에 있는 userName, content를 저장한다.


## 4. 게시판 - 글 수정

- put method를 사용한다.
- params로 수정할 id를 가져온다.
- sql의 update문과 where절을 사용하여 title 및 content update한다.


## 5. 게시판 - 글 삭제

- put method를 사용한다.
- params로 삭제할 id를 가져온다.
- sql의 delete문과 where절을 사용하여 해당 컬럼 삭제한다.


## 6. 게시판 - 글 리스트 가져오기

- mysql의 select 문으로 데이터를 가져와서 ejs의 for문을 사용하여 뿌려준다.


## 7. session 기능

- express-session을 설치하여 login할 때 session을 저장한다.


## 8. pagenation 기능


<br>

# **DB 설명**

## board 테이블

- id (auto_increment) 사용
- displayName (닉네임)
- username (유저이름)
- title (게시판 글 제목)
- content (게시판 글)
- w_date (작성일)

## user 테이블

- id (auto_increment) 사용
- username (닉네임)
- displayName (유저이름)
- password (유저 비밀번호) 
- email (유저 이메일)
- tel (전화번호)


<br>

# **사용 여부**

## 1. html, css만 사용하여 웹 페이지를 구현

- reset.css를 사용하여 모든 페이지의 style을 최적화시켜둔다.
- bootstrap을 사용하여 테이블 및 버튼 style 적용한다.


## 2. 웹 페이지 디자인

- bootstrap를 이용한 css의 기술들을 사용하였다.


## 3. javascript

- node를 사용하여 express 서버 연동했다.
- node를 사용하여 mysql 연동했다.
- CRUD의 기능을 적용했다.
- mysql session 기능을 적용했다.


## 4. express 서버 연동

- npm install express
- node를 사용하여 express 서버 연동했다.


## 5. DB 연동

- mysql 사용
- node를 사용하여 mysql 연동했다.

## 6. 인증

- mysql session을 사용하여 로그인 session 저장한다.

[ 4 ~ 6 ] 를 하기 위해 클라우드 서비스로 heroku를 활용하였다.


## 7. 메인 레이아웃
- 로그인/회원가입/게시판/글 작성/글 수정/글 detail 


# 비고 및 고찰

이번 과제를 진행하던 중 월요일에 교수님께서 서버와 DB를 추가 점수로 분류하고 프론트엔드 부분 위주로 평가하신다고 하여서 살짝 당황했다. 

세세한 디자인보다 전체적인 과제의 완성도를 우선으로 하여 비교적 난이도가 높은 서버와 DB에 중점을 뒀는데 갑작스럽게 하루 전에 과제가 수정되어 어쩔 수 없이 그대로 진행하였다. 

그래도 좋은 경험이 될 것 같다.


