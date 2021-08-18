# Linux Basic
##### 권한 변경
root로 권한 변경
```{.bash}
-$ sudo su - root
-#
```  
log out
```{.bash}
exit
```
##### 파일 구조
root 경로로 이동  
디렉토리 리스트  
디렉토리 리스트 자세히 옵션  
home으로 이동
```{.bash}
/$ cd /
/$ ls
/$ ls -l
/$ cd /home
```

##### 파일 경로와 순회
현재 디렉토리 경로를 출력 `pwd`  
디렉토리 목록 나열 `ls`  
디렉토리를 변경 `cd`  
나의 home 디렉터리 `~`  
도움말 `man {command}`

##### 파일 관리
디렉토리 생성 `mkdir`  
디렉토리 삭제 `rmdir`  
빈 파일 생성 `touch`  
파일 이동 / 이름 변경 `mv`  
파일 삭제 `rm`  
파일 복사 `cp`  

##### 파일 찾기
현재 디렉토리에서(/) 이름으로 파일 찾기 `find ./ -name file_name` 현재 디렉토리에서 file_name 파일 찾기  
사이즈 옵션 `find . -name *.java -size +1c` 최소 1바이트 크기 이상 `*.java` 파일을 root 아래에서 찾기  
파일 내부 보기 `cat`  
문서 내부 text 검색 `grep "class" Hello.java`  
파일 이름 목록화 검색 'ls Hello[12].java'  
파일 비교(위치만) `cmp`  
파일 비교(내용) `diff`  
파일 형태 검색 `file`  

##### 유용한 명령어
화면 지우기 `clear`  
이전 명령어 보기 `history`  
이전 명령어 실행 `!번호`  
결과를 파일로 저장 `history > test.txt` history 명령어 결과를 test.txt로 저장   
결과를 파일에 추가하기 `echo "hello" >> test` hello를 test에 추가  
실행결과를 명령어 입력으로 받기 `cat test | grep He` test 파일 출력을 He를 찾는다.  
실행결과를 한화면씩 보기 `ls | less`  
실행결과를 sort `cat test | sort -r`  
명령어 연속 입력 `touch test1; echo "okay~" >> test1; cat test1`

##### 파일 압축 관리
파일 압축하기 `tar -cf name.tar a b c` `tar -zcf name.tar.gz a b c`  
압축풀기 `tar -xvf name.tar`  `tar -zxvf name.tar.gz`  
   -f 파일 이름을 지정  
   -c 파일을 tar로 묶음  
   -x tar 압축을 품  
   -v 내용을 자세히 출력  
   -z gzip으로 압축하거나 해제함  
   -t 목록 출력  
   -p 파일 권한을 저장  
   -C 경로를 지정  

##### 링크
Hard link file `ln Original_FileName Link_FileName`  
Symbolic link file `ln -s 실행파일 바로가기`  
환경변수 `$PATH`  

##### 사용차 추가/편집/삭제
사용자 추가 `useradd`  
사용자 변경 `usermod`  
사용자 삭제 `userdel`  
사용자 확인 `cat etc/passwd`  
사용자 패스워드 `sudo passwd 사용자이름`  

##### 디렉토리 소유권 변경  
디렉토리 소유권 변경 `sudo chown user_name:group_name dir` 

##### 파일 권한 변경
`chmod 644 test.txt` 소유자 소유그룹 일반유저의 rwx를 각각 2진수로 표현  
`chmod ugo+rw test.txt` 소유자, 그룹, 일반유저에 rw 추가  
`chmod a-wx test.txt` 모든 유저에 wx 권한 삭제   

