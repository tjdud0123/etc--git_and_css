# git_memo
쓰는 git 명령어 모음


### 🔶  branch1에서 작업 중인데 branch2로 이동하고 싶을 때
commit 하지말고 add한 후 <br>
```
$ git stash
```
branch2로 이동
```
$ git checkout branch2
```
branch1으로 컴백
```
$ git checkout branch1
```
복구
```
$ git stash pop
```
### 🔶  마지막 커밋을 취소하고 staged된 상태로 돌리고 싶을 때
```
$ git reset --soft HEAD~
```
