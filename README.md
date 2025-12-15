# C-
C learnings

The main bitwise operators are:

• AND (&)
• OR (|)
• XOR (^)
• NOT (~)
• Left Shift (<<)
• Right Shift (>>)

**AND**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/and.png)

**OR**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/or.png)

**XoR**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/Xor.png)

**NOT**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/not.png)

**Left-Shift**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/leftshitf.png)

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/leftshift1.png)

**Right-Shift**

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/rightshift.png)

![image alt](https://github.com/SDRG1998/C-/blob/d8d8558d39831bb804b3b6448e16bd5a1426ba70/img/rightshift1.png)

**Important Practice Problems on Bitwise Algorithm:**

**1. How to Set Bit**

    • If we want to set a bit at nth position in the number 'num', it can be done using the 'OR' operator( | ).  

    • Then, use the "OR" operator to set the bit at that position. "OR" operator is used because it will set the bit even if the bit is unset previously in the binary representation of the number 'num'.

    • If the bit would be already set then it would remain unchanged.

**2. How to unset/clear a bit at n'th position in the number **

    • First, we left shift '1' to n position via (1<<n) then we use bitwise NOT operator '~' to unset this shifted '1'.

    • Now after clearing this left shifted '1' i.e making it to '0' we will 'AND'(&) with the number 'num' that will unset bit at nth position.

**3. Toggling a bit at nth position **

    • Toggling means to turn bit 'on'(1) if it was 'off'(0) and to turn 'off'(0) if it was 'on'(1) previously. We will be using the 'XOR' operator here which is this '^'. The reason behind the 'XOR' operator is because of its properties. 

    • Properties of 'XOR' operator. 
        1^1 = 0
        0^0 = 0
        1^0 = 1
        0^1 = 1
    
    • If two bits are different then the 'XOR' operator returns a set bit(1) else it returns an unset bit(0).

**4. Checking if the bit at nth position is Set or Unset**

    • We used the left shift (<<) operation on 1 to shift the bits to nth position and then use the & operation with number given number, and check if it is not-equals to 0.

**5. Multiply a number by 2 using the left shift operator**

    int main()
    {
      int num = 12;
      int ans = num << 1;
      return 0;
    }

**6. Divide a number 2 using the right shift operator**

    int main()
    {
      int num = 12;
      int ans = num >> 1;
      cout << ans << endl;
      return 0;
    }

**7. Compute XOR from 1 to n (direct method)**

    • The  problem can be solved based on the following observations:

    • Say x = n % 4. The XOR value depends on the value if x.

    • If, x = 0, then the answer is n.
       x = 1, then answer is 1.
       x = 2, then answer is n+1.
       x = 3, then answer is 0.
