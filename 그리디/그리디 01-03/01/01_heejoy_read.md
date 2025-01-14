### 🔆 **문제 간단 요약**

<aside>
💡 N명의 모험가가 있는 마을에서 각 모험가에 대해 공포도 X를 측정한다. 모험가의 안전을 위해 공포도가 X인 모험가는 X명 이상으로 이루어진 모험가 그룹에 참여해야 모험을 떠날 수 있다. N명의 모험가의 각 공포도를 알 때, 만들 수 있는 모험가 그룹 수의 최댓값을 구해보자.

</aside>

1. 입력
    1. 모험가 N명
    2. N명의 모험가의 각 공포도
2. 출력
    1. 나올 수 있는 모험가 그룹의 최댓값
3. 반드시 모든 모험가를 그룹에 넣을 필요는 없음

### 🔆예외 사항

1. 모험가의 수는 1이상 100,000이하임
2. 각 모험가의 공포도 값은 N이하의 자연수임
3. 공포도는 한 줄로 입력받으며 공백으로 구분함

### 🔆필요한 기능2

1. **필요한 값을 입력받는 함수: `inputValue()`**
    1. 모험가의 수: N
        
        → 1(min)이상 100,000(max)이하인지 확인 (상수로 지정)
        
    2. 각 모험가의 공포도를 저장할 리스트: fear_list
2. **입력한 공포도의 유효성 검사하는 함수 : `checkInputValue(N, fear_list)`**
    1. 1이상의 정수인가→ 0과 공백 등의 입력은 재입력
    2. 공포도의 값이 N이하인지
3. **모험가들의 그룹을 만드는 함수 : `groupingAdventurers(fear_list)`**
    1. 내림차순 정렬
    2. 가장큰 수를 기준으로 그룹핑 : group_list
        1. fear_list를 큰 수를 차례로 삭제하는 대로 저장 f_list
        2. 가장 큰 수인 첫번째 원소를 저장 : n
        3. 큰 수의 길이만큼 그룹핑 : group
        4. 그룹핑한 길이만큼 리스트 자르기 (새로운 f_list가 됨)

1. **만든 그룹의 개수가 최댓값인지 검사하는 함수 : `checkGroupNumMax(group_list)`**
    1. group_list의 길이 : groupNum
    2. maxGroupNum
        1. None인 경우 초깃값이므로 검사하지 않고 groupNum을 저장함
        2. 이후 groupNum과 비교하여 큰 값 저장