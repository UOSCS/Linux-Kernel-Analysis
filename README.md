# Linux-Kernel-Analysis
Analyze the Linux Kernel.

##### 리눅스 커널 심층 분석 3e, 로버트 러브 지음 | 황정동 옮김, 에이콘

<hr>

## 목차
- [1주차 : 1. 리눅스 커널 입문 ~ 2. 커널과의 첫 만남](#1주차)
- [2주차 : 3. 프로세스 관리 ~ 4. 프로세스 스케줄링](#2주차)
- [4주차 : 6. 커널 자료구조](#4주차)
- [5주차 : 7. 인터럽트와 인터럽트 핸들러 ~ 8. 후반부 처리와 지연된 작업](#5주차)
- [6주차 : 9. 커널 동기화 개요 ~ 10. 커널 동기화 방법](#6주차)

<hr>

## 1주차 
- #### 주제
    - `monolithic kernel`과 `micro kernel`의 차이점은 무엇이고, 각각의 장단점은 무엇인가? 그리고, __리눅스__ 는 둘 중 어디에 가까운가?

    - 리눅스가 `Unix like (유닉스와 비슷하면서 유닉스가 아니다)`이라고 불리는 이유는 무엇인가?

    - 커널 메모리는 왜 __페이징 기능__ 을 사용할 수 없는가? 

    - `SMP`의 확장성이 낮은 이유는 무엇인가?
- #### [토론 내용](/Week_1/week1_0306.md)
- #### [노트 정리](/Week_1/week1_note.png)

## 2주차
- #### 주제
	- `x86 아키텍쳐`는 왜 레지스터를 아껴 써야 하는가?
	
	- __프로세스__ 와 __스레드__ 의 차이는 무엇인가?
		- `리눅스`에서 __스레드__ 개념을 별도로 정의하지 않고, 단지 *자원을 공유하는 프로세스* 의 형태로 구현하는 이유는 무엇인가?
	
	- 커널이 __부모프로세스__ 보다 __자식프로세스__ 를 의도적으로 먼저 실행해야 하는 이유는 무엇인가?
	
	- __CFS 스케줄러__ 는 __O(1) 스케줄러__ 의 어떤 문제점을 해결하였으며, __CFS 스케줄러__ 가 가지는 한계는 무엇인가?
		- __O(1) 스케줄러__ 는 어떤 부작용을 가지는가? 그러한 부작용을 가지는 이유는 무엇인가?
		- `리눅스`가 두 가지 별개의 우선순위 단위 *(나이스 값, 실시간 우선순위)* 를 가지는 이유는 무엇인가?
	
- #### [토론 내용](/Week_2/week2_0313.md)
- #### [노트 정리](/Week_2/week2_note.png)

## 4주차
- #### 주제
	- __리눅스의 연결리스트__ 가 __일반적인 연결리스트__ 보다 나은 점은 무엇인가?
	
	- 리눅스의 __레드블랙트리__ 가 __전통적인 레드블랙트리__ 와 다른 점을 설명하시오.
	
	- 리눅스의 `CFS스케줄러`가 `rbtree`를 사용하는 이유를 `rbtree`가 여타 자료구조와 비교하여 가지는 장점을 근거로 설명하시오.
	
	- 각 자료구조의 장단점을 기술하고, 사용되는 상황을 예시로 제시하시오.
	
- #### [토론 내용](/Week_4/week4_0327.md)
- #### [노트 정리](/Week_4/week4_note.png)

## 5주차
- #### 주제
	- `하드웨어` 에 __인터럽트__ 가 발생한 시점부터 __인터럽트__ 처리 후 이전에 실행되던 작업으로 돌아가기까지의 과정을 상세히 설명하시오.
	
	- __전역 cli()함수__ 를 제거한 가장 결정적인 이유를 설명하시오.
	
	- __인터럽트 처리__ 를 할 때 __전반부__ 와 __후반부__ 를 구분하는 이유를 설명하시오.
	
	- `softirq`, `tasklet`, `workqueue`에 대해 설명하시오.
	
- #### [토론 내용](/Week_5/week5_0403.md)
- #### [노트 정리](/Week_5/week5_note.png)

## 6주차
- #### 주제
	- `스핀락`과 `세마포어`의 특징을 설명하고, `스핀락`과 `세마포어` 각각을 어느 조건 속에서 사용하면 좋은지를 둘의 차이점을 근거로 하여 설명하시오.
	
	- 재귀적인 락은 어떻게 구현되며 언제 사용하는가?
	
	- __배리어__ 의 필요성을 설명하고 배리어 함수들의 기능에 대해 논하시오.
	
	- 락을 구현할 때 신경써야 할 사항들에는 어떤 것들이 있는지 논하시오.
	
- #### [토론 내용](/Week_6/week6_0501.md)
- #### [노트 정리](/Week_6/week6_note.png)

