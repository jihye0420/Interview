- **기본 SQL함수 종류**

| 숫자형 함수 | 연산 대상과 반환값이 숫자형인 함수 | ABS(), ROUND() 등 |
| --- | --- | --- |
| 문자형 함수 | 연산 대상과 반환값이 문자형인 함수 | CONCAT(), SUBSTRING() 등 |
| 날짜형 함수 | 연산 대상과 반환값이 날짜형인 함수 | SYSDATE(), YEAR() 등 |
| 형 변환 함수 | 연산 대상의 데이터 타입을 변환하는 함수 | CAST(), CONVERT() 등 |
| 기타 함수 | 흐름을 제어하는 함수 | IF(), IFNULL() 등 |
| 집계 함수 | 집계 쿼리에서 사용하는 함수 | SUM(), MAX(), AVG() 등 |
| 윈도우 함수 | 좀 더 세밀한 데이터 분석을 위한 분석 함수 | RANK(), LAG() 등 |

- **수식 연산자**

| 연산자 | 설명 | 사용 예 |
| --- | --- | --- |
| + | 더하기 | 2 + 3 → 5 |
| - | 빼기 | 3 - 2 → 1 |
| * | 곱하기 | 3 * 2 → 6 |
| / | 나누기, 몫을 반환함 | 3 / 2 → 1.5 |
| %, MOD | 나머지 | 5 % 2 → 15 </br> MOD 2 → 1 |
| DIV | 나누기, 몫에서 정수 부분만 반환함 | 3 DIV 2 → 1 |

- **숫자형 함수**

| 함수 | 반환값 | 사용 예 |
| --- | --- | --- |
| ABS(x) | x의 절댓값 | ABS(-3) → 3 |
| CEIL(x), CEILING(x) | x보다 큰 최소 정수 | CEIL(6.5) → 7 |
| FLOOR(x) | x보다 작은 최대 정수 | FLOOR(6.5) → 6 |
| EXP(x) | 자연로그의 밑 e의 x승 | EXP(2) → 7.38905609893065 |
| LN(x) | 밑이 e인 x의 로그 | LN(2) → 0.6931471805599453 |
| LOG(b, x) | 밑이 b인 x의 로그, b 생략 시 밑은 e | LOG(3, 9) → 2 |
| LOG10() | 밑이 10인 x의 로그 | LOG10(100) → 2 |
| LOG2() | 밑이 2인 x의 로그 | LOG2(8) → 3 |
| MOD(n, m) | n을 m으로 나눈 나머지 | MOD(21, 5) → 1 |
| POW(x, y), POWER(x, y) | x의 y승 | POWER(2, 3) → 8 |
| RAND([n]) | 0보다 크거나 같고 1보다 작은 난수(실수) 반환함 </br> RAND 함수를 실행할 때마다 반환되는 값(난수)은 달라지지만, 매개변수 n(생략 가능)을 명시하면 여러 번 실행해도 같은 값 반환함 | RAND() → 0.14949947330122765 |
| ROUND(x, d) | x를 소수점 이하 d 자리까지 반올림함 </br> d 생략 시 0을 적용해 정수 반환함 </br> d가 음수이면 소수점 기준 왼쪽(정수 부분)으로 기준점을 이동함 | ROUND(2.354,1) → 2.4 |
| SIGN() | 매개변수가 0보다 크면 1, 0이면 0, 0보다 작으면 -1 | SIGN(-5) → -1 |
| SQRT() | 제곱근 | SQRT(3) → 1.7320508075688772 |
| TRUNCATE(x, d) | x를 소수점 이하 d 자리에서 잘라냄 | TRUNCATE(2.354,1) → 2.3 |

- **문자형 함수**

