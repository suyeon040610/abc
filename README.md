# top
+ 시스템의 상태를 실시간으로 확인
+ 프로세스의 CPU, 메모리, 스왑 등의 사용량을 파악할 수 있음
---
##### 옵션 없이 실행

`$ top`

![3](https://github.com/suyeon040610/abc/assets/166946373/da8365eb-a219-41d6-97eb-ae2f5c9ca3d9)


+ PID : 프로세스 ID
+ USER : 프로세스를 실행시킨 사용자 ID
+ PRI : 프로세스 우선순위 (priority)
+ NI : NICE 값. 일의 nice value 값. 마이너스를 가지는 nice value는 우선순위가 높음
+ VIRT : 가상 메모리의 사용량 (SWAP + RES)
+ RES : 현재 페이지가 상주하고 있는 크기 (Resident Size)
+ SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합
+ S : 프로세스의 상태 (S-sleeping, R-running, W-swapped out process, Z-zombies)
+ %CPU : 프로세스가 사용하는 CPU의 사용율
+ %MEM : 프로세스가 사용하는 메모리 사용율
+ COMMAND : 실행된 명령어

---

##### 명령어 옵션
+ `-u username` : 사용자 이름으로 식별된 특정 사용자에 대한 프로세스만 표시
+ `-d seconds` : 업데이트 사이의 지연 시간을 초 단위로 지정 (기본값은 3초)
+ `-n number` : 명령어가 종료되기 전의 반복 횟수(업데이트)를 지정
+ `-b` : 스크립트에 유용한 배치 모드에서 명령을 실행
+ `-c` : 명령 이름을 실행 파일 이름이 아닌 "COMMAND" 열에 표시

---
---

# ps
+ Process State의 약자로 현재 실행 중인 프로세스와 상태를 출력하는 명령어
+ _보통 grep 명령어와 많이 사용됨_

---
##### 옵션 없이 실행

`$ ps`

![2](https://github.com/suyeon040610/abc/assets/166946373/2a35b55b-5d94-4046-b66b-408165d0bfd4)

+ PID : 프로세스의 식별 번호
+ TTY : 프로세스와 연결된 터미널
+ TIME : 총 CPU 사용 시간
+ COMMAND : 프로세스의 실행 명령행

---

##### 명령어 옵션
+ `-A` : 모든 프로세스를 출력
+ `-e` : 커널 프로세스를 제외한 모든 프로세스 출력
+ `-r` : 현재 실행 중인 프로세스 출력
+ `-p` : 특정 PID를 지정하여 출력

---
---

# jobs
+ 작업의 상태를 표시하는 명령어
+ 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력
+ 각 작업에는 번호가 붙어 있어 kill 명령어 뒤에 '%번호' 등으로 사용할 수 있음

---
##### 옵션 없이 실행

`$ jobs`

![5](https://github.com/suyeon040610/abc/assets/166946373/407e21df-aa2d-432b-856c-f3e1031adc56)


_단, 실행중인 작업이 없다면 아무것도 출력되지 않음_

![4](https://github.com/suyeon040610/abc/assets/166946373/fe201489-f57c-4d4e-a5b1-ef6d00d6f9a4)

---
##### 명령어 옵션
+ `-l` : 프로세스 ID와 함께 잡 목록을 출력
+ `-n` : 마지막 알림 이후 변경된 잡만 출력
+ `-p` : 잡의 프로세스 ID만 출력
+ `-r` : 실행 중인 잡만 출력
+ `-s` : 중지된 잡만 출력

---
---

# kill
+ 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어
+ 대개는 프로세스를 죽일 때 사용

---
##### 사용하는 방법
`kill [pid]`
죽이려는 프로세스의 pid를 얻은 다음 kill 명령어의 인자로 넘기면 됨

![6](https://github.com/suyeon040610/abc/assets/166946373/9a4e3b67-96b8-4629-8aac-71bad9c45e98)

---
##### 명령어 옵션
+ `-9`   : 프로세스를 제거
+ `-15`  : 프로세스를 정상적으로 중지
+ `-l`   : 사용 가능한 모든 신호 목록을 가져옴
