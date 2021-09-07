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

### 🔶  브랜치 생성 + 체크아웃
```
$ git checkout -b <branch name>
```

### 🔶 원격 브랜치 목록보기
```
$ git branch -r
```

### 🔶 모든 브랜치 목록보기
```
$ git branch -a
```

### 🔶 브랜치 이름 바꾸기
```
$ git branch -m <branch name> <new branch name>
```

### 🔶 로컬 브랜치 삭제
```
$ git branch -D <branch name>
```

### 🔶 원격 브랜치 삭제
```
$ git push origin --delete <branch name>
```

### 🔶 commit한 이전 코드 취소하기
```
$ git reset — hard HEAD^
```

### 🔶 코드는 살리고 commit만 취소하기
```
$ git reset — soft HEAD^
```
### 🔶 로컬에서 다른 branch merge 하기
```
$ git merge <branch name>
```

### 🔶 merge 취소하기
```
$ git reset — merge
```

### 🔶 마지막 커밋 메세지 수정하기
```
$ git commit --amend -m "new msg"
```

### 🔶 commit을 취소하고 해당 파일들은 staged 상태로 워킹 디렉터리에 보존
```
git reset --soft HEAD^
```

### 🔶 원격 머지 commit을 취소하고 올리고 싶을때
```
git revert -m 1 <commit number> // 기존 브랜치 기준
git revert -m 2 <commit number> // 머지시킨 
```

# css_memo
css 메모

### 🔶 비율계산
[참고](https://www.w3schools.com/howto/howto_css_aspect_ratio.asp)
```
div {
  background-img: url('url');
  width: 100%;
  padding-top: 75%; /* 4:3 Aspect Ratio (divide 3 by 4 = 0.75) */
}
```

### 🔶 position absolute 상태에서 중앙정렬
[참고](https://yuddomack.tistory.com/entry/div-%EA%B0%80%EC%9A%B4%EB%8D%B0-%EC%A0%95%EB%A0%ACfeat-position-absolute)
```
#parent {
  position: relative;
  width: 100%;
  padding-top: 100%; // 1:1 비율
}

#child {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```
### 🔶 \n 으로 들어온것 html에서 자동 한줄띄기 처리
```css
.text-block {
    white-space: pre; // or pre-line
}
```
[참고](https://stackoverflow.com/questions/54979287/replace-n-to-new-line-on-vuejs)

### 🔶 android 브라우저 등 디바이스마다 픽셀계산이 다를 수 있어 isBottom 계산시 보충 값을 설정해 주어야함 (소수점 보완)
```js
const isBottom = (this.$listCont.scrollTop()+2) + this.$listCont.innerHeight() >= this.lastScrollH;
const isBottom = (this.$listCont.scrollTop()+2) + this.$listCont.innerHeight() >= this.$listCont[0].scrollHeight;
```
