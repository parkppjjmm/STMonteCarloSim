Monte Carlo 시뮬레이션에서 사용된 변수

- mu (μ):
의미: 평균 일일 로그 수익률 (mean of daily log returns)
설명: 주식의 평균적인 일일 수익률을 나타냅니다. 로그 수익률을 사용함으로써 수익률이 일정한 시간 간격마다 동일한 분포를 갖도록 보장합니다.
계산 방법: 과거 주가 데이터에서 일일 로그 수익률을 계산한 후 그 평균값을 사용합니다.
예시 값: 0.0005

- sigma (σ):
의미: 일일 로그 수익률의 표준 편차 (standard deviation of daily log returns)
설명: 주식 수익률의 변동성을 나타냅니다. 수익률의 표준 편차가 클수록 주가의 변동성이 크다는 것을 의미합니다.
계산 방법: 과거 주가 데이터에서 일일 로그 수익률의 표준 편차를 계산합니다.
예시 값: 0.02

- num_simulations:
의미: 시뮬레이션 횟수 (number of simulations)
설명: Monte Carlo 시뮬레이션을 수행할 때 생성할 주가 경로의 수입니다. 더 많은 시뮬레이션을 수행할수록 결과의 신뢰도가 높아집니다.
예시 값: 1000

- time_horizon:
의미: 시뮬레이션 기간 (time horizon)
설명: 시뮬레이션이 진행되는 시간 기간을 나타냅니다. 일반적으로 거래 일수로 계산하며, 1년은 약 252개의 거래일로 구성됩니다.
예시 값: 252 (1년간의 거래일 수)




[결과]

![output](https://github.com/parkppjjmm/Monte-Carlo-Simulation/assets/56201670/1420d1f8-4ab6-410d-b567-14b7a1397e1b)




mu와 sigma 계산:
- 과거 주가 데이터를 사용하여 일일 로그 수익률을 계산합니다.
- Log Return = ln(P(t)/P(t-1))
- mu는 이 로그 수익률의 평균값, sigma는 표준 편차를 의미합니다.
 
※ Mean Final Price (평균 최종 주가):
의미: 시뮬레이션의 모든 경로에서 1년 후의 주가의 평균값입니다.
설명: 다양한 시뮬레이션 경로를 통해 예상되는 평균 주가를 나타냅니다. 이는 주가의 미래 가치를 평균적으로 평가하는 데 도움이 됩니다.

※ Median Final Price (중앙값 최종 주가):
의미: 시뮬레이션 경로에서 1년 후 주가의 중앙값입니다.
설명: 중앙값은 시뮬레이션 경로의 중간값으로, 절반의 경로가 이 값보다 낮고 나머지 절반이 이 값보다 높습니다. 이는 주가가 균등하게 분포되었을 때의 중간값을 나타냅니다.

※ 25th Percentile (25번째 백분위수):
의미: 시뮬레이션 경로에서 1년 후 주가의 25번째 백분위수 값입니다.
설명: 이 값은 주가가 시뮬레이션 경로의 하위 25% 내에 있는 주가 수준을 나타냅니다. 즉, 시뮬레이션 경로의 25%가 이 값보다 낮고 나머지 75%가 이 값보다 높습니다. 이는 주가의 하락 위험을 평가하는 데 유용합니다.

※ 75th Percentile (75번째 백분위수):
의미: 시뮬레이션 경로에서 1년 후 주가의 75번째 백분위수 값입니다.
설명: 이 값은 주가가 시뮬레이션 경로의 상위 25% 내에 있는 주가 수준을 나타냅니다. 즉, 시뮬레이션 경로의 75%가 이 값보다 낮고 나머지 25%가 이 값보다 높습니다. 이는 주가의 상승 잠재력을 평가하는 데 유용합니다.

[요약]
- 평균 최종 주가는 모든 시뮬레이션 경로의 평균값으로, 주가의 예상되는 평균 수준을 나타냅니다.
- 중앙값 최종 주가는 중간값으로, 주가가 균등하게 분포되었을 때의 중간값을 제공합니다.
- 25번째 백분위수는 하위 25% 경로의 주가 수준을 나타내며, 주가의 하락 위험을 평가합니다.
- 75번째 백분위수는 상위 25% 경로의 주가 수준을 나타내며, 주가의 상승 잠재력을 평가합니다.
