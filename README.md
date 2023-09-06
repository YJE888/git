# Git
### 참고 GIT 작업 흐름
Working Area에서 파일을 수정 
-> 수정한 파일 중 일부를 Staging Area로 추가 ($ git add file1 file2)
-> Staging Area에 있는 변경 사항 커밋 ($ git commit -m "First Commit")
-> 로컬 저장소에 기록
-> 원격 저장소에 기록($ git push origin master)

### git
- git 설치
```
# yum -y install git
```
- git 초기화
```
$ mkdir git
$ cd git

$ git init

$ git config --global user.name “username”
$ git config --global user.email “email@email.com"
```
- staging area로 파일 이동
```
$ git status
$ git add file1 file2
$ git status

# 스테이징 영역의 파일을 삭제하는 방법
# 방법 1)
$ git reset file2 = $ git rm -cached file2

# 방법2) .gitignore 사용
$ vi .gitignore
    # 무시할 디렉토리
    my_folder/

    # 특정 확장자의 파일 무시
    *.log

    # 특정 파일 제외
    !important_file.txt
```

- Staging Area에 있는 변경 사항 커밋
```
$ git commit -m "add first two file"
```
