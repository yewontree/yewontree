# Linux ClI #

```bash
$ pwd   현재 경로(계층 주소)
$ cd    change directory
$ ls    list files and directorie
```

|문자|설명|
|:---:|:---|
|.| current directory|
|..|	upper-level directory|
|~| 	home of current user|
|/[directory name]|	absolute path|
|./[directory name]|	relative path|
|../[directory name]|	상위 폴더로 가서 선택|
### ls ###
|커맨드|설명|
|:---:|:---|
|$ls -l|show detailed information|
|$ls -lh|same -l, but size in unit|
|$ls /[directory name]|-l,-lh 등을 앞에 써서 같이 쓸 수 있음|
|$ls -la ..|List all files (even ones with names beginning with a period character, which are normally hidden) in the parent of the working directory in long format

Tab key : autocompletion
Up arrow key : past commands

```bash
$clear 터미널 쓱싹
```
#### cp & mv & rm ####
```bash
$ cp [복사할 파일] [파일 이름]
$ cp -r ../[파일 이름] .
: 디렉터리 복사. (../상위 디렉터리안 에 있는 [파일 이름]을 현재 디렉토리에 복사)

$mv [바꿀 파일] [새로운 이름] //디렉터리도 같은 방
$mv [옮길 파일] ../목적 디렉터리

$rm [지울 파일]
$rm -r [지울 디렉터리]
$rm -i []   :지울거냐고 물어봄
```
#### mkdir ####
```
$mkdir [새로운 디렉터리의 이름]
```
### Wildcard ###
|문자|설명|
|:---:|:---|
|\*|all filenames|
|g*|g로 시작하는 모든 파일|
|b*.txt|b로 시작하는 모든 txt파일|
|Data???| Data로 시작하고 뒤에 문자 세 개가 있는 파일|

*rm과 \*을 쓸 때 매우 주의가 필요 ls로 먼저 확인하고 지울 것
ClI가 아니라 GUI에서 지우는 것이 가장 안전(휴지통 있음)*

##### 도움이 필요하다면 ####
#
```
$help [검색할 커맨드]
$man [] //나갈 때 q
```
창 닫을 때 $exit