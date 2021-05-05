https://github.com/cpu500m/SE_EngineeringAssignment2
___
# **소프트웨어공학 과제2**
# **목표 : github에서 다른사람들과 소스 공유를 하고, git을 통하여 소스의 버전관리, 소스작성과정에서의 협업을 익히기 위함.(아래 두꺼운글씨로 작성한 부분이 가상의 시나리오입니다.)** 
## **우선 작업공간인 폴더를 git의 관리하에 둬야함.**

![init과 config](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/init%EA%B3%BC%20config%EB%A1%9C%20%EB%93%B1%EB%A1%9D..PNG?raw=true)

### 이때 사용된 명령어 :
* [init](#init) : 현재 작업중인 폴더가 git의 관리하에 있게 함.
#### 사용법 :
```
git의 관리 하에 둘 폴더 내에 들어가서 
    git init
```
<br>

* config : 본인의 메일과 이름등을 출력할 수 있는 명령어. 
    > --global:  유저이름이나 이메일등 작성자의 정보를 저장.
 ### 사용법 :
 ```
 메일 등록 : git config --global user.email "유저이메일"
 이름 출력 : git config user.name
 ```
  ### 메일, 이름 출력 예시:
  ![config를 통한 출력](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/config%EB%A1%9C%20%EC%9D%B4%EB%A6%84,%EB%A9%94%EC%9D%BC%ED%99%95%EC%9D%B8.PNG?raw=true)
  <br>

## **관리하에 둔 폴더내에서 작업을 어느정도 진행했다면 , 현재상태를 언제든 꺼낼 수 있는 타임캡슐같은 공간에 저장하기 위한 명령어 사용.**
![status](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/status%20%EC%B2%AB%EB%B2%88%EC%A7%B8.PNG?raw=true)
![Add](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/Add%EC%82%AC%EC%9A%A9.PNG?raw=true)
### 이때 사용된 명령어 :
* status : 현재 상태를 출력함.
 ### 사용법 :
 ```
    git status
 ```  
* add : 현재 상태에서 타입캡슐에 추가되지 않은 내용을 캡슐에 넣음.
    > -A : 인덱스가 이미 엔트리를 가지는것까지 모두 올림.
 ### 사용법 :
 ```
    git add -A
 ```
 ## **캡슐안에 내용들을 저장했다면 언제든지 꺼낼수 있도록 일단 묻어놔야함. 캡슐을 묻는 명령과 현재 묻혀있는 캡슐을 보여주는 명령어를 실행해봄.**
 ![commit과 log](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/commit%EA%B3%BC%20log.PNG?raw=true)
 ### 이때 사용된 명령어:
 * commit : 정보가 들어있는 캡슐을 묻음.
    >-m : 묻을 캡슐에 대한 설명을 추가함.
### 사용법 :
 ```
    git commit 
    git commit -m "부가 설명"
 ```
* log : 지금껏 묻은 타입캡슐들을 보여줌.
    > --all: 묻힌 캡슐들을 모두 보여준다.
### 사용법 :
 ```
    git log 
    git log --all
```
## **타임캡슐을 묻은 후 그 작업물에 대해 내용을 추가했는데 , 추가한 설명이 마음에 들지않아서 다르게 설명하고 싶음. 아까 묻어놨던(저장했던) 시점으로 돌아가고싶음.**
![변경 첫번째](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/%EB%82%B4%EC%9A%A9%EB%B3%80%EA%B2%BD%EC%B2%AB%EB%B2%88%EC%A7%B8..PNG?raw=true))
![reset](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/reset%EC%9C%BC%EB%A1%9C%20%EB%8F%8C%EB%A6%BC..PNG?raw=true)

### 이때 사용된 명령어:
* reset : 과거에 캡슐을 저장해놨던 시점으로 돌아감.
    > --hard :돌아간 시점 이후를 모두 잊음.(다시 못돌아감)
 ### 사용법 :
 ```
    git reset 돌아갈시점일련번호 --hard
```
## **이제 이렇게 작업 내용들을 다 삭제하고 과거로 돌아가는 것이 아니라, 새로운 평행우주를 만들어서 거기서 새로운 시도를 해보고싶음.**
![NewTry생성](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/NewTry%EC%83%9D%EC%84%B1.PNG?raw=true)
![checkout으로넘어감](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/checkout%EC%9C%BC%EB%A1%9C%20%EB%84%98%EC%96%B4%EA%B0%90.PNG?raw=true)

### 이때 사용된 명령어:
* branch : 기존의 내용을 그대로 담고있는 새로운 평행우주 생성, 나무에서 나뭇가지가 여러갈래로 뻗어가듯 그런거라 보면됨.
    >-a: 로컬에서의 브랜치뿐만아니라 원격저장소의 브랜치까지 보여줌.<br>
    >-M : 브랜치 이름변경.<br>
    >-D : 브랜치 삭제.
