## 🔆문제 요약

- 입력
    - N : 볼링공의 개수
    - M : 공의 최대 무게
- 출력
    - 두 사람이 볼링공을 고르는 경우의 수

## 🔆예외 사항

- 입력값
    - N은 1이상 1000이하 자연수
    - M은 1이상 10이하 자연수
    - 첫째줄: N과 M은 공백으로 구분되어 입력 받음
        - 2개가 맞는지
    - 둘째줄: M이하 무게의 N개의 볼링공 무게를 공백으로 분리하여 입력받음
        - M개가 맞는지
- 각 볼링공은 무게가 적혀있고, 공의 번호는 1번부터 순서대로 부여 됨
- 같은 무게의 공이 여러 개 있을 수 있지만, 서로 다른 공으로 간주함

## 🔆기능 설명

- 상수
    - `N_MIN`, `N_MAX` : N 최솟값, 최댓값
    - `M_MIN`, `M_MAX` : M 최솟값, 최댓값
- `inputValue()` : 입력받기
    - 값을 입력받기
- `inputNM()` : NM 입력 받기
- `inputBallList()` : 무게가 M이하인 N개의 볼링공 개수를 저장
- `checkValueMinMax_True(value, valueMin, valueMax)` : 최솟값, 최댓값 만족
- `checkAlpha_True(value)` : 리스트 내 문자열이 문자인가
- `find_combination(`) : 조합 찾기
    - `ball_combination_list` : 조합 리스트