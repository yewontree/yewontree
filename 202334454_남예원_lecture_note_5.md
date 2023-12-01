# Linux CLI-2 #

### Standard Output > ###
```bash
$ ls -lh > __.txt // ls -lh의 결과를  __.txt로 저장
$ cat __.txt //__.txt 내용을 보여줌
$ ls -lh >> __.txt // __.txt에 누적되게 ls -lh의 내용 추가
```
### Standard Input < ###
```bash
$ sort < words.txt // words.txt를 sorting 후 출력
$ sort < words.txt > sorted_words.txt // 출력하지 않고 sorted_words.txt에 저장
```
### Pipelines | ###
```bash
$ command1 | command2 
//command1의 output을 command2 에 input으로 넣는다$ ls -lh | less //새로운 스크린에 출력 : 스크롤
$ ls | wc -l // 파일이 몇 개인지 출력
```
### Expansion ###
```bash
$ echo ___ // 뒤에 오는 문자들(___) 출력
$ echo * // 현재 디렉토리에 있는 파일 전부 출력
$ echo ~ // 현재 사용자의 홈 디렉터리 출력
$ echo ~(user_name) // 특정 사용자의 홈 디렉터리 출력
```
#### Tip: Backslash \ ####
: 커맨드를 보기 편하게 줄바꿈해서 입력 가능
```bash
$ ls -l\
> --reverse \ // 여기서 > 는 입력 대기 중
> --human-readable // -- command의 풀네임
```
### Permissions ###
Linux is a multi-user system.
Files and diractories have a permission assigned differently to owner / group / others.
*rwx : read. write, execute*
```bash
-rwxr-xr-x l root root 1113504 Jun 6 2019 /bin/bash
```
세 자리로 끊어읽기 rwx r-x r-x
- file owner 는 rwx 가능
- group owner,  other users 는 read, execute만 가능

#### chmod ####
changes permissions.
```bash
chmod 600 some_file
```
6=110=rw- for owner  // 이진수
0=000=--- for group  
0=000=--- for others

#### Superuser ####
has all system administation authority
```bash
sudo -i
``` 
sudo를 쓰기 전에  superuser 이어야 함.

### Shell Script ###
```bash
#!/bin/bash (bash script 라는 걸  알려줌)
#어쩌구저쩌구이건주석
$ nano myscript.sh # myscript라는 파일이 있다면 거기에 작성, 없다면 새로 생성되고 작성 가능
$ sh myscript.sh #script 실행
```
#### Tip: History ####
 썼던 커맨드 히스토리 볼 수 있음
```bash
$ history > history_command.txt # txt 파일로 저장까지
```

