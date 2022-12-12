### AI 프로젝트 스마트 팩토리과 A반 8조
---------------
###  facerecognition
실시간으로 저장된 사람의 얼굴을 인식하는 프로그램

-----------------------------------------------------
### 작품소개
facerecognition을 통해서 실시간으로 사진을 저장합니다.저장된 사진은 눈,코,입의 좌표를 기억하고 실시간으로 전송되는 영상의 사람과 비교합니다.
처음 사람의 얼굴이 인식되면 unknown으로 저장되고 저장이된 사람의 좌표를 기억하고 그 사람의 얼굴을 person_##으로 인식합니다.
저장된 사람의 사진은 montage형식으로 보기 쉽게 따로 전송이되며 unknown 사진들 또한 따로 저장이 됩니다.
저장된 person 명을 move함수를 통해서 임의로 변경을 하면 실시간으로 person의 이름이 변경된 이름으로 바뀌어서 인식합니다.

--------------------------------------------------
### 작품설계의 목적 및 결과

저희 조는 cctv에서 사람을 찾을때 영상만보고 사람을 찾는게 힘들고 불편하다고 생각했습니다.그래서 AI가 저장된 사람의 얼굴을 저장하고 있고 따로 분류를
하면 사람을 찾을때 더 편하지않을까 라는 생각에서 프로젝트를 시작하게되었습니다. 처음에는 저희가 할수 없는 영역이라고 생각을 했지만 난이도를 수정함에 따라서 학교내 cctv라는 제한된 영역에서라도 사용할수 있지않을까 하는 생각하게 되었고 그 결과로 저희반 사람의 얼굴이라도 인식을 하는 프로그램을 만들고자 노력했습니다. 그 결과로 디렉토리의 명을 바꿀수 있는 방법을 찾았고 그 값을 저희 조원의 이름을 넣어 확임함으로서 소수의 인원을 인식할수있다는 결과를 만들어냈습니다. 저희 조는 큰 목표에 도달하기위한 여러번의 작은 목표중 하나를 달성했다고 생각합니다.

------------------------
### 초기 실행결과 및 문제점

![제목 없음](https://user-images.githubusercontent.com/111891607/207052603-b887b489-0969-4c50-bd66-9abe0d25541f.gif)

실행결과 김성훈 학우를 인식한것을  확인할수 있는데, 2명이상의 얼굴이 들어오게 되면,한명 의 얼굴을 인식 못하거나, 눈,코,입의 위치만 얼추 비슷하면 모두 김성훈으로 인식하는 문제점을 발견했습니다.한번 훈련된 얼굴을 정확하게 인식하고, 두 명 이상의 얼굴이 인식되어도 기존의 Unknown으로 인식하지 않도록 개선하려했습니다.

-------------------------
### 인식과정

![1](https://user-images.githubusercontent.com/111891607/207052925-ffba5416-2fcf-4252-8994-4b0702579dbd.gif)
Unknown >>person인식    Person디렉토리 변환  Move result/person_00(디렉토리 이름)result/Mingi ----> 디렉토리 이름을 원하는 이름으로 변경

--------------

### 사진저장과정

![2](https://user-images.githubusercontent.com/111891607/207053331-3361f71c-19eb-4dcf-a3f2-8c6687805162.gif)

--------------
### Montage 파일 

![3](https://user-images.githubusercontent.com/111891607/207053846-d38cb24a-22c2-418c-8e7e-27fbc7b25dde.gif)

각 디렉토리 파일에 저장된 얼굴을 보기쉽게 몽타주형식으로 변환한 파일 
이 부분은 범죄현장에 있는 CCTV속  범인의 얼굴이 정확하게 나오지 않을때, 몽타주 파일을 생성해 범인의 몽타주를  목격자 진술보다 보다 정확하게 그려낼수 있을거 같습니다.

--------------------

### 실행 영상



https://user-images.githubusercontent.com/111891607/207061427-d2bcf00b-15ab-4317-aca3-66c988d04dc3.mp4




-------------------

### 실행 결과
라즈베리파이를 이용하여 브레드보드에 램프1,2를 각각 8번핀,9번핀에 연결후 Mingi가 인식되었을때 8번핀에 연결한 램프가 불이켜지고  Sunghun 이 인식되었을때 8번핀 램프 불이꺼지고 9번핀 램프불이 켜집니다.
그리고 (Unknown 또는 person)  즉 학습되지않은 얼굴이 인식되는경우에 8,9번핀 램프에 불이 모두꺼지게 됩니다.

--------------------











