# Account

## 프로젝트 소개
Java와 Spring Boot를 이용한 계좌 관리 시스템을 만드는 프로젝트 과제입니다. 

## ⏱️ 개발 기간
* 2022.11.27 - 2022.12.03 <br>

## ⚒️ 개발 환경 
* Java 8 <br>
* IDE : IntelliJ 2022.02 <br>
* Framework: Springboot(3.0.0)<br>
* Database : H2 <br>
* ORM : Spring data JPA <br>

## 🖥️ 주요기능 

### Custom Exception Handling - [상세정보 - WIKI](https://github.com/heyazoo1007/Account/wiki/%EC%A3%BC%EC%9A%94-%EA%B8%B0%EB%8A%A5-%EC%86%8C%EA%B0%9C(Exception))
* 예외처리는 @ExceptionHandler를 이용해 구현 
* 커스텀 예외처리 Enum(ErrorCode)을 이용해서 구현

### 💰 계좌 관련 API - [상세정보 - WIKI](https://github.com/heyazoo1007/Account/wiki/%EC%A3%BC%EC%9A%94-%EA%B8%B0%EB%8A%A5-%EC%86%8C%EA%B0%9C(Account))

계좌 생성 
* 유일한 10자리 계좌번호 랜덤으로 생성
* 사용자 검증 
* 사용자가 소유한 계좌 수에 따른 검증 

계좌 해지 
* 사용자 없는 경우 검증 
* 사용자와 계좌 소유주가 다른 경우 검증
* 계좌가 이미 해지 상태인 경우 검증 
* 잔액이 있는 경우 검증 

계좌 확인 
* 사용자 없는 경우 검증 <br>

### 💸 거래 관련 API - [상세정보 - WIKI](https://github.com/heyazoo1007/Account/wiki/%EC%A3%BC%EC%9A%94-%EA%B8%B0%EB%8A%A5-%EC%86%8C%EA%B0%9C(Transaction))
잔액 사용 
* 사용자 없는 경우 검증 
* 사용자와 계좌 소유주가 다른 경우 검증
* 계좌가 이미 해지 상태인 경우 검증 
* 거래 금액이 잔액보다 큰 경우 
* 거래금액이 너무 작거나 큰 경우 검증 

잔액 사용 취소
* 원거래 금액과 취소 금액이 다른 경우 검증(부분 취소 불가능)
* 트랜잭션이 해당 계좌의 거래가 아닌 경우 검증 

거래 확인
* 해당 트랜잭션이 존재하지 않는 경우 실패 응답 
* 성공 거래와 실패 거래 모두 조회 가능 

