# 1221.-Split-a-String-in-Balanced-Strings

Balanced strings are those who have equal quantity of 'L' and 'R' characters.

Given a balanced string s split it in the maximum amount of balanced strings.

Return the maximum amount of splitted balanced strings.

````c#

public class Solution {
    public int BalancedStringSplit(string s) {

        int res = 0;
        int len = 0;
        int rel = 0;
        
        for(int i=0; i<s.Length; i++)
        {
            
            if(s[i] == 'R'){
               ++rel;             
            }
            if(s[i] == 'L'){
                ++len;
            }
            
             if(len == rel && len > 0)
            {
                rel = 0; 
                len = 0;
                ++res; 
            }
        }
        
        return res;
    }
}
`````
