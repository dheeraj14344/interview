
# Answers
--------------------

### 🔹 **Pattern Printing**

1. Centered Pyramid Pattern (*)
    
    ```
        *    
       ***   
      *****  
     ******* 
    *********
    ```
    
    ### ✅ **Solution:**
    ```php
    function pyramid($n){
        for ($i=1; $i <= $n; $i++) { 
            echo str_repeat(" ", $n - $i);
            echo str_repeat("*", 2 * $i -1);
            echo PHP_EOL;
        }
    }
    
     pyramid(5);
    ```
    ---

2. Inverted Pyramid
    
    ```
    *********
     *******
      *****
       ***
        *
    ```
    
    ### ✅ **Solution:**
    ```php
    function reversePyramid($n){
      for ($i = $n; $i >= 1; $i--) { 
          echo str_repeat(" ", $n - $i);
          echo str_repeat("*", 2 * $i - 1);
          echo PHP_EOL;
      }
    }
    
     pyramid(5);
    ```
    ---
