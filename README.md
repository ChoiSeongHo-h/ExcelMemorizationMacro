# ExcelMemorizationMacro
## 스토리
- 군대에서.... 영어공부와 변리사 시험 준비를 하며 만들었다.
## 기능
- 우선순위가 부여되는 암기장
- 나온 단어가 계속 출현하지 않음
- 잘 아는 단어는 적은 빈도로 출현함
- 모르는 단어는 잦은 빈도로 출현함
## 사용 예시
### 1. 단어의 등록
- ![qa](https://user-images.githubusercontent.com/72921481/214938195-2f2d57bb-e406-438f-a6b3-918e730c01ad.png)
- 외울 단어와 뜻을 적는다.
  - 둘 모두 기재되어있어야 한다.
### 2. 단어 순위 부여
- ![order](https://user-images.githubusercontent.com/72921481/214938200-7b8c44c4-fb6e-4f6e-8b1f-3576b65c5031.png)
- `순위 부여`를 누르자 모두 0순위가 된 상태
- 또한 각 단어는 번호를 가지게 되었다.
- 한편 현재 출현한 단어는 `사과`, 사과의 선택번호는 1번이고 이를 번호로 찾을 수 있다.
- 뜻은 조그만하게(안보이게) 표시하였다.
### 3-1. 알아요
- ![know](https://user-images.githubusercontent.com/72921481/214938202-1d865a73-e53d-488f-b676-635ed906aa2d.png)
- 이전에 `오렌지`를 `알아요` 한 상태.
- 알아요를 눌렀다면 +5만큼 후순위로 밀려난다.
  - 저 칸은 수정할 수 있다. ex 3
- `오렌지`는 5순위가 된 것을 확인할 수 있다.
- 5개의 0순위 선택풀에서 현재는 최우선순위 0순위가 4개뿐이므로 선택풀이 4개가 되었다.
  - 즉 4개중에서만 선택된다.
- 한편, `Mask RCNN`은 0순위(최우선순위)라서 그 중에서 랜덤으로 선택되었다.
### 3-2. 몰라요
- ![dont](https://user-images.githubusercontent.com/72921481/214938203-753f3630-3ca2-49ef-9160-f34d6d774e18.png)
- 이전에 'Mask RCNN` 을 `몰라요` 한 상태.
- 1순위만큼 후순위로 밀려난다.
- 'Mask RCNN...`이 0순위에서 1순위로 밀려났다.
- 한편, `2+2`는 0순위(최우선순위)라서 그 중에서 랜덤으로 선택되었다.
## 그 외
- 중복검사는 의미의 중복을 검사하는 것이 아니라 단어의 중복을 검사
- 실행취소는 이전에 잘못클릭되어 잘못 점수 메겨진것을 실행취소한다.
- 20번 클릭(알아요 or 몰라요)마다 자동 저장된다.
- 잘 알아요는 굉장히 큰 순위가 부여되어서 더이상 출현하지 않게된다.
## 사용자가 수정가능한 셀
- `+ n 순위 후배치 셀`
- `n 회 클릭됨 셀`
- 단어와 그 의미 셀
