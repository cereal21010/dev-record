### 새로운 저장소 만들기
```
git init
```

### 저장소 받아오기
- 로컬 저장소 복제(clone)
```
git clone /로컬/저장소/경로
```
- 원격 서버의 저장소 복제
```
git clone 사용자명@호스트:/원격/저장소/경로
```

### 작업의 흐름
- 실제 파일들로 이루어져있는 작업 디렉토리(Working directory) -> 준비 영역(staging area) 역할인 인덱스(Index) -> 최종 확정본(commit)인 HEAD

![image](https://user-images.githubusercontent.com/57171304/182372548-b4a0044b-a2e9-46c2-b066-10189acd7a2f.png)

### 추가와 확정(commit)
- 아래 명령어로 인덱스(stage)에 추가
```
git add <파일 이름>
git add *
```
- 실제 변경 내용을 확정하는 명령어
```
git commit -m "first commit"
```
*변경된 파일이 HEAD에 반영되고, 아직 원격 저장소에는 반영되기 전

### 변겨 내용 발행(push)하기
- 변경 내용을 원격 서버로 올리는 명령어
```
git push origin(원격) master(로컬)
```
- 기존에 있던 원격 저장소를 복제한 것이 아니라면 아래의 명령어 사용
```
git remote add origin <원격 서버 주소> 
```

### 가지(branch)치기
- 가지를 만들고 갈아타는 명령어
```
git checkout -b feature_x
```
- master가지로 돌아가는 명령어
```
git checkout master
```
- 가지를 삭제한는 명령어
```
git branch -d feature_x
```


### 로컬 변경 내용 되돌리기
- 로컬의 변경 내용을 원격 저장소의 내용으로 되돌릴 수 있다.
```
git checkout -- <파일 이름>
```
*stage(git add)에 추가되거나, 새로 생성하 파일은 그대로 남는다.

- 로컬의 모든 변경 내용과 확정본을 포기하고 원격 저장소의 최신 이력을 가져오고,
로컬 main 가지가 origin의 이력을 가리키도록 할 수 있다.
```
git reset --hard origin/master
```

출처 : https://rogerdudler.github.io/git-guide/index.ko.html











