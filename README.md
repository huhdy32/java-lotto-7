# java-lotto-precourse

---

## 로또 발매기 프로젝트

- 입력된 금액만큼 자동으로 로또를 선택하며, 각 로또의 번호를 출력한다.
- 입력된 로또 당첨 번호와 보너스 번호를 위에서 구매한 로또번호를 비교하여, 사용된 금액 대비 수익률을 계산 및 출력한다.

---

## 구현 목록

### 0. 통합 기능

- [ ] 기능간 연결
- [ ] 오입력 부터 재입력

---

### 1. 주요 기능

- [X] **(1) 로또 발행 기능**
  - [X] 하나의 로또
    - [X] 총 6개의 당첨 번호
    - [X] 각 숫자는 1 ~ 45
    - [X] 번호 중복 불가
  - [X] 각 로또를 생성할 때, 로또 번호를 랜덤으로 생성 기능
  - [X] 입력된 금액에 대해 1000원 단위로 로또를 발행 기능

- [X] **(2) 로또 저장 기능** 
  - [X] 발급된 로또들 저장
  - [X] 발급된 로또들 조회

- [X] **(3) 로또 번호 비교 기능**
  - [X] 당첨번호와 보너스 번호로 각 로또를 비교하여 몇등인지 계산 기능

| 개발상태 | 등수  | 조건                       | 금액            |
|-----|-----|--------------------------|---------------|
| ✅   | 1등  | 6개 번호 모두 일치              | 2,000,000,000 |
| ✅   | 2등  | 5개 번호 일치 `AND` 보너스 번호 일치 | 30,000,000    |
| ✅   | 3등  | 5개 번호 일치                 | 1,500,000     |
| ✅   | 4등  | 4개 번호 일치                 | 50,000        |
| ✅   | 5등  | 3개 번호 일치                 | 5,000         |

- [X] **(4) 수익률 계산 기능**
  - [X] 당첨금액 종합 기능
  - [X] 입력 금액과 총 당첨 금액을 비교해 수익률 계산 기능

---

### 2. UI 기능
- **출력**
  - [X] **(1) 구매 금액 안내 출력 기능**
    - `구입금액을 입력해 주세요.\n`
  - [X] **(2) 로또 발행 목록 출력 기능**
    - `{}개를 구매했습니다.\n`
    - `[number, number, number, number, number, number]\n`
    - `[number, number, number, number, number, number]\n`
  - [X] **(3) 당첨 번호 안내 출력 기능**
    - `당첨 번호를 입력해 주세요.\n`
  - [X] **(4) 보너스 번호 입력 안내 출력 기능**
    - `보너스 번호를 입력해 주세요.\n`
  - [X] **(5) 결과 출력 기능**
    - [ ] 수익률 출력 기능
    - `총 수익률은 XX.X%입니다.\n`
    - [X] 당첨 통계 출력 기능
```
당첨 통계\n
---\n
3개 일치 (5,000원) - ${}개\n
4개 일치 (50,000원) - ${}개\n
5개 일치 (1,500,000원) - ${}개\n
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개\n
6개 일치 (2`,000,000,000원) - 0개\n
```

- **입력**
  - [ ] **(1) 구입 금액 입력**
    - 1000원 단위
    - ex) `52000`
  - [ ] **(2) 당첨 번호 입력**
    - 중복 불가
    - 1 ~ 45
    - 6자리 숫자
    - ex) `1, 2, 3, 4, 5, 6`
  - [ ] **(3) 보너스 숫자 입력**
    - 중복 불가
    - 1 ~ 45
    - ex) `44`

---

### 3. 예외 처리

- [ ] 예외 발생 시 에러메시지 출력

- [X] 로또 숫자가 중복된 경우
- [X] 로또 숫자가 6개가 아닌 경우
- [X] 로또 1 ~ 45 가 아닌 경우

---