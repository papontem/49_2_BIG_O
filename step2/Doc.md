## Step Two: Calculating Time Complexity

Determine the time complexities for each of the following functions. If you’re not sure what these functions do, copy and paste them into the console and experiment with different inputs!

    function logUpTo(n) {
        for (let i = 1; i <= n; i++) {
            console.log(i);
        }
    }

Time Complexity: logUpTo(n) is linear O(n), it is not a constant as it will take longer depending on the value of n.
---

    function logAtLeast10(n) {
        for (let i = 1; i <= Math.max(n, 10); i++) {
            console.log(i);
        }
    }

Time Complexity: f(n) is linear O(n) it will print 10 when n is lower than ten but were meassuring for the worst case, being O(n) not O(1).
---

    function logAtMost10(n) {
        for (let i = 1; i <= Math.min(n, 10); i++) {
            console.log(i);
        }
    }

Time Complexity: f(n) is constant O(1) it will never go past 10 iterations
---
    function onlyElementsAtEvenIndex(array) {
        let newArray = [];
        for (let i = 0; i < array.length; i++) {
            if (i % 2 === 0) {
            newArray.push(array[i]);
            }
        }
        return newArray;
    }

Time Complexity: f(n) is linear O(n) , were going through an array and half of the time were executing another command, and updating a value in memory, so it would be something like n/2 .... no? simpified is n as we expand to infinity 
---
    function subtotals(array) {
        let subtotalArray = [];
        for (let i = 0; i < array.length; i++) {
            let subtotal = 0;
            for (let j = 0; j <= i; j++) {
                subtotal += array[j];
            }
            subtotalArray.push(subtotal);
        }
        return subtotalArray;
    }

Time Complexity: f(n) is quadratic O(n^2) as were lopping throught the array twice, and the second time were pushing the addition of each element before to a value in memory,  
---
    function vowelCount(str) {
        let vowelCount = {};
        const vowels = "aeiouAEIOU";

        for (let char of str) {
            if(vowels.includes(char)) {
                if(char in vowelCount) {
                    vowelCount[char] += 1;
                } else {
                    vowelCount[char] = 1;
                }
            }
        }

    return vowelCount;
    } 

Time Complexity: f(n) is linear O(n) were only looping once through the string and time depends on the length of the string when extended to inifinity..