# 3주차 필기


https://github.com/OppSpark/2023_2_problem/blob/main/3week/HW/20230912.ipynb




<aside>
💻 그래프 책 p.61

</aside>

그래프 

- 그래프는 정점(Vertex) 와 간선(Edge)의 집합으로 하나의 간선은 2개의 정점을 연결
- 무방향 그래프와 방향 그래프로 나뉜다.

정점 a 와 b를 연결하는 간선 : (a,b)

정점 a에서 b로 간선의 방향이 있는 경우 : <a,b>

차수

- 정점에서 인접한 정점의 수
    - 방향 그래프 점의 차수는 진입 차수와 진출 차수로 구분함
    

경로(path)

- 시작점 u 부터 도착점 v 까지 정점을 나열하여 표현

단순 경로

- 경로 상의 정점들이 모두  다른 경로

사이클

- 시작점과 도착점이 같은 단순 경로

연결 성분  // 책 p.62

- 그래프에서 정점들이 서로 연결되어 있는 부분


연결 성분은 3개

가중치

- 간선에 가중치가 부여된 그래프
    - 가중치 : 거리 ,시간 음수 일 수 있음

<aside>
💻 그래프 자료 구조

</aside>

그래프 자료구조

- 인접리스트
- 인접 행렬

희소 그래프 

- 대부분 정점의 평균 차수가 작음
- 간선의 수는 최대 간선 수인 n(n-1)/2 보다 훨씬 작으므로 인접리스트가 적합

조밀 그래프

- 간선의 수가 최대 간선수에 근접한 그래프

<aside>
💻 그래프 탐색 , DFS , BFS

</aside>

Code    dfs.py

깊이 우선 탐색 (DFS)

- DFS 의 탐색 시간  O(n+m)
- n = 정점 ,  m = 간선

Code   bfs.py
너비 우선 탐색 (BFS)

- BFS 의 탐색 시간O(n + m)
- n = 정점 ,  m = 간선

<aside>
💻 위상 정렬

</aside>

위상 정렬

- 사이클이 없는 방향 그래프에서 정점을 선형 순서로 나열하는 것

위상 정렬 찾기

- 순방향 방법
    - 진입 차수가 0인 정점 v 로 부터 시작해 v를 출력하고 v를 그래프에서 제거하는 과정을 반복
- 역방향 방법
    - 진출 차수가 0인 정점 v 를 출력하고 v를 그래프에서 제거하는 과정을 반복하여 얻은 출력 리스트를 역순으로 만들어 결과를 얻음
    