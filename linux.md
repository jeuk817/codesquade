# 리눅스 명령어 정리

## 목록

1. ls - 현재 위치의 파일목록을 조회하는 명령어
2. cd - 디렉토리를 이동하는 명령어
3. touch - 파일의 용량이 0인 파일을 생성, 날짜 변경하는 명령어
4. mkdir - 디렉토리를 생성하는 명령어
5. cp - 파일을 복사하는 명령어
6. mv - 파일을 이동시키는 명령어
7. rm - 파일을 제거하는 명령어
8. cat - 파일의 내용을 화면에 출력하거나 파일을 만드는 명령어
9. redirection - 화면에 출력되는 결과를 파일로 저장하는 명령어
10. pwd - 현재 디렉토리의 위치를 확인하는 명령어
11. echo - 매개변수를 표준출력으로 보내주는 명령어
12. grep - 파일 내에서 지정한 패턴이나 문자열을 찾은 후에, 그 패턴을 포함하고 있는 모든 행을 표준 출력해주는 
13. pipe -|를 기준으로 앞에 있는 커맨드의 표준 출력을 뒤에 있는 커맨드의 표준 입력으로 사용하는 명령어


## 설명
1. ls (list segments) 
  : ls 는 현재 위치의 파일 목록을 조회하는 명령어 입니다.
    * ls -l : 숨김 파일들을 제외한 파일들의 상세정보를 나타냅니다.
    * ls -al : 모든 파일들의 상세정보를 나타냅니다.
    
2. cd (change directory) 
  : cd 는 경로를 이동할 때 사용하는 명령어 입니다.
    * cd ~ : 어느 곳에든지 홈디렉토리로 바로 이동합니다.
    * cd .. : 상위 디렉토리로 이동합니다.
    * cd /dir : 절대경로 dir 로 이동할 경우 사용합니다.
    * cd - : 이동하기 바로전의 디렉토리로 이동합니다.
    
3. touch 
  : touch 는 파일의 용량이 0인 파일을 생성, 날짜 변경하는 명령어 입니다.
    * touch filename : filename 의 파일을 생성합니다.
    * touch -c filename : filename 의 시간을 현재시간으로 변경합니다.
    * touch -t 200001011200 filename : filename 의 시간을 날짜정보(YYYYMMDDhhmm) 로 변경합니다.
    * touch -r filename1 filename2 : filename2의 날짜정보를 filename1 의 날짜정보와 같게 변경합니다.
    
4. mkdir (make directory) 
  : mkdir 은 새로운 디렉토리를 만들 때 사용하는 명령어입니다.
    * mkdir dirname : dirname 의 디렉토리를 생성합니다.
    
5. cp (copy) 
  : cp 는 파일을 복사하는 명령어 입니다.
    * cp file cfile : file 을 cfile 이라는 이름으로 복사합니다.
    * cp -f file cfile : 복사할 때 복사대상이 있으면 지우고 강제로 복사합니다.
    * cp -R dir cdir : 디렉토리 복사할 때 사용하며, 폴더안의 모든 하위경로와 파일들을 모두 복사합니다.
    
6. mv (move) 
  : mv 는 파일을 이동하는 명령어 입니다. cp 와 비슷하지만 다른 점은 cp 는 파일을 복사하여 원본 파일이 남아있지만 mv 는 원본 파일이 남지 않는다는 점입니다. 그래서 이름 변경시에도 사용가능합니다.
    * mv fname mfname : fname 의 파일을 mfname 의 이름으로 이동/변경 합니다.
    * mv -b fname mfname : mfname 의 파일이 존재하면 mfname 을 백업한 뒤에 이동합니다.
    * mv -f fname mfname : mfname 의 파일이 존재하면 백업 없이 덮어씁니다.
    
7. rm (remove) 
  : rm 은 파일이나 디렉토리를 삭제할 때 사용하는 명령어 입니다.
    * rm fname : fname 을 삭제합니다.
    * rm -f fname : fname 을 묻지 않고 삭제합니다.
    * rm -r dir : dir 을 삭제합니다.
        * 디렉토리는 -r 옵션 없이는 삭제할 수 없습니다.
        
8. cat (catenate) 
  : 표준입력을 표준출력으로 보내주는 역할을 하며, 파일이름을 인자로 받아서 그 내용을 출력할 때 사용합니다.
    * cat fname : fname 의 내용을 출력합니다.
    * cat fname1 fname2 : fname1 과 fname2 의 내용을 이어서 출력합니다.

9. redirection ( '>' , '>>' ) 
  : 표준출력의 내용을 뒤에오는 argument 파일에 넣어주는 기능을 하며, 리눅스 스트림의 방향을 조정하는 명령어 입니다.
    * 명령 > 파일 : 명령의 결과를 파일로 저장합니다.
        * cat fname1 fname2 > fname3 : fname1,fname2 를 출력하고 fname3 이라는 파일에 저장합니다.
    * 명령 >> 파일 : 명령의 결과를 파일에 추가합니다.
        * cat fname4 >> fname3 : fname3 에 fname4 의 내용을 추가합니다.
    * 명령 < 파일 : 파일의 데이터를 명령에 입력합니다.
        * cat < fname1 : fname1 의 내용을 출력합니다.
    * ex) cat < fname1 > fname2 : fname1 의 내용을 출력하는 결과물을 fname2 에 저장합니다.
    
10. pwd
  : 현재 디렉토리의 위치를 확인하는 명령어 입니다.

11. echo
  : 매개변수를 표준출력으로 보내주는 명령어 입니다.

12. grep
  : grep 명령은 파일 내에서 지정한 패턴이나 문자열을 찾은 후에, 그 패턴을 포함하고 있는 모든 행을 표준 출력해 줍니다. 물론, 한 디렉토리 내에서 지정한 패턴을 포함하는 파일을 출력할 수도 있습니다. grep 명령은 하나 이상의 파일로부터 프로그램 수정 등을 위해 변수, 또는 함수명을 찾을때 많이 사용됩니다.
~~~
 cat hello.txt | grep hello
~~~

13. Pipe
  : 일반적으로 "A | B" 처럼 사용하는데 |를 기준으로 A에 있는 커맨드의 표준 출력을 B에 있는 커맨드의 표준 입력으로 사용합니다.