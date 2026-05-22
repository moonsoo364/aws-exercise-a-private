# 개요

# 260521 CodeDeploy 실습

'AWS 인프라 구축 가이드' 저자 깃의 script로 AWS CodeDeploy 실행이 안되서 해당 깃 파일을 내 깃에 받아서 코드 수정 후 다시 배포함

[deopard님의 원본 git branch](https://github.com/deopard/aws-exercise-a/tree/code-deploy)

## 수정한 코드

이전 명령어를 직접 ami 를 생성한 인스턴스에 접속해서 호출해 보면 권한 관련 문제가 발생함

이전 `restart_server` 스크립트 내용 
```bash
service nginx restart
```

sudo 권한으로 부여하니 정상 실행 되었음 다만 실무 환경에서는 자동화 스크립트 전체를 `sudo`로 실행하는 방식은 보안상 권장되지 않는다.

```bash
sudo systemctl restart nginx
```
# 260522 AWS Secrets Manager 실습
IAM 유저와 `SecretManagerReadPolicy` 정책을 생성한 뒤 accessKey를 발급받아 
JS 애플리케이션에서 AWS SDK를 이용해 secrets manager에 저장된 키를 조회해보는 실습을 진행함
 