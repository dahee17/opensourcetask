# **top**
---
* 시스템에서 프로세스 목록을 <span style="color:red">cpu 사용량</span> 이 높은 것부터 보여주는 명령어
* 시스템 프로세스와 메모리 사용 상태를 3초간격으로 업데이트하여 출력

* 실행 전 옵션
  *     -b : 순간의 정보를 출력(배치 모드)
  *     -n [num] : top 실행 주기를 num번 만큼 설정
  *     -p [pid]: process ID의 정보만을 출력
 
* 실행 후 옵션
  *  shift + p : cpu 사용률 내림차순
  *  shift + m : 메모리 사용률 내림차순
  *  shift + t : 프로세스가 실행되고 있는 시간 순서(시행된 시간이 큰 순서)
  *  k : 프로세스 종료

<img src="https://t1.daumcdn.net/cfile/tistory/99285B3F5B14C72B1E">

# **ps(process)**
---
* **현재 실행 중인 프로세스 목록과 상태를 보는 명령어**

* 옵션
  * ps -e : 실행중인 모든 프로세스 정보 출력(현재 사용자 뿐만 아니라 다른 사용자들까지)
  *    -f : 프로세스에 대한 자세한 정보 출력(부모프로세스 pid 확인가능)
  *    -l : -f보다 더 상세한 정보 출력
  *    -ef : 모든 프로세스를 풀 포맷으로 출

      >ps -e | grep abc

<img src="https://search.pstatic.net/common/?src=http%3A%2F%2Fcafefiles.naver.net%2FMjAyMDAzMTZfMTkw%2FMDAxNTg0MzE2Nzc5MTg4.YN2FwvuzTyJ5BZlikCUndSsmTmkKvrq1dy615VM0S3og.vtZr0oBdu28NwNbUBsekGfGDH4qD1Cx0qWI-65yixFwg.PNG%2Fps.PNG&type=sc960_832">

# **jobs**
---
* **작업의 상태를 표시하는 명령어**
* 현재 쉘 프로세스의 자식 백그라운 프로세스들을 보여줌

* 옵션
  *        -l : 프로세스 그룹 id를 state필드 앞에 출력
  *        -n : 프로세스 그룹 중에 대표 프로세스 id 출력
  *        -p : 각 프로세스 id에 대해 한 행씩 출력

      > jobs [option] [작업번호]

|출력 결과| |
|:---:|:---:|
|running|작업이 계속 진행|
|done|작업이 완료되어 0을 반환|
|stopped|작업이 일시 중단|


# **kill**
---
* **kill  : 프로세스를 지정하고 신호(signal)를 보내서 제어하는 명령어**
* 주로 프로세스를 종료하는 용도

* 옵션
  *        -9 : pid 지정하여 종료시 사용
  *        -l : 신호로 사용할 수 있는 신호이름들을 보여줌

> kill [option] [pid]
>> kill ps -ef | grep 프로세스이름 | grep -v grep | awk '{print $2}’






