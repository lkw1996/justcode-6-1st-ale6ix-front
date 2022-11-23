# ALE6IX PROJECT

## 프로젝트 소개

- 해외 유명 디자이너 브랜드 ALESSI (http://alessi.co.kr) 를 클론 코딩 하였습니다.
- 프로젝트 내의 짧은 기간동안 세션 복습과 새로운 기능을 도전해 보고자 디자인은 클론코딩 하였고 기능을 구현하는 데에 중점을 두었습니다.
- 개발은 최소한의 라이브러리를 사용하여 직접 구현하였고 영상에서 보여지는 부분 모두 Fetch함수와 api를 이용하여 백엔드와 통신하여 작업하였습니다.

### 개발 인원 및 기간

- 개발기간 : 2022/8/29 ~ 2022/9/8
- 개발 인원 : 프론트엔드 4명, 백엔드 2명
- [백엔드 github 링크](https://github.com/wecode-bootcamp-korea/justcode-6-1st-ale6ix-back)

### 프로젝트 선정이유

- E-commerce는 필요한 부분을 컴포넌트화하여 섹션을 나누거나 fetch를 이용하여 api통신으로 데이터를 주고 받는등
  지금까지 학습한 부분을 각자 맡은 페이지내에서 복습할 수 있고 새로운 기능을 추가로 학습할 수 있기에 선정하게 되었다.

### 데모 영상(이미지 클릭)

[![home](https://velog.velcdn.com/images/ch00ng10000/post/3ff906f7-d6ea-43a6-92f1-fc37b06e3eae/image.png)](https://youtu.be/X2f3YSx6h0Q)

<br>

## 적용 기술 및 구현 기능

### 적용 기술

> - Front-End : React.js, sass, slick, react-modal
> - Back-End :  node.js, express, jwt, Bcrypt, My SQL
> - Common : RESTful API


### 구현 기능👇

### 회원가입
https://user-images.githubusercontent.com/103557910/190311848-7b40b3c3-ef0b-416d-9f9d-aa3987227d34.mp4
- 아이디 중복 검사
- 휴대폰 인증번호받기 구현(휴대전화 10자리 이상 때만 '인증번호받기' 버튼 활성화)
- 이용약관 체크박스 구현
- 회원가입 완료 페이지에 DB에 등록된 유저의 정보(ID, NAME, EMAIL) 확인 section 구현
### 로그인
https://user-images.githubusercontent.com/103557910/190311806-a61f4ec2-0e9d-49c1-86be-c0e61c43c99a.mp4
- 회원여부 확인
- 로그인 성공 시 유저의 TOKEN 로컬스토리지에 저장
- 로그인 상태에서 nav header에 유저의 ID 나타나게 구현
- 로그아웃 시 main page로 이동 및 로컬스토리지에 있는 token 삭제
### 메인페이지
- 이미지 슬라이드 구현(라이브러리 사용x, 슬라이드 버튼 기능, 무한 슬라이드)
- 중복 Title컴포넌트 화
- Magazine 목데이터 사용
- 데이터 받아서 제품섹션 구현
### 제품 페이지
- 서버에 데이터 요청 이후 받아온 데이터로 레이아웃 및 스타일링 구현
- 오프셋 기반의 페이지네이션 이용하여 페이지 버튼 및 로직 구현
- 각 제품 클릭시 해당하는 제품 상세 페이지로 이동하도록 동적 라우팅 구현
### 제품 상세페이지
https://user-images.githubusercontent.com/100896832/190037169-28a7dff9-cf77-4e42-8583-b76d1ef0eb66.mp4
- 제품 상세 데이터 서버에 요청 이후 레이아웃 구현 및 스타일링
- 수량(+,-)버튼 구현, 상품수량이 상품재고보다 많아지면 재고 알림창 구현
- POST 요청 : 수량,제품번호 post 통신
- 상품문의, 후기 : 추가&삭제 버튼 기능 구현. api호출 (GET: 렌더링 ,POST: 추가 ,DELETE: 삭제)
### nav,footer
- 내비게이션 메뉴 카테고리 클릭 시 해당하는 데이터 페이지로 이동하도록 동적 라우팅 구현
### 검색창
https://user-images.githubusercontent.com/100896832/190058209-81c8bdc1-f5f7-4ec4-b3c1-a13d225d83fd.mp4
- GET : 서버로부터 query문 사용하여 값을 가져옴
- GO!버튼 클릭 or Enter 검색한 상품들이 나오게 구현
### 장바구니
[https://user-images.githubusercontent.com/100896832/190034745-3bc71213-3d35-449f-b8d6-559ff5bb8991.mp4](https://user-images.githubusercontent.com/100896832/190036250-5f0e6159-baae-4493-baab-3821ba085697.mp4
)
- 조건부 렌더링으로 상품이 없을때 '장바구니 가 비어있습니다' 문구 구현
- GET : 장바구니에 담긴 상품들 화면에 렌더링
- PATCH : 장바구니 상품 수량변경 -> 유저 아이디,상품 아이디,변경된 수량을 담아서 요청 
- DELETE : 개별 상품 삭제, 체크된 상품 삭제, 전체삭제(장바구니 비우기)

## 개인별 구현 사항

#### 김충만/FE
- 회원가입 페이지
- 로그인 페이지
- NAV HEADER 통신 

#### 서지원/FE
- 메인페이지 레이아웃
- 제품 상세페이지 POST 요청
- 장바구니 레이아웃, 기능구현 및 통신
- 검색창 레이아웃, 기능구현 및 통신

#### 양미옥/FE
- 메인페이지 제품 섹션 컴포넌트화, 레이아웃
- 메인페이지 이미지슬라이드 버튼기능, 무한슬라이드
- NAV Bar & Footer 레이아웃, 내비게이션 바 mock-up 기능구현
- 상품문의, 후기 레이아웃 기능구현 및 api통신

#### 이기완/FE
- 제품 페이지 레이아웃, 기능구현 및 통신
- 제품 상세 페이지 레이아웃, 기능구현 및 통신
- React Router 이용 - Nav bar / 제품 상세 동적 라우팅 구현
- React paginate 이용 - 제품 페이지 내 페이지네이션 기능 구현

 ---

<br>

## 팀원 github주소

[김충만/FE](https://github.com/kimchoongman)
<br>
[서지원/FE](https://github.com/tjwldnjs123)
<br>
[양미옥/FE](https://github.com/miogy)
<br>
[이기완/FE](https://github.com/lkw1996)

## Reference

- 이 프로젝트는 [알레시](http://alessi.co.kr) 사이트를 참조하여 학습목적으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
- 이 프로젝트에서 사용하고 있는 사진 모두 알레시 코리아의 동의하에 작업되었습니다.
