-----
### 의사컬럼 (Pseudo-column)
-----
1. 테이블의 컬럼처럼 동작하지만, 실제로 테이블에 저장되지 않는 컬럼
2. NEXTVAL, CURRVAL : Sequence에서 사용
3. ROWNUM, ROWID
   - ROWNUM : 쿼리에서 반환되는 각 로우들에 대한 순서 값을 나타내는 의사컬럼
   - ROWID : 테이블에 저장된 각 ROW가 저장된 주소 값을 가리키는 의사컬럼 (각 ROW를 식별하는 값으로 유일한 값을 가짐)
   - B-Tree 인덱스는 테이블에서 인덱스 키로 잡혀있는 컬럼과 해당 테이블 로우를 찾아가기 위한 주소 정보 저장하는 것이 ROWID
```sql
SELECT ROWNUM, ROWID, EMPNO
FROM EMP;
```