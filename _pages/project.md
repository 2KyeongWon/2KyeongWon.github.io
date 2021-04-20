---
title: "재고 관리 "
permalink: /Project/
layout: single

author_profile: true
---

## 재고 관리 3인 프로젝트입니다.

#### 제작기간 21년4월10일~ 21년4월20일

> 개발 목적

핸드폰으로 손 쉽게 재고관리가 가능한 웹사이트
오늘 사용한 재고를 출고하고 주문을 통해 입고를 하는 간단한 프로젝트 입니다.

> 개발 순서

업무분석 -> 인터페이스 구성 -> 시스템제작 -> DB구축 -> 오류수정 -> 완성

1. 업무 분석
   주제 선정
2. 인터페이스 구성
   기본 템플릿 AdminLTE를 이용
3. 시스템 제작
   Spring, ajax, jQuery를 사용하여 제작
4. DB 구축
   OracleDB 사용
5. 오류 수정

> 프로그램 설명

**홈 화면, 로그인(세션이용), 회원가입**
<img src="/assets/images/index.jpg" width="800" height="800"/>
로그인 후 사이트 이용 가능, 회원가입 기능

**로그인 후 홈 화면**
<img src="/assets/images/home.jpg" width="800" height="800"/>
재고관리, 거래처 확인 등 확인가능

**재고 추가, 수정, 삭제**
<img src="/assets/images/edit.jpg" width="800" height="800"/>
ajax를 이용해 재고 추가, 수정, 삭제 기능

**거래처 추가, 수정**
<img src="/assets/images/customer.jpg" width="800" height="800"/>
ajax를 이용해 거래처 추가, 수정, 삭제 기능

**재고 알람**
<img src="/assets/images/alarm.jpg" width="800" height="800"/>
재고 수량이 5개 이하면 나타납니다

**주문, 입고**
<img src="/assets/images/order.jpg" width="800" height="800"/>
주문시 바로 입고 처리 됩니다

**출고**
<img src="/assets/images/outcount.jpg" width="800" height="800"/>
출고시 바로 출고 처리 됩니다

**출입고 확인**
<img src="/assets/images/inout.jpg" width="800" height="800"/>
입출고 확인 기능입니다
수량 x 가격 입니다 !

**1:1 문의사항**
<img src="/assets/images/question.jpg" width="800" height="800"/>
DB에 글과 댓글 기능을 만들어 기본 템플릿을 가져와 코딩만 하였습니다

**1:1 문의사항 관리자 화면**
<img src="/assets/images/masterquestion.jpg" width="800" height="800"/>
관리자는 모든 회원 목록과 함께 대화 내용이 나옵니다

> 사용한 Oracle Table

테이블 이름: MEMBERS
**고객정보**

| 순번 |  한글명  |    영문명     |  데이터타입   |
| :--: | :------: | :-----------: | :-----------: |
|  1   | 고객번호 |  MEMBER_NUM   |  NUMBER(5,0)  |
|  2   | 고객이름 |  MEMBER_NAME  | VARCHAR2(30)  |
|  3   |  이메일  | MEMBER_EMAIL  | VARCHAR2(360) |
|  4   | 패스워드 |  MEMBER_PWD   | VARCHAR2(60)  |
|  5   | 장바구니 | MEMBER_BASKET |  NUMBER(5,0)  |

테이블 이름: IM
**재고목록**

| 순번 |  한글명  |   영문명   |  데이터타입   |
| :--: | :------: | :--------: | :-----------: |
|  1   | 고객번호 | MEMBER_NUM |  NUMBER(5,0)  |
|  2   |   번호   |    IDX     |  NUMBER(5,0)  |
|  3   | 상품코드 |    CODE    | VARCHAR2(30)  |
|  4   |  상품명  |    NAME    | VARCHAR2(30)  |
|  5   |   가격   |   PRICE    |  NUMBER(5,0)  |
|  6   |  거래처  |   MARKET   | VARCHAR2(300) |
|  7   |   비고   |  REMARKS   | VARCHAR2(360) |
|  8   |   수량   |  QUANTITY  |  NUMBER(5,0)  |
|  9   |   날짜   |  REGDATE   | VARCHAR2(300) |

테이블 이름: CUSTOMERS
**거래처목록**

| 순번 |  한글명  |   영문명   |  데이터타입   |
| :--: | :------: | :--------: | :-----------: |
|  1   | 고객번호 | MEMBER_NUM |  NUMBER(5,0)  |
|  2   |   번호   |    IDX     |  NUMBER(5,0)  |
|  3   |   분류   |    CODE    | VARCHAR2(60)  |
|  4   | 거래처명 |    NAME    | VARCHAR2(60)  |
|  5   |   전화   |   PRICE    | VARCHAR2(60)  |
|  6   |  이메일  |   MARKET   | VARCHAR2(300) |
|  7   |   비고   |  REMARKS   | VARCHAR2(360) |

테이블 이름: BASKET
**장바구니**

| 순번 |  한글명  |   영문명   |  데이터타입   |
| :--: | :------: | :--------: | :-----------: |
|  1   | 고객번호 | MEMBER_NUM |  NUMBER(5,0)  |
|  2   |   번호   |    IDX     |  NUMBER(5,0)  |
|  3   | 상품코드 |    CODE    | VARCHAR2(60)  |
|  4   |  상품명  |    NAME    | VARCHAR2(60)  |
|  5   |   가격   |   PRICE    |  NUMBER(5,0)  |
|  6   |  거래처  |   MARKET   | VARCHAR2(300) |

테이블 이름: OUTCOUNTBASKET
**출고목록**

| 순번 |  한글명  |   영문명   |  데이터타입   |
| :--: | :------: | :--------: | :-----------: |
|  1   | 고객번호 | MEMBER_NUM |  NUMBER(5,0)  |
|  2   |   번호   |    IDX     |  NUMBER(5,0)  |
|  3   | 상품코드 |    CODE    | VARCHAR2(30)  |
|  4   |  상품명  |    NAME    | VARCHAR2(30)  |
|  5   |   가격   |   PRICE    |  NUMBER(5,0)  |
|  6   |  거래처  |   MARKET   | VARCHAR2(300) |

테이블 이름: INOUTCOUNT
**출입고테이블**

| 순번 |   한글명   |   영문명   |  데이터타입   |
| :--: | :--------: | :--------: | :-----------: |
|  1   |  고객번호  | MEMBER_NUM |  NUMBER(5,0)  |
|  2   |    번호    |    IDX     |  NUMBER(5,0)  |
|  3   |  상품코드  |    CODE    | VARCHAR2(30)  |
|  4   |   상품명   |    NAME    | VARCHAR2(30)  |
|  5   |   거래처   |   MARKET   | VARCHAR2(30)  |
|  6   |    가격    |   PRICE    |  NUMBER(5,0)  |
|  7   |    수량    |  QUANTITY  |  NUMBER(5,0)  |
|  8   |    날짜    |  REGDATE   | VARCHAR2(300) |
|  9   | 출입고구분 | COUNT_NUM  |  NUMBER(5,0)  |

테이블 이름: MBOARD
**1:1문의테이블**

| 순번 |  한글명  |   영문명   |   데이터타입   |
| :--: | :------: | :--------: | :------------: |
|  1   | 고객번호 | MEMBER_NUM |  NUMBER(5,0)   |
|  2   |   번호   |    IDX     |  NUMBER(5,0)   |
|  3   | 문의내용 |    CONT    | VARCHAR2(1000) |
|  4   | 문의답글 |   REPLY    | VARCHAR2(1000) |
|  5   |   날짜   |  REGDATE   |  VARCHAR2(30)  |

> 제작후기

> 향후 구현 예정