### 사용법 :
```
    git branch "생성할 브랜치이름"
    git branch  //현재 존재하는 브랜치들을 보여준다.
    git branch -D "브랜치명"
```
* checkout : 다른 브랜치로 넘어감.
    > -b:브랜치를 만들고 넘어감.<br>
### 사용법 :
```
    git checkout "브랜치명"
```
## **NewTry라는 브랜치에서 새로운 캡슐을 생성했는데, 이게 마음에 들어서 기존 내용에 통합하고 싶음.**

![merge](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/NewTry%EC%97%90%EC%84%9C%20%EC%83%88%EB%A1%9C%EC%9A%B4%20%EC%BA%A1%EC%8A%90%EC%83%9D%EC%84%B1,%20merge%EA%B9%8C%EC%A7%80.PNG?raw=true)

### 이때 사용된 명령어:
* merge :  다른 평행우주에서 내용을 가져와 통합. 
### 사용법 :
 ```
    git merge "통합할브랜치이름"
```
## **이 프로젝트가 여러 브랜치들을 통합했다고 가정. 그럴경우 log로 기록을 봤을때 알아보기가 너무복잡함. 그래서 통합된 과정들을 좀더 단순화해서 보고싶음.**
![되돌림](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/rebase%EB%A5%BC%EC%93%B0%EA%B8%B0%EC%9C%84%ED%95%B4%20%EB%90%98%EB%8F%8C%EB%A6%BC..PNG?raw=true)
![rebase](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/rebase%20%EC%82%AC%EC%9A%A9.PNG?raw=true)

### 이때 사용된 명령어:
* rebase :  다른 평행우주에서 내용을 가져와 통합.(변경을 한줄로 정리) 
### 사용법 :
 ```
    git rebase "통합할브랜치이름"
```
## **작업을 어느정도 하고보니 이젠 다른사람들과 코드를 공유하면서 같이 작업하고싶음.**
![remote와push](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/remote%EC%99%80%20push.PNG?raw=true)

### 이때 사용된 명령어:
* remote : 현 폴더의 원격 레파지토리를 확인함 
### 사용법 :
 ```
    git remote //연결된 원격저장소 확인
    git remote add "원격레파지토리이름" "주소"//주소에 해당하는 곳에 레파지토리이름 으로 저장.
```
* push : 로컬저장소(현재 작업하고있는 폴더)의 내용을 원격 저장소(github)에 올림.
### 사용법 :
 ```
    git push
```
## **지금까지 A라는 컴퓨터에서 작업을했는데, 일이 생겨서 B라는 컴퓨터로 이어서 작업을 해야함.**

![clone](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/clone%EB%A1%9C%20%EC%BD%94%EB%93%9C%EB%82%B4%EB%A0%A4%EB%B0%9B%EA%B8%B0.PNG?raw=true)

### 이때 사용된 명령어:
* clone :  원격저장소에 있는 코드를 내려받음.
### 사용법 :
 ```
    git clone "URL"(주소)
```
## **B컴퓨터에서 어느정도 작업을 진행하고, 이를 저장하기위해 원격 저장소에 올렸음.**
![B에서저장](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/%EB%85%B8%ED%8A%B8%EB%B6%81%EC%97%90%EC%84%9C%20push.PNG?raw=true)
## **다시 A컴퓨터로 돌아와서 작업을 진행하려하는데, B에서 진행해 놓은것이 있기때문에 업데이트 후 진행해야 함.**
![pull](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/pull%EB%A1%9C%20%EC%BD%94%EB%93%9C%20%EC%97%85%EB%8D%B0%EC%9D%B4%ED%8A%B8.PNG?raw=true)

### 이때 사용된 명령어:
* fetch : 원격저장소의 상황을 최신 상황으로 업데이트 함.
### 사용법 :
 ```
    git fetch
```
* pull : 로컬저장소의 코드를 원격저장소의 내용으로 업데이트 함.
### 사용법 :
 ```
    git pull 원격명 브랜치명
```
## **다른 사람들과 협업을위해 NewTry라는 브랜치 들어있는 내가 내용을 추가한 파일을 올림.**
![브랜치올리기](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/%EB%8B%A4%EB%A5%B8%20%EB%B8%8C%EB%9F%B0%EC%B9%98%EB%A5%BC%20%EC%98%AC%EB%A6%AC%EA%B8%B0..PNG?raw=true)     

## **코드가 거의 완성됐고, 이정도가 첫번째 버전(릴리즈)라고 생각함. 이걸 내놓고싶음.**
![tag](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/tag.PNG?raw=true)

![tag](https://github.com/cpu500m/SE_EngineeringAssignment2/blob/main/images/tag%20%EC%98%AC%EB%A6%AC%EA%B8%B0.PNG?raw=true)

### 이때 사용된 명령어:
* tag : 현재 버전을 저장. 
### 사용법 :
 ```
    git tag "tag이름"
    git push 원격명 태그명 // 태그를 원격저장소에 올림.
```

|명령어|링크|
|:--|:--|
|init|[init](#init)
