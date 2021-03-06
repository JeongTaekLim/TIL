# 프로세스와 쓰레드의 차이

출처 - https://gmlwjd9405.github.io/2018/09/14/process-vs-thread.html

## 프로세스란

> 컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램

- 메모리에 올라와있고, 실행되고 있는 프로그램의 인스턴스(독립적인 개체)
- 운영체제로부터 시스템 자원을 할당받는 작업의 단위
- CPU 시간, 메모리 주소공간, Code, Data, Stack, Heap의 구조로 되어있는 독립된 메모리영역
- 각 프로세스는 별도의 주소 공간에서 실행되며, 한 프로세스는 다른 프로세스의 변수나 자료구조에 접근할 수 없다.
- 한 프로세스가 다른 프로세스의 자원에 접근하려면 프로세스간의 통신(IPC) 를 사용해야 한다. - Ex. 파이프, 파일, 소켓 등을 이용한 통신방법

## 쓰레드란

> 프로세스 내에서 실행되는 여러 흐름단위

- 프로세스가 할당받은 자원을 이용하는 실행의 단위
- 쓰레드는 프로세스 내에서 각각 Stack만 따로 할당받고 Code, Data, Heap 영역은 공유한다.
- 쓰레드는 한 프로세스 내에서 동작되는 여러 실행의 흐름으로, 프로세스 내의 주소 공간이나 자원들(힙 공간 등) 같은 프로세스 내에 쓰레드끼리 공유하면서 실행된다.
- 같은 프로세스 안에 있는 여러 쓰레드들은 힙 공간을 공유한다.
