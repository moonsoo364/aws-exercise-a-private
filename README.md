# 개요

'AWS 인프라 구축 가이드' 저자 깃의 script로 Code Deploy 실행이 안되서 해당 깃 파일을 내 깃에 받아서 코드 수정 후 다시 배포함
[deopard님의 원본 git branch](https://github.com/deopard/aws-exercise-a/tree/code-deploy)

# 수정한 코드

이전 명령어를 직접 ami 를 생성한 인스턴스에 접속해서 호출해 보면 권한 관련 문제가 발생함

이전 `restart_server` 스크립트 내용 
```bash
service nginx restart
```

sudo 권한으로 부여하니 정상 실행 되었음

```bash
sudo systemctl restart nginx
```
