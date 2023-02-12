# java-racingcar

자동차 경주 미션 저장소

## 📝 기능 목록

### UI 기능

- 입력받는 기능
    - [x] 경주할 자동차의 이름을 한줄로 입력받아 컴마 단위로 파싱하는 기능
    - [x] 시도할 횟수를 입력받는 기능
        - 자연수가 아니면 `IllegalArgumentException`을 발생시킨다.
- 출력하는 기능
    - [x] 실행 결과를 출력하는 기능
    - [x] 최종 결과를 출력하는 기능

### 도메인 기능

- 자동차
    - [x] 이름을 전달받아 자동차를 생성하는 기능
        - null이면 `IllegalArgumentException`을 발생시킨다.
        - 5자 초과면 `IllegalArgumentException`을 발생시킨다.
        - 빈 문자열이면 `IllegalArgumentException`을 발생시킨다.
    - [x] 자동차를 전진하는 기능
        - 4 이상일 경우 전진하고, 3 이하면 멈춘다.
- 경주참여 자동차들
    - [x] 전달받은 이름들로 자동차 여러 대를 생성하는 기능
        - 이름의 개수가 1개인 경우, `IllegalArgumentException`을 발생시킨다.
        - 중복된 이름이 존재하는 경우 `IllegalArgumentException`을 발생시킨다.
    - [x] 참여 자동차들을 1회 경주시키는 기능
    - [x] 자동차 간의 위치를 비교해 우승자 이름을 산출하는 기능
- 랜덤 숫자 생성기
    - [x] 특정 범위의 랜덤 숫자를 생성하는 기능

### UI-도메인 연결 기능 (컨트롤러)

- [x] 시도할 횟수를 전달받아 그 횟수만큼 경주를 진행하는 기능
- [x] 자동차의 정보를 전달받아 이름과 위치를 뷰에 넘겨주는 기능
- [x] 최종 결과를 넘겨받아 뷰에 넘겨주는 기능

## ♻️ 2단계 리팩터링 검토 목록

- 미션 요구사항에 따라 MVC 패턴 기반으로 리팩터링 진행
- [x] 패키지명 및 패키지 구조 수정
- [x] 각종 책임 분리에 대하여 클래스 설계 검토
- [x] 1단계 피드백 기반으로 비효율적인 코드 수정
- [ ] 상수 처리
- [ ] final 처리가 필요한 변수 검토
- [ ] 테스트 코드 수정
    - 중복 줄이고 테스트 픽스처 생성하기
    - 원활한 리팩터링을 위해 프로덕션 코드에 영향받지 않도록 하기
    - 메시지 비교를 이용한 더 정확한 예외 테스트 고민하기
- [ ] 클린 코드를 위한 개선 검토
