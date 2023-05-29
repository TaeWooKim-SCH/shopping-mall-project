[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fzop1234%2Ffe-sprint-coz-shopping&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CONTRIBUTORS&edge_flat=false)](https://hits.seeyoufarm.com)

# 쇼핑몰 프로젝트
코드스테이츠에서 진행된 솔로 프로젝트입니다. 주어진 디자인으로 쇼핑몰을 만드는 프로젝트입니다.

## Stack
<img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=Javascript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/> <img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/> <br/>

- ```CSS```: 개발 시간의 효율성을 늘리기 위해 테일윈드를 사용했습니다. 또한 가독성을 높이기 위해 테일윈드 스타일드 컴포넌트도 함께 사용했습니다.

### 설계
깃허브 프로젝트에서 스크럼을 이용해 플래닝을 했습니다.
1. 메인 페이지에서 Route를 통해 페이지 별로 다른 경로로 이동하도록 설정
2. 공통적으로 쓰일 Navbar, Card, Filter, Modal, Footer은 각각 컴포넌트로 만들어 사용
3. 메인 페이지, 제품 목록 페이지, 북마크 목록 페이지 총 3개의 페이지를 각각 컴포넌트로 만듦
4. 북마크 목록을 저장하기 위해 쓰일 저장소는 로컬 스토리지 사용. 추후 DB 또는 서버로 구현할 계획 있음

## 문제 해결 과정
### 😁 무한 스크롤
먼저 데이터는 코드스테이츠에서 제공한 상품 목록 API를 사용했습니다. 
하지만 API를 불러올때마다 순서가 랜덤으로 바뀌고 페이지 구분이 안되어 있는 API였습니다.
따라서 순서 보장이 되지 않는다는 문제점과 직접 데이터를 나누는 과정이 필요했습니다.
두 가지 로직을 생각했습니다.
1. 데이터를 10개씩 API에서 불러와서 보여줍니다. -> 순서 보장이 안되기 때문에 중복 데이터 발생 -> 중복 데이터 처리 -> 스크롤마다 데이터 개수가 천차만별일 수 있는 문제점
2. 처음에 데이터 100개를 모두 받아와서 직접 20개씩 데이터를 잘라줘서 구현 -> 결국 처음 렌더될 때 모든 데이터를 불러오기 때문에 그렇게 효율적이지는 않습니다. 
위 두 가지 방법 중 1번은 데이터가 아예 받아와지지 않을 경우도 생기기 때문에 비효율적이더라도 무한 스크롤 기능 구현에 집중을 하기 위해 2번 방법을 선택했습니다.


## 프로젝트 결과
![image](https://github.com/zop1234/fe-sprint-coz-shopping/assets/124567984/4e1c412e-154f-4a79-b819-3e142ae0ee67)
![image](https://github.com/zop1234/fe-sprint-coz-shopping/assets/124567984/2e49fe4a-ceae-4582-8542-c48c694a4108)
![image](https://github.com/zop1234/fe-sprint-coz-shopping/assets/124567984/c9c8e62c-e1f9-4977-a1df-26064c929c70)
