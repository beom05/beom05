# top명령어
## top명령어란 

**실시간으로 CPU 사용률을 체크해주는 도구이다.**

윈도우의 작업관리자랑 비슷하며, 리눅스를 사용하는 서버의 성능이나 
현재 돌아가고 있는 상황을 볼 때
사용한다.

top 명령어는 실시간으로 시스템의 프로세스와 메모리 사용 상태를 모니터링한다.

## 사용법: 터미널에서 top 입력
![image_top](https://github.com/beom05/beom05/blob/main/linux_top.png)

## 주요 기능:

PID: 프로세스 ID

USER: 프로세스를 실행한 사용자

PR: 프로세스의 우선순위

NI: 프로세스의 nice 값

VIRT: 가상 메모리 사용량

RES: 실제 메모리 사용량

SHR: 공유 메모리 사용량

S: 프로세스 상태 (R: 실행 중, S: 대기, Z: 좀비, 등)

%CPU: CPU 사용률

%MEM: 메모리 사용률

TIME+: 실행 시간

COMMAND: 실행된 명령어

## 옵션:

-u [USER]: 특정 사용자의 프로세스만 표시

-p [PID]: 특정 PID의 프로세스만 표시

-n [ITERATIONS]: 지정한 횟수만큼 업데이트 후 종료

# ps 명령어
ps 명령어는 현재 실행 중인 프로세스의 스냅샷을 보여준다.

## 사용법: 터미널에서 ps 입력
![image_ps](https://github.com/beom05/beom05/blob/main/linux_ps.png)

## 주요 기능:

PID: 프로세스 ID

TTY: 터미널 타입

TIME: CPU 사용 시간

CMD: 실행된 명령어

## 옵션:

-e 또는 -A: 모든 프로세스 표시

-f: 자세한 포맷으로 출력

-u [USER]: 특정 사용자의 프로세스 표시

-p [PID]: 특정 PID의 프로세스 표시

aux: 모든 프로세스를 상세히 표시 (a 모든 사용자, u 사용자/CPU/메모리 사용률, x 터미널에 종속되지 않은 프로세스)

# jobs 명령어
jobs 명령어는 현재 셸 세션에서 실행 중인 작업 목록을 보여줍니다.

## 사용법: 터미널에서 jobs 입력

## 주요 기능:

[N]: 작업 번호

Job State: 작업 상태 (Running, Stopped, 등)

Command: 실행된 명령어

## 옵션:

-l: 작업의 PID 표시

-n: 상태가 변경된 작업만 표시

-p: 각 작업의 프로세스 ID만 표시

# kill 명령어
kill 명령어는 지정한 프로세스를 종료합니다.

## 사용법: kill [옵션] PID

## 주요 기능:

PID: 종료할 프로세스의 ID

## 옵션:

-l: 사용 가능한 신호 목록 표시

-s [SIGNAL] PID: 특정 신호를 사용하여 프로세스 종료 (기본은 SIGTERM)

-9 PID: 강제 종료 신호 (SIGKILL) 사용

## 예제:

kill 1234: PID 1234인 프로세스에 기본 종료 신호 (SIGTERM) 전송

kill -9 1234: PID 1234인 프로세스를 강제 종료 (SIGKILL)