| 함수 | 반환값 | 사용 예 |
| --- | --- | --- |
| CHAR_LENGTH(str)</br>CHARACTER_LENGTH(str) | str 문자열의 문자 개수 반환 | CHAR_LENGTH('AB') → 2 |
| LENGTH(str) | str 문자열의 바이트(Byte) 수 반환</br>한글 1글자 = 3 byte | LENGTH('AB') → 2 |
| CONCAT(s1, s2...) | s1, s2 등의 문자열을 하나로 이어 붙여서 반환 | CONCAT('A', 'B') → AB |
| CONCAT_WS(sep, s1, s2... ) | s1, s2 등의 문자열을 sep로 연결해 반환 | CONCAT_WS('-', 'A', 'B') → A-B |
| FORMAT(x, d) | 숫자 x의 정수 부분 3자리마다 콤마를 추가해 문자열로 반환</br>소수점 이하 d자리 기준으로 반올림 | FORMAT(123456.13457, 3) → 123,456.135 |
| INSTR(str, substr) | str 문자열에서 substr 문자(열)를 찾아 시작 위치 반환 | INSTR('ABC', 'C') → 3 |
| LOCATE(substr, str, pos)</br>POSITION(substr IN str) | str 문자열에서 substr 문자(열)를 찾아 시작 위치 반환, pos 입력 시 해당 위치부터 검색 시작 | LOCATE('C', 'ABCDEFG') → 3 |
| LOWER(str)</br>LCASE(str) | str 문자열을 소문자로 반환 | LOWER('ABC') → 'abc' |
| UPPER(str)</br>UCASE(str) | str 문자열을 대문자로 반환 | UPPER('abc') → 'ABC' |
| LPAD(str, len, padstr) | str 문자열을 len 길이만큼 반환하는데, 자리가 남으면 왼쪽을 padstr 문자로 채움 | LPAD('ABC', 5, '*') → '&#42;&#42;ABC' |
| RPAD(str, len, padstr) | str 문자열을 len 길이만큼 반환하는데, 자리가 남으면 오른쪽을 padstr 문자로 채움 | RPAD('ABC', 5, '*') → 'ABC&#42;&#42;' |
| LTRIM(str) | str 문자열에서 왼쪽 공백 제거 | LTRIM(' ABC ') → 'ABC ' |
| RTRIM(str) | str 문자열에서 오른쪽 공백 제거 | RTRIM(' ABC ') → ' ABC' |
| LEFT(str, len) | str 문자열을 len 길이만큼 왼쪽에서 잘라서 반환 | LEFT('ABCDE', 2) → 'AB' |
| RIGHT(str, len) | str 문자열에서 len 길이만큼 오른쪽에서 잘라서 반환 | RIGHT('ABCDE', 2) → 'DE' |
| REPEAT(str, count) | str 문자열을 count만큼 반복 | REPEAT('Ya', 3) → 'YaYaYa' |
| REPLACE(str, from_str, to_str) | str 문자열에서 from_str 문자열을 찾아 to_str로 변경 | REPLACE('NaNaNa', 'a', 'b') → 'NbNbNb' |
| REVERSE(str) | str 문자열을 거꾸로 반환 | REVERSE('abcdefg') → 'gfedcba' |
| SPACE(N) | N개의 공백 문자 반환 | SPACE(3) → ' ' |
| SUBSTR(str, pos, len)</br>SUBSTRING(str, pos, len)<br>MID(str, pos, len) | str 문자열의 pos 위치에서 len 길이만큼 문자를 잘라서 반환 | SUBSTR('ABCD', 3, 1) → 'C' |
| TRIM([{BOTH-LEADING&#124;TRAILING} [remstr] FROM] str) | str 문자열에서 remstr 문자를 앞(LEADING)이나 뒤(TRAILING) 또는 앞뒤(BOTH)에서 제거 | TRIM(LEADING 'x' FROM 'xxSQLxx') → 'SQLxx' |
| STRCMP (str1, str2) | str1과 str2 문자열을 비교해 같으면 0, str1이 str2보다 크면 1, 작으면 -1을 반환 | STRCMP('A', 'B') → -1 |
- **날짜형 함수**

| 함수 | 반환값 | 사용 예 |
| --- | --- | --- |
| CURDATE()</br>CURRENT_DATE()</br>CURRENT_DATE | 현재 날짜 반환 | CURDATE() → 2021-01-01 |
| CURTIME(),</br>CURRENT_TIME()</br>CURRENT_TIME | 현재 시각을 시:분:초 형태로 반환 | CURTIME() → 20:02:10 |
| NOW(),</br>CURRENT_TIMESTAMP()</br>CURRENT_TIMESTAMP | 현재 날짜와 시간 반환</br>쿼리 수행 시간 | NOW() → 2021-01-01 20:02:10 |
| DAYNAME (date) | date의 요일을 반환 | DAYNAME('2021-01-01') → Friday |
| DAYOFMONTH(date)</br>DAY(date) | date에서 일을 반환 | DAYOFMONTH('2021-01-02') → 2 |
| DAYOFWEEK(date) | date에서 일을 요일별 숫자로 반환(1: 일요일, 7: 토요일) | DAYOFWEEK('2021-01-02') → 7 |
| DAYOFYEAR(date) | date에서 1년 기준으로 날짜를 일수로 반환, 반환값의 범위는 1~366 | DAYOFMONTH('2021-12-31') → 365 |
| LAST_DAY(date) | date가 속한 월의 마지막 날짜 반환 | LAST_DAY('2021-01-02') → 2021-01-31 |
| YEAR(date) | date에서 연 반환 | YEAR('2021-01-02') → 2021 |
| MONTH(date) | date에서 월 반환 | MONTH('2021-02-02') → 2 |
| QUARTER(date) | date의 분기 반환 | QUARTER('2021-02-02') → 1 |
| WEEKOFYEAR(date) | date가 몇 주차인지 반환(1~53주) | WEEKOFYEAR('2021-02-22') → 8 |
| HOUR(time) | time에서 시간 반환 | HOUR('10:53:24') → 10 |
| MINUTE(time) | time에서 분 반환 | MINUTE('10:53:24') → 53 |
| SECOND(time) | time에서 초 반환 | SECOND('10:53:24') → 24 |
| DATE(expr) | expr에서 날짜 부분 반환 | DATE('2021-01-02 12:32:10') → 2021-01-02 |
| TIME(expr) | expr에서 시간 부분 반환 | TIME('2021-01-02 12:32:10') → 12:32:10 |
| DATE_ADD(date, INTERVAL expr unit)</br>ADDDATE(date, INTERVAL expr unit) | date에 expr unit을 더한 날짜 반환 | DATE_ADD('2021-01-10',INTERVAL 10 DAY) → 2021-01-20 |
| ADDDATE(expr, days) | expr에 days를 더한 날짜 반환 | ADDDATE('2021-01-10', 10) → 2021-01-20 |
| DATE_SUB(date, INTERVAL expr unit)</br>SUBDATE(date, INTERVAL expr unit) | date에 expr unit을 뺀 날짜 반환 | DATE_SUB('2021-01-10',INTERVAL 5 DAY) → 2021-01-05 |
| SUBDATE(expr, days) | expr에서 days를 뺀 날짜 반환 | SUBDATE('2021-01-10', 5) → 2021-01-05 |
| EXTRACT(unit FROM date) | date에서 unit으로 지정된 부분 반환 | EXTRACT(YEAR_MONTH FROM '2021-01-31') → 202101 |
| DATEDIFF(expr1, expr2) | expr1에서 expr2를 뺀 날짜를 일수로 반환 | DATEDIFF('2021-01-31', '2021-01-21') → 10 |
| DATE_FORMAT(date, format) | date를 format에 명시된 형태로 변환해 반환 | DATE_FORMAT('2021-01-31', %y %) → 21/01/31 |
| STR_TO_DATE(str, format) | str을 format에 맞게 날짜로 변환 | STR_TO_DATE('21,1,2021', '%d,%m,%Y') → 2021-01-21 |
| MAKEDATE(year, dayofyear) | year에 dayofyear에 해당하는 일수를 더한 날짜 반환 | MAKEDATE(2021, 100) → 2021-04-10 |
| SYSDATE() | 현재 날짜 반환</br>함수 호출 시간 | SYSDATE() → 2021-01-31 12:39:20 |
| WEEK(date, mode) | date가 몇 주차인지 반환 | YEARWEEK('2021-10-01') → 39 |
| YEARWEEK(date, mode) | date가 속한 연도와 주차 반환 | YEARWEEK('2021-10-01') → 202139 |

- **unit에 사용할 수 있는 단위**

| unit 값 | 설명 | expr 형식(사용 예) |
| --- | --- | --- |
| YEAR | 연 | INTERVAL 1 YEAR |
| MONTH | 월 | INTERVAL 1 MONTH |
| QUARTER | 분기 | INTERVAL 1 QUARTER |
| WEEK | 주 | INTERVAL 1 WEEK |
| DAY | 일 | INTERVAL 1 DAY |
| HOUR | 시 | INTERVAL 1 HOUR |
| MINUTE | 분 | INTERVAL 1 MINUTE |
| SECOND | 초 | INTERVAL 1 SECOND |
| YEAR_MONTH | 연월 | INTERVAL '1 1' YEAR_MONTH |
| DAY_HOUR | 일시 | INTERVAL '1 1' DAY_HOUR |
| DAY_MINUTE | 일시분 | INTERVAL '1 1:20' DAY_MINUTE |
| DAY_SECOND | 일시분초 | INTERVAL '1 1:20:12' DAY_SECOND |
| HOUR_MINUTE | 시분 | INTERVAL '1:20' HOUR_MINUTE |
| HOUR_SECOND | 시분초 | INTERVAL '1:20:12' HOUR_SECOND |
| MINUTE_SECOND | 분초 | INTERVAL '20:12' MINUTE_SECOND |

- **DATE_FORMAT 함수에 사용하는 주요 식별자**

| 식별자 | 설명 | 예 |
| --- | --- | --- |
| %Y | 4자리 연도 | 2000, 2021 |
| %y | 2자리 연도 | 20, 21 |
| %M | 월의 영문 표기 | January, December |
| %m | 2자리 월 | 01, 02, 12 |
| %b | 월의 축약 영문 표기 | Jan, Feb, Dec |
| %c | 숫자형 월 | 1, 2, 3, 12 |
| %d | 2자리 일 | 01, 02, 31 |
| %e | 1자리 일 | 1, 2, 31 |
| %j | 3자리 1년 기준 일수 | 001,002, 100, 365 |
| %H | 24시간 기준 시 | 00, 01,10, 17, 23 |
| %h, %I | 12시간 기준 시 | 00,01, 10, 12 |
| %p | AM(오전) 또는 PM(오후) | AM, PM |
| %i | 2자리 분 | 00, 01, 59 |
| %S, %s | 2자리 초 | 00, 01, 59 |
| %T | 24시간 기준 시:분:초 | 13:34:05 |
| %r | 12시간 기준 시:분:초 AM|PM | 01:34:05 PM |
| %W | 요일의 영문 표기 | Sunday |
| %w | 숫자 요일(0: 일요일, 1: 월요일, 6:토요일) | 6(2021-01-09일 경우) |
| %U | 00~53 형식 주차(한 주의 시작: 일요일) | 01(2021-01-03일 경우) |
| %u | 00~53 형식 주차(한 주의 시작: 월요일) | 00(2021-01-03일 경우) |
| %V | 01~53 형식 주차(한 주의 시작: 일요일) | 01(2021-01-03일 경우) |
| %v | 01~53 형식 주차(한 주의 시작: 월요일) | 53(2021-01-03일 경우) |

* **WEEK 함수에서 사용할 수 있는 mode 값**

| mode 값 | 주의 시작일 | 반환값 범위 | 1월 1일을 포함한 주차 |
| --- | --- | --- | --- |
| 0 | 일요일 | 0~53 | 일요일 포함 |
| 1 | 월요일 | 0~53 | 4일 이상 포함 |
| 2 | 일요일 | 1~53 | 일요일 포함 |
| 3 | 월요일 | 1~53 | 4일 이상 포함 |
| 4 | 일요일 | 0~53 | 4일 이상 포함 |
| 5 | 월요일 | 0~53 | 월요일 포함 |
| 6 | 일요일 | 1~53 | 4일 이상 포함 |
| 7 | 월요일 | 1~53 | 월요일 포함 |

```sql
# 아래와 같이 출력
SELECT 7 % 2, 7 MOD 2, 7 / 2, 7 DIV 2; 
SELECT CEIL(4.5), FLOOR(4.5); # 5, 4
SELECT LN(100), LOG(100), LOG(10, 100), LOG10(100);
SELECT MOD(5, 4), 5 MOD 4, 5 % 4;

SELECT DATE_ADD('2021-01-20', INTERVAL 5 DAY) DATEADD,
       ADDDATE('2021-01-20', INTERVAL 5 DAY) ADD_DATE1,
       ADDDATE('2021-01-20', 5 ) ADD_DATE2;

SELECT DATE_FORMAT('2021-01-20 13:42:54', '%d-%b-%Y') Fmt1,
       DATE_FORMAT('2021-02-20 13:42:54', '%U %W %j') Fmt2;

SELECT WEEK('2021-01-03', 0) MODE0,
       WEEK('2021-01-03', 1) MODE1,
       WEEK('2021-01-03', 2) MODE2,
       WEEK('2021-01-03', 3) MODE3,
       WEEK('2021-01-03', 4) MODE4,
       WEEK('2021-01-03', 5) MODE5,
       WEEK('2021-01-03', 6) MODE6,
       WEEK('2021-01-03', 7) MODE7;
```