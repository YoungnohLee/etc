## How to use `venv` & `conda`

```
### venv
$ python -m venv NAME
$ .\NAME\Scripts\activate
$ pip install -r requirements.txt

# 주피터 노트북에서 가상환경을 사용하려면, 주피터 노트북 내부에 가상환경 설치해야함
$ pip install jupyter
$ pip install ipykernel
$ python -m ipykernel install --user --name NAME --display-name "출력될 커널 이름"

$ deactivate

### conda
$ conda create --name NAME
$ conda create --name NAME python=VERSION

$ activate NAME
$ conda install PACKAGE.NAME
$ conda search PACKAGE.NAME

$ conda list --export > package-list.txt
$ conda install --file package-list.txt

$ conda env list

# 현재 활성화 되어있는 conda 환경 export 하기
$ conda env export > environment.yaml
# yaml 파일로부터 conda 가상환경 import 하기
$ conda env create --file environment.yaml

```

## How to use `git`
```
### 설정
$ git config --global user.name "MY NAME"
$ git config --global user.email "junior0101@naver.com"

$ git init
# git remote add origin https://github.com/YoungnohLee/etc.git # git 을 원격 저장소에 저장하게 해주는 엔드포인트

$ git pull https://github.com/YoungnohLee/etc.git # git 원격 저장소와 동기화
# git clone https://github.com/YoungnohLee/etc.git # remote origin 에는 clone 해온 remote url 이 저장되어있음.

### 소스 기록
$ git add . # 모든 변경사항을 git 에 추가해줌
$ git remote show origin # remote origin 에 원격 저장소 주소가 잘 등록되었는지 확인

### 소스 커밋
$ git status # 파일의 추적 상태 ## Staged 상태의 파일은 아직 커밋된 상태가 아님.
$ git commit -m "MY COMMMIT MESSAGE"

### 소스 푸시
$ git pull origin main # main branch 를 pull 하여 로컬 저장소와 동기화
$ git push origin main


### 브랜치
$ git branch 
$ git branch BRANCH_NAME 
$ git checkout BRANCH_NAME # 새로운 브랜치로 접속

$ git push origin BRANCH_NAME
$ git branch -d OLD_BRANCH_NAME

```