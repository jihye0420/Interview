# 1장 데이터베이스와 SQL

- **데이터베이스** : 데이터의 집합
- **데이터베이스 & DBMS**
    - **DBMS** : 데이터베이스를 관리하고 운영하는 소프트웨어, 파일의 단점을 보완하여 대량의 데이터를 효율적으로 관리 & 운영하기 위해서 등장
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/0519b017-c484-4f29-bdad-8b43a8399377/Untitled.png)
        
    - **SQL** : DBMS에 데이터를 구축, 관리, 활용하기 위해서 사용되는 언어, DBMS를 통해 중요한 정보들을 입력, 관리, 추출 가능
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/b85f1e58-bf19-43f6-983e-251933ee2d90/Untitled.png)
        
    - **DBMS 분류** : 계층형, 망형, **관계형**, 객체지향형, 객체지향형, 객체관계형
        - 계층형 DBMS : 트리 형태, 처음 구성 이후 변경이 어려움이 단점 ⇒ 사용 X
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/a8d573c7-27a4-475b-93b5-e743ea07ea55/Untitled.png)
            
        - 망형 DBMS : 계층형 보완, 모든 구조를 이해해야지만 프로그램 작성 가능 단점 ⇒ 사용 X
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/30d2b8a1-b0b2-45ce-be0b-19431c5f0d9e/Untitled.png)
            
        - **관계형 DBMS == RDBMS(Relational Database Management System) : 테이블(열(column), 행(row)), ex) MySQL**
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/aff6a7c9-44a3-4140-a35c-a6cbc93f1b57/Untitled.png)
            
- **DBMS에서 사용되는 언어: SQL**
    - SQL : 관계형 데이터베이스에서 사용되는 언어
        - 표준 SQL : 국제표준화기구에서 SQL에 대한 표준을 정해서 발표
        - DBMS 각 회사는 자신의 제품의 특성을 반영한 변형된 SQL을 사용
            - 오라클 ⇒ PL/SQL
            - SQL 서버 ⇒ T-SQL
            - **MySQL ⇒ SQL**
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/35a7bcc7-c843-4751-8d64-bcb54fea2ebe/87fec5d5-ebaa-4b44-95a4-01d224628b7c/Untitled.png)
            

---

요약

---

실습