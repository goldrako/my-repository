# my-repository
## git 명령어 실습을 위한 레포지토리

### git-crypt 실습
 https://github.com/AGWA/git-crypt

 $ git-crypt init

 그리고 repository root 경로애 .gitattributes 파일을 만들고 내부에 git-crypt가 적용될 파일을 적어주면 된다.

```sh
config/production/** filter=git-crypt diff=git-crypt
# more...
```

#### key export

```
$ git-crypt export-key /path/to/key
```
전달받은 해당 key 파일을 사용하여 복호화 처리에 이용

#### unlock

암호화된 레포지토리를 클론하여 받은 곳에서 key를 이용하여 복호화함

```sh
$ git-crypt unlock /path/to/key
```


### Ref
[git-crypt](https://joont92.github.io/git/git-crypt/)  
[[Github] git-crypt 적용하기](https://ye-geeee.tistory.com/70)  