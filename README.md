# AWS Cloud9
AWS Cloud9 인스턴스 종료와 관련된 설정

## autoshutdown-configuration
- 파일 위치: Cloud9 EC2 사용자 계정 홈디렉토리/.c9
  만약 사용자 계정이 ubuntu 라면
  /home/ubuntu/.c9
  
- 파일명: autoshutdown-configuration
```
SHUTDOWN_TIMEOUT=30
```

## stop-if-inactive.sh
- 파일 위치: Cloud9 EC2 사용자 계정 홈디렉토리/.c9
- 역할: cron job에 의해 매분마다 실행하여 미사용 여부를 확인
- /etc/cron.d/c9-automatic-chutdown
  ```
  * * * * * root /home/ubuntu/.c9/stop-if-inactive.sh
  ```
