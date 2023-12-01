# Git-1 #

: Version control 과 Collaboration 에 도움을 주는 시스템

#### Version control ####
- changes : 베이스 버전에서 수정한 부분 데이터를 저장함 변화를 쌓아가며 버전 갱신
- snapshots : 수정된 파일 자체를 저장함 (Git 방식)

#### Collaboration ####
- local : 내 컴퓨터에서만 수정 가능, 다른 사람과 협업 어려움

- centralized : 중앙 서버에 Database가 있어 여러 컴퓨터가 접근 가능. 중앙서버가 다운되면 수정하고 저장하는 데에 문제 생김

- distributed : 서버 컴퓨터가 있고, 각 사용자 컴퓨터에도 Database가 있음. 서버 파일에 문제가 생겨도 복구 용이. 각 사용자가 자기 컴퓨터에서 수정할 수 있고 서버에 업로드하거나 서버에서 가져올 때만 통신함.

### Status ###

 modified : 파일을 수정함

 staged : staging area로 옮긴 상태

 comitted : snapshot을 찍었다, 특정 버전을 기록했다

  

  ### Git configuration ###

  : are stored in three levels

  1. system level : 모든 사용자와 repository에 영향을 줌

  2. global level : 현재 유저의 모든 repository에 영향을 줌

  3. local level : 그 현재 repository에만 영향을 줌

  Each level overrides values in the previous level

  local <-- global <-- system (시스템에 있는 걸 글로벌이 덮고, 글로벌에 있는 걸 로컬이 덮어 쓴다)

  config명령은 처음에 한 번만 쓰면 된다.


```bash
     $ git config --global user.name "Yewon Nam" 
     $ git config --global user.email yewontree@gachon.ac.kr
     $ git config --global init.defaultBranch main
     $ git init #현재 directory에 .git 생성
     $ ls -lha #a 붙이면 숨겨진 파일까지 출력
     $ git status #현재 status 출력함. commit 전에는 No commits yet도 나옴
```

  - [출력]Untracked files: ... (현재 이 directory에 존재하지만 git이랑 관련 x)

```bash
     $ git add [file_name] 
```
  - stage에 올라간 상태

  [출력]Changes to be commited: [git add 한 file_name] 


  - stage에 올라간 파일을 수정하고 status를 확인할 때
    [출력]Changes not staged for commit: [수정한 파일]
    이 상태에서 commit 하면 수정 전 파일이 commit 됨. 수정한 파일을 commit하려면 다시 git add 해주면 됨.

```bash
     $ git add . #모든 파일 staging
     $ git rm --cached [file_name] #Unstaging
     $ nano .gitignore #이 파일 안에 적힌 파일은 git이 무시함
```

  .gitignore file

- \*.a 		// 확장자가 a인 모든 파일 무시

- !file_name.a // ! 붙은 건 무시 안 함

  ### Commit ###
```bash
$ git commit -m ["commmit message"] #현재 commit 하는 게 어떤 것이다 이름 해주기
$ git log #지금까지 commit한 기록 볼 수 있음
$ git branch #현재 branch 출력
$ git branch -m [현재 branch 이름] [바꿀 branch 이름] #branch 이름 변경
```



