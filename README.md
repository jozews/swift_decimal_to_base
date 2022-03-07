# swift_decimal_to_base

```
var digits = [0]
var base = 2

for decimal in 1..<100 {

    for index in (0..<digits.count).reversed() {
        if digits[index] + 1 < base {
            digits[index] += 1
            break
        }
        else {
            digits[index] = 0
            if index == 0 {
                digits.insert(1, at: 0)
            }
        }
    }

    let str = digits.map{ String($0) }.joined(separator: "")
    print(decimal, str)
}

```
