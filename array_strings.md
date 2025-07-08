### 🔹 **Array and strings**

1. Find duplicate in an array single or multiple
    
    ```
    Array
    (
        [0] => 2
        [1] => 3
        [2] => 1
    )
    ```
    
    ### ✅ **Solution:**
    ```php
    function findDuplicate($array){
        $seen = [];
        $duplicates = [];
    
        foreach ($array as $value) {
            if (isset($seen[$value])) {
                $duplicates[$value] = true;
            }else {
                $seen[$value] = true;
            }
        }
        return array_keys($duplicates);
    
    }

    print_r(findDuplicate([1, 2, 3, 4, 2, 5, 3, 6, 1]));
    ```
---

2. Find the missing number from 1 to N
    
    ```
    Missing number: 3
    ```
    
    ### ✅ **Solution:**
    ```php
    function findMissingNumber($arr, $n){
        $expectedSum = $n * ($n + 1) / 2;
        $actualSum = array_sum($arr);
    
        return $expectedSum - $actualSum;
    }

    $arr = [1, 2, 4, 5]; // n = 5
    echo "Missing number: " . findMissingNumber($arr, 5);
    ```
---

3. Reverse a string without using built-in functions
    
    ```
    reeta: ateer
    ```
    
    ### ✅ **Solution:**
    ```php
    function reverseString($str){
        $reversed = "";
        $length = 0;
    
        // Count characters without using strlen
        while (isset($str[$length])) {
            $length++;
        }
    
        // Reverse manually
        for ($i = $length - 1; $i >= 0; $i--) {
            $reversed .= $str[$i];
        }
    
        return $reversed;
    }

    echo reverseString("reeta");
    ```
---

3. Reverse a string without using built-in functions
    
    ```
    malayalam is a palindrome
    ```
    
    ### ✅ **Solution:**
    ```php
    function isPalindrome($str) {
        $len = strlen($str);
    
        for ($i = 0; $i < $len / 2; $i++) {
            if ($str[$i] !== $str[$len - 1 - $i]) {
                return false;
            }
        }
    
        return true;
    }

    $input = "malayalam";
    echo isPalindrome($input) ? "$input is a palindrome" : "$input is not a palindrome";
    ```
---
