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
