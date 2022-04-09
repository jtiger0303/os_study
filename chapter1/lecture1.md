## Issue #1 (I/O) ##
#### How to perform I/Os efficiently? ####

1) I/O devices and CPU can execute concurrently.
- I/O가 시간이 오래 걸리기 때문에 CPU는 놀고 있다.

2) Each device controller has a local buffer(device driver가 관리).
3) CPU is a precious resource so it should be freed from time-consuming.
- 다른 device들이 cpu를 잘 활용할 수 있겠끔 해야 하고, 그 결과 device 효율이 늘어난다.

### Interrupt ###
- polling: 중간에 CPU가 계속해서 물어보는 방식(효율성이 떨어지고, 이 것을 보완해주기 위한 방법: interrupt)
- *Hardware Interrupt*: 연산이 끝났음을 프로세스한테 알려주는 방식(효율성이 좋다)

### Interrupt Handling ###
- 무엇을 수행하고 있는 지 정보 저장이 필요

## Issue #2 (Protection) ##
- how to prevent user applications from harming the system?

- What if application accesses disk drives directly?/application executes the HLT instruction?(더 이상 실행할게 없으면-> idle)

- Operating System에 의해서만 수행 가능

### Protected Instructions(a.k.a privileged instructions[ex: HLT]) ###
1) cannot be done from user mode(application)

2) Direct I/O Access, Accessing system registers, memory state management 수행하려고 할 시에 cpu에 interrupt 발생

* Kernel mode vs user mode 
- mode: application이 돌 때는 비트 3/ system call 할 때에는 비트 1
- protected instruction은 오직 kernel mode에서만 사용 가능

## Issue #3 (Servicing Requests) ##
1) How to ask services to the OS? (Control을 os로 넘겨준다)

2) User program들은 OS에 요청 필수

- USER: Load, Store, add, INC(파일에서 읽어오고 싶다)->system call[ex) read()]
- Kernel



