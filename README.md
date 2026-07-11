# Zoho_Mentor
### 2193. Minimum Number of Moves to Make Palindrome
```java
public class Solution{
    public static int find(char[] arr,int k,char ch)
    {
        for(int i=k;i>=0;i--)
        {
            if(arr[i] == ch) return i;
        }
        return 0;
    }
    public static int minMovesToMakePalindrome(String s) {
        int l = 0;
        int r = s.length()-1;
        int ans = 0;
        char[] arr = s.toCharArray();
        while(l<r)
        {
            if(arr[l] == arr[r])
            {
                l++;
                r--;
            }
            else
            {
                int k = r;
                int idx = find(arr,k,arr[l]);
                if(idx != l)
                {
                    while(idx<r)
                    {
                        ans++;
                        char ch = arr[idx];
                        arr[idx] = arr[idx+1];
                        arr[idx+1] = ch;
                        idx++;
                    }
                }
                else
                {
                    ans++;
                    char temp = arr[l];
                    arr[l] = arr[l+1];
                    arr[l+1] = temp;
                }
            }
        }
        return ans;
    }
}public class Solution{
    public static int find(char[] arr,int k,char ch)
    {
        for(int i=k;i>=0;i--)
        {
            if(arr[i] == ch) return i;
        }
        return 0;
    }
    public static int minMovesToMakePalindrome(String s) {
        int l = 0;
        int r = s.length()-1;
        int ans = 0;
        char[] arr = s.toCharArray();
        while(l<r)
        {
            if(arr[l] == arr[r])
            {
                l++;
                r--;
            }
            else
            {
                int k = r;
                int idx = find(arr,k,arr[l]);
                if(idx != l)
                {
                    while(idx<r)
                    {
                        ans++;
                        char ch = arr[idx];
                        arr[idx] = arr[idx+1];
                        arr[idx+1] = ch;
                        idx++;
                    }
                }
                else
                {
                    ans++;
                    char temp = arr[l];
                    arr[l] = arr[l+1];
                    arr[l+1] = temp;
                }
            }
        }
        return ans;
    }
}
```







# C/C++ Output Prediction Questions

A well-organized collection of C/C++ output prediction, pointers,
strings, loops, control flow, structures, unions, arrays, functions,
macros, and miscellaneous interview questions.

> **Note:** The technical content is preserved. This file focuses on
> improving readability and GitHub presentation.

## Table of Contents

-   Pointers
-   Strings
-   Loops
-   Complex and Nested Loops
-   Control Flows

------------------------------------------------------------------------

## Questions

> Paste the original questions here. The formatting style should be:

### Question N

``` c
// code
```

**Output**

``` text
...
```

**Explanation**

-   Point 1
-   Point 2

------------------------------------------------------------------------

Repeat for all questions.

