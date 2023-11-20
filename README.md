# sleep-preprocessing


1. 수면 알고리즘 연구 방향

-2가지 수면 상태 분석 : 수면 시간 패턴, 심박 패턴

-day by day 수면 상태는 유사도에 대한 가중 평균으로 계산

-sleep = alpha * 수면 시간 유사도 + (1-alpha)*hr센서 유사도로 결정

-특정 기간 동안 비정상 수면 상태가 n번 이상 발생하면 알람

1)특징 정규화

![image](https://github.com/wlehd12/sleep-preprocessing/assets/125344095/a16bc687-5ca6-443c-a4a0-033eb80569de)


-특징값의 크기가 사람마다 다름 -> 0-1사이로 scaling

-하루 동안 분석해야하는 샘플수가 다름-> 1D subsampling 으로 하루 10000개로 샘플수 고정

-다양한 노이즈로 인해 원 신호와 복구한 신호의 차이 중 작은 차이가 있는 경우 역치 함수 적

![image](https://github.com/wlehd12/sleep-preprocessing/assets/125344095/692b09c4-a7c7-412e-84b6-87ed9c5ae5c1)



