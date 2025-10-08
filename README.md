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
