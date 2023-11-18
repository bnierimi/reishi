## t/Reishi
[_yours bnierimi_](https://bnierimi.vercel.app)

- Website: ...
- Release: ...
- License: ...


### Sample code
```py
# Types
integer, float, bytes

# String
"This is a string"
```

```py
# # Multi line | Docstring
`this
is for
docstring`
"""
if backtick ` not in 256 ASCII characters
    then this
"""
```

```py
# Chars
'f'

# Bytes
b'f'

# Hex
0x12d3ef2e87f72f7d23e6de6f

# Oct
0o123234342342342342334327

# Oct
0b101011101010010010110010

# Booleans
True or False

# Others
* None | Nil | Null | Void
Any

# Booleans
is_hungry = False
is_alive = True

# Enums
enums Fruits{
    Berry=1,
    Pineapple,
    Mango,
    Apple,
}
```

```py
# Seq Types
# List
[1, 2, True, "Room"]
basket: string[] = ["Berry", "Mango", "Apple"]
basket: <string | boolean>[3]{string boolean string} = ["Berries", True, "Onions"]

* # # Tuple
# ()

# Array: Matrix
# Shape default[1 Row]
angle: array[1] = (1, 2, 3, 4, 5)

# Shape [Row Colomn]
angle: array[2][2, 2] = ([1, 2],
                         [3, 4])

# Shape [Row Colomn]
angle: array[3][3, 2] = ([[1, 2, 3],
                          [4, 5, 6]],
                         [[4, 5, 6],
                          [7, 8, 9]],
                         [[7, 8, 9],
                          [0, 1, 2]])
                            
my_array.transpose()
```

```py
# Type Convertion
matrix = Matrix(array_one)
matrix.transpose()

# # Using the as function
as(matrix, array_one).transpose()
```

```py
# Dictionary
dictionary = {
    0: "Yeagerist",
    1: "Espada",
    2: "Kaizoku",
}
dictionary[0]

# Variable Declarations
name = "Radiance Babajide"
age: int = 20

# Constants
const YONKO = "tsurgeon"
const MAX_SCORE: int = 100
const{
    NAKAMA = "Corazon"; YEARS: <int | float> = 2
}
```

```py
# Interfaces
interface Address{address: hex}
interface Account{
    name: string
    wallet_address: Address
    public_key: oct
}
* interface Point{
    x, y: int
}

my_account = Account{
    name: "Akagami"
    wallet_address: Address{0x308d3ef2e87f72f7d23e6de6}
    public_key: 0o123234342342342342334327
}
print(my_account.public_key)
```

```py
# Control flow
## Conditional Statements
if x >= 32{
    ...
} elif 25 <= x < 31{
    ...
} else{
    ...
} then{}

# # Match | Switch Statements
match x {
    case MAX_SCORE{}
    else{}
}then{}

# Loops
for x in range(1){
    print(x)
}
for x in 0..5{
    print(x)
}
for i, x in [0, 10, 20, 30]{
    print(i, x)
}

* loop {
    x == 2: break | continue
}

x = 0
running = True
while running {
    break if x == 2
    x += 1
}

r = 0
while r < 10 {
    print(r)
}
```

```py
break if x == 2 else print(False)
```

```py
# Functions Definition
def main(){ # returns None by default
    print("")
}

def like(id: hex, *args, **kwargs) -> bool{
    # args -> a list
    # kwargs -> a dictionary
    return False
}


# OOP
class BornAgain(Object){
    def __init__(name) -> None{}
}
```

```py
# Package | Module
import stdio as io
import "bnierimi/reiatsu" as reiatsu
from math import factorial as fact
from "https://github.com/bnierimi/reiatsu" import pressure as ps
# fetch pressure from "https://github.com/bnierimi/reiatsu" as reiatsu
```

```py
# Contracts: Creating contracts
interface Party{
    name: string,
    id: hex,
}

interface Item{
    id: hex,
    name: string,
    quatity: int,
    unitPrice: float,
}

interface Contract {
    seller: Party
    buyer: Party
    offer: {
        by: Party,
        items: Item[],
        amount: float
    }
    acceptance: {
        by: Party,
        timestamp: string
    }
    consideration: {
        amount: float,
        method: string
    }
    capacity: {
        sellerCapacity: bool,
        buyerCapacity: bool,
    }
    purpose: {
        buyerPurpose: string,
        sellerApproval: bool
    }
    mutuality: bool
    certainty: bool
    type: "written" | "oral"
    terms: list
}

class SalesContract(Contract) {
    def __init__(self, seller: Party, buyer: Party):
        self.seller = seller
        self.buyer = buyer
}
```
