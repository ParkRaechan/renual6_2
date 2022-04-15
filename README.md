# 리뉴얼 6조 2대팀

## 주제 - 멀티키오스크(세탁,아이스크림주문)

[팀플 기초 작성 노션_링크](https://www.notion.so/65eba034e61c4cfabff76e16270f2340)

### 진행단계
1. 주제선정 브레인 스토밍
2. 주제 선정과 취합
3. 주제에 맞는기능 생각하기
4. 데이터베이스(db) 설계
5. 에프엑스(fx) 설계
6. 컨트롤(java) 설계
7. fx 기초 제작
8. 코드작성 1
9. 중간점검
10. 코드작성 2
11. 오류검출테스트
12. 최종점검









###1. 주제선정 브레인 스토밍
![팀플 re6_2 기초2](https://user-images.githubusercontent.com/100547978/163544146-cf73d27e-3582-48d8-ad2c-a472da80c302.jpg)












기능-세탁기,건조기이용후 아이스크림할인


- 간단기능
    - 세탁,건조 [ 회원 비회원 ]
        - 세탁종류 선택
            - 중형 [온도,세기]
                - 세탁기번호선택
                    - 30분지난후 다시 이용가능
            - 대형 [온도,세기]
                - 세탁기번호선택
                    - 20분지난후 다시 이용가능
        - 건조
            - 건조기선택
                - 중형 [ 온도 ]
                    - 건조기 번호선택
                        - 30분지난후 다시 이용가능
                - 대형 [ 온도 ]
                    - 건조기 번호선택
                        - 20분지난후 다시 이용가능
    
    (전부 사용하고 있다면 각각 전부사용중 이라고 뜸)
    
    ---
    
    - 아이스크림주문
        - 상품목록
            - 장바구니
        - 결제창
            - 쿠폰입력 [ 있음 없음 ]
            - 카드결제 | 현금결제
    
    ---
    
    - 관리자페이지
        - 기계관리
            - 제품추가 버튼
                - 카테고리 번호:
                    - 000
                        
                        1자리 a[세탁기], b[건조기]
                        
                        2자리 1[대형] 2[주형]
                        
                        3자리 기계순서
                        
                - 카테고리:
                - 가격:
            - 테이블뷰클릭
                - 상세보기 페이지
                    - 가격조절
                    - 세제추가
            - 뒤로가기버튼
        - 제품관리
            - 제품 상세보기
                - 재고채워넣기
            - 제품추가 버튼
        - 매출통계보기
    - 큰틀설계 예시 그림[ 관리자페이지 x ]
        
      
- DB
    - 기계 machine
        - 기계번호 [ 자동번호 ] mnum
        - 현존세재량 mamount
        - 휴대폰번호 mphone
        - 온도 mtemperature
        - 세기 mdegree
        - 기계시작시간 mtime
    - 제품 product
        - 제품번호 [ 자동번호 ] pnum
        - 재고 pinventory
    - 매출 **sales**
        - 매출번호 [ 자동번호 ] snum
        - 일자 sdate
        - 카테고리번호 [ FK ] cnum
        - 가격 sprice
    - 카테고리 category
        - 카테고리번호 [ 자동번호 ] [pk] cnum
        - 기계 번호 [ FK ] mnum
        - 제품 번호 [ FK ] pnum
        - 카테고리(기계/제품) 이름 cname
        - 가격 cprice
- DB그림예시
    
    

## 일정(4/12~4/26)

- 일정 토글
    - 12일
        - 아이디어회의
        - 큰틀 일정작성
    - 13일
        - 아이디어회의
        - 큰틀 일정작성
        - 기능별 연관도 그림판 설계 (?간단설계)
        - DB설계
    - 14일
        - 프론트설계 및 java
    - 15일
        - java이어서 and 최종설계(역할분담)
    - 16일 주말
        - ㅁ
    - 17일 주말
        - ㅁ
    - 18일
        - ㅁ
    - 19일
        - ㅁ
    - 20일
        - ㅁ
    - 21일
        - ㅁ
    - 22일
        - ㅁ
    - 23일 주말
        - ㅁ
    - 24일 주말
        - ㅁ
    - 25일
        - 테스트
    - 26일
        - 테스트
        
