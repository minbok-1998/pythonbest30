- info
  - lv1
  - 조합

# 알리는 포케가 좋아
![알리의 포케 가게](./10_1.webp)

## 문제 설명
개리가 스페이스 스톤을 사용하여 노역장에서 동족을 구하고 구출된 동족들은 자유를 얻었습니다. 노역장에서 데이터분석을 하던 알리는 평소 좋아하던 포케 가게를 열었습니다.
친절한 알리는 손님이 원하는 토핑의 수와 꼭 들어가야 할 토핑을 말하면 만들 수 있는 모든 포케의 조합을 안내합니다.

포케에 넣을 수 있는 토핑은 아래와 같습니다.

```text
연어, 참치, 닭가슴살, 베이컨, 버섯
```

손님은 토핑을 최대 5개까지 고를 수 있으며, 꼭 들어가야 할 토핑도 고를 수 있습니다. 알리는 주문에 맞는 포케의 조합을 안내해야 합니다.

단, 아무것도 입력하지 않을 경우 `“기본 포케가 제공됩니다.”`라고 안내해야 합니다.

---

## 제한 사항

- 0 ≤ 토핑 수 ≤ 5
- 토핑은 안내된 토핑 중 선택해야 합니다. (연어, 참치, 닭가슴살, 베이컨, 버섯)

---

## 입출력 예

| 입력              | 출력                                                                                                                                                                                                                                                                       |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| []                | “기본 포케가 제공됩니다.”                                                                                                                                                                                                                                                  |
| [2, “연어”]       | [["연어", "참치"], ["연어", "닭가슴살"], ["연어", "베이컨"], ["연어", "버섯"]]                                                                                                                                                                                             |
| [3, “연어, 참치”] | [["연어", "참치", "닭가슴살"], ["연어", "참치", "베이컨"], ["연어", "참치", "버섯”]]                                                                                                                                                                                       |
| [3, “”]           | [["연어", "참치", "닭가슴살"], ["연어", "참치", "베이컨"], ["연어", "참치", "버섯"], ["연어", "닭가슴살", "베이컨"], ["연어", "닭가슴살", "버섯"], ["연어", "베이컨", "버섯"], ["참치", "닭가슴살", "베이컨"], ["참치", "닭가슴살", "버섯"], ["닭고기", "베이컨", "버섯"]] |

---

## 입출력 설명

- 토핑의 수와 토핑을 입력받습니다.
- 토핑의 수는 0부터 5까지 입력할 수 있습니다. 또한, 토핑은 안내된 토핑(연어, 참치, 닭가슴살, 베이컨, 버섯)에서 선택해야 하며, 문자열로 입력받습니다.
- 토핑을 선택하지 않을 경우는 빈 문자열로 입력합니다.
- 토핑의 조합은 배열로 출력합니다.

<br/>

### 1. 아무것도 입력하지 않을 경우

아무것도 입력하지 않은 경우, 즉 빈 배열([])이 입력된 경우는 토핑의 수는 0개, 원하는 토핑은 없는 것으로 간주합니다. 따라서 **"기본 포케가 제공됩니다.”**가 출력됩니다.
<br/>

### 2. 토핑의 수와 토핑 모두 입력된 경우

예를 들어 토핑의 수가 2, 꼭 들어가야 할 토핑으로 “연어”가 입력되었다면,

5개의 토핑 중 “연어”가 포함된 2개의 토핑을 선택해야 하므로 해당하는 모든 조합은 아래와 같습니다.

```text
[["연어", "참치"], ["연어", "닭가슴살"], ["연어", "베이컨"], ["연어", "버섯"]]
```

<br/>

### 3. 토핑을 입력하지 않은 경우

예를 들어 토핑의 수로 3이 입력되었지만, 토핑은 입력되지 않는다면 
5개의 토핑 중 필수로 포함하는 토핑 없이 3개를 선택해야 합니다. 그 조합은 아래와 같습니다.


```text
[["연어", "참치", "닭가슴살"], ["연어", "참치", "베이컨"], ["연어", "참치", "버섯"],
["연어", "닭가슴살", "베이컨"], ["연어", "닭가슴살", "버섯"], ["연어", "베이컨", "버섯"],
["참치", "닭가슴살", "베이컨"], ["참치", "닭가슴살", "버섯"], ["닭고기", "베이컨", "버섯"]]
```
