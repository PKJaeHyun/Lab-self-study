# Outline of "Neural ODE"
<https://arxiv.org/abs/1806.07366>
---
## Idea

기존의 Residual Network는 결국 discrete한 hidden state를 통과하고, 그 과정은 아래와 같은 수식으로 나타낸다.

$$ h_t+1 = h_t+f(h_t,\theta_t) $$

여기서 t의 간격(step)을 줄이면

$$ \frac{dh(t)}{dt} = f(h(t),t,\theta) $$

라는 ODE로 hidden unit의 continuous 한 dynamics를 표현할 수 있다. 결국 t=0의 Input Layer h(0)에서 시작해서, t=T의 Output Layer h(T)를 ODE로 계산하는 문제로 바뀐다.

***여기서 의문점***

1. hidden state를 f라는 함수로 이렇게 간단하게 표현할 수 있는가? 항상?
2. f가 uniformly Lichitz continuous 하다는 가정을 하는데 현실의 모델들도 이를 만족하는가?


