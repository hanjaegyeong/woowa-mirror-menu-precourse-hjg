## 구현할 기능 목록

**요구사항**

- 평일 식사 카테고리, 메뉴 랜덤 추천
- 메뉴 추천 완료 시 프로그램이 종료
- 한 주에 같은 카테고리는 최대 2회까지만 추천
- 한 주에 한 코치 중복메뉴 추천x

**입력 및 검증**

- 코치 이름 입력
    - `,` 로 구분해서 입력
    - 각 코치의 이름은 최소 2글자, 최대 4글자
    - 최소 2명, 최대 5명
- 각 코치가 못 먹는 메뉴 입력
    - `,` 로 구분해서 입력
    - 각 코치 최소 0개, 최대 2개의 못 먹는 메뉴 존재
        - 먹지 못하는 메뉴가 없으면 빈 값을 입력
        - 추천 못하는 경우는 없음

**출력**

- 구분, 카테고리, 각 코치별 메뉴 출력
- 구분 출력
    - `[ 구분 | 월요일 | 화요일 | 수요일 | 목요일 | 금요일 ]`
    - 단순 상수 집합
- 카테고리 출력
    - `[ 카테고리 | 한식 | 한식 | 일식 | 중식 | 아시안 ]`
    - 랜덤 로직 처리 결과 출력
- 각 코치별 메뉴 출력
    - `[ 토미 | 쌈밥 | 김치찌개 | 미소시루 | 짜장면 | 팟타이 ]`
- 마지막 문구 출력
    - `추천을 완료했습니다.`

**예외처리**
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException를 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.