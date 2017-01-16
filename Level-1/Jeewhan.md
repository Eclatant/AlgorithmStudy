[x만큼 간격이 있는 n개의 숫자](http://tryhelloworld.co.kr/challenge_codes/135)

```python
def number_generator(x, n):
    arr = [x]
    for i in range(1, n):
        arr.append(x + i * x)
    return arr

print(number_generator(3,5))

# 배워야 할 풀이

def number_generator(x, n):
    return [i * x + x for i in range(n)]
print(number_generator(2, 5))

def number_generator(x, n):
    return list(range(x, n * x + 1 , x))
```

[핸드폰번호 가리기](http://tryhelloworld.co.kr/challenge_codes/132)

```javascript
function hide_numbers(s){
  var result = ""
  for (let i = 0; i < s.length - 4; i++) {
    result += "*";
  }
  result += s.slice(-4);
  
  return result;
}

console.log("결과 : " + hide_numbers('01033334444'));

// 배워야 할 풀이

function hide_numbers(s) {
  return s.replace(/\d(?=\d{4})/g, "*");
}

function hide_numbers(s){
  return Array(10).join('*').substr(0,s.length - 4) + s.substr(s.length - 4, 4);
}
```
