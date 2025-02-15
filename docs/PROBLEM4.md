## 🚀 기능 요구 사항

어느 연못에 엄마 말씀을 좀처럼 듣지 않는 청개구리가 살고 있었다. 청개구리는 엄마가 하는 말은 무엇이든 반대로 말하였다.

엄마 말씀 word가 매개변수로 주어질 때, 아래 청개구리 사전을 참고해 반대로 변환하여 return 하도록 solution 메서드를 완성하라.

| A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Z | Y | X | W | V | U | T | S | R | Q | P | O | N | M | L | K | J | I | H | G | F | E | D | C | B | A |

### 제한사항

- word는 길이가 1 이상 1,000 이하인 문자열이다.
- 알파벳 외의 문자는 변환하지 않는다.
- 알파벳 대문자는 알파벳 대문자로, 알파벳 소문자는 알파벳 소문자로 변환한다.

### 실행 결과 예시

| word | result |
| --- | --- |
| "I love you" | "R olev blf" |

### 기능 목록
1. word의 첫번째 문자부터 마지막 문자까지 반복하며 각 문자가 알파벳인지 아닌지 확인한다.
2. 알파벳이라면 26개의 알파벳을 13개씩 두개의 영역으로 구분해 기준을 중앙에 제일 가까운 알파벳으로 삼는다. 
   왼쪽 알파벳의 기준-M(m), 오른쪽 알파벳의 기준-N(n)
3. 해당 알파벳이 왼쪽(앞쪽) 알파벳인지, 오른쪽(뒷쪽) 알파벳인지 구분한다.
4. 알파벳이 속한 영역의 기준으로 부터 떨어져 있는 거리를 구하고, 그 거리만큼 반대쪽 영역의 기준으로부터 그 거리만큼 떨어져 있는 문자로 변경한다.
5. 변환된 모든 알파벳과 변환되지 않은 알파벳이 아닌 문자열들을 모두 합친 문자열을 리턴한다.