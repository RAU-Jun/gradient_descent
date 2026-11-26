# 경사 하강법 (Gradient Descent) 직접 구현

라이브러리 없이 손실 함수 **y = x²** 의 최솟값을 경사 하강법으로 찾아가는 과정을 구현했습니다.

- 언어: Python (외부 라이브러리 없음)
- Claude AI는 github 정리에만 사용, 코드 작성에는 미사용함.

```
src/
  gradient_descent_x2.py   # 경사 하강법 구현
results/
  output.txt               # 100번 반복한 출력 결과
```

## 방법

- 손실 함수 `L(x) = x²`, 기울기 `L'(x) = 2x`
- 초기값 x = 10, 학습률 0.1, 100회 반복
- 갱신식: `x ← x − 학습률 × L'(x)`  → 매 반복마다 x가 0.8배씩 줄어듦

## 결과

| 반복 | x | Loss |
|---|---|---|
| 1 | 8.0 | 64.0 |
| 2 | 6.4 | 40.96 |
| 5 | 3.2768 | 10.737 |
| 100 | 2.04 × 10⁻⁹ | 4.15 × 10⁻¹⁸ |

x가 최솟값 위치인 0에 수렴하는 것을 확인했습니다. 전체 출력은 [`results/output.txt`](results/output.txt)에 있습니다.

## 실행 방법

```bash
python src/gradient_descent_x2.py
```
