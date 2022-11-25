### Task 8 kyu

[Task link](https://www.codewars.com/kata/5951d30ce99cf2467e000013/)

Description:

Given an unsorted array of 3 positive integers [ n1, n2, n3 ], determine if it is possible to form a Pythagorean Triple using those 3 integers.

A Pythagorean Triple consists of arranging 3 integers, such that:

a2 + b2 = c2
Examples

[5, 3, 4] : it is possible to form a Pythagorean Triple using these 3 integers: 32 + 42 = 52

[3, 4, 5] : it is possible to form a Pythagorean Triple using these 3 integers: 32 + 42 = 52

[13, 12, 5] : it is possible to form a Pythagorean Triple using these 3 integers: 52 + 122 = 132

[100, 3, 999] : it is NOT possible to form a Pythagorean Triple using these 3 integers - no matter how you arrange them, you will never find a way to satisfy the equation a2 + b2 = c2
Return Values

    For Python: return True or False
    For JavaScript: return true or false
    Other languages: return 1 or 0 or refer to Sample Tests.






### My solution

```Java

import java.util.Arrays;

public class PythagoreanTriple {

    public int pythagoreanTriple(int[] triple) {

        if (triple[0] * triple[0] + triple[1] * triple[1] == triple[2] * triple[2] | triple[0] * triple[0] + triple[2] * triple[2] == triple[1] * triple[1] || triple[2] * triple[2] + triple[1] * triple[1] == triple[0] * triple[0]) {
            return 1;
        } else return 0;
    }
}

```

### Favourite solution from code-wars

```Java

class PythagoreanTriple {
    int pythagoreanTriple(final int[] triple) {
        final int a2 = triple[0]*triple[0];
        final int b2 = triple[1]*triple[1];
        final int c2 = triple[2]*triple[2];
        return a2 + b2 == c2 || a2 + c2 == b2 || b2 + c2 == a2 ? 1 : 0;
    }
}

```

I like this syntax construction, I mean using ? instead of if

# Have a nice day!