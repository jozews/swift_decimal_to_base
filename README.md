# swift_decimal_to_base

Count to N in any base lower than 10

```
let N = 100
let base = 2

var digits = [0]

for decimal in 1..<N {

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
