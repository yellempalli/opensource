
1. For Loops in Java and Python:

```python
# Python for loop
for i in range(5):    # range(5) generates 0,1,2,3,4
    print(i)

# Python for loop with list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

```java
// Java for loop
for(int i = 0; i < 5; i++) {
    System.out.println(i);
}

// Java for-each loop
String[] fruits = {"apple", "banana", "cherry"};
for(String fruit : fruits) {
    System.out.println(fruit);
}
```

2. Array Reversal:

```python
# Python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr
```

```java
// Java
public static void reverseArray(int[] arr) {
    int left = 0, right = arr.length - 1;
    while(left < right) {
        int temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;
        left++;
        right--;
    }
}
```

3. Vowels and Consonants Count for Multiple Test Cases:

```python
def count_vowels_consonants(s):
    vowels = set('aeiouAEIOU')
    v_count = c_count = 0
    
    for char in s:
        if char.isalpha():
            if char in vowels:
                v_count += 1
            else:
                c_count += 1
    return v_count, c_count

# Handle multiple test cases
t = int(input())  # number of test cases
for _ in range(t):
    s = input()
    vowels, consonants = count_vowels_consonants(s)
    print(f"Vowels: {vowels}, Consonants: {consonants}")
```

4. ASCII Values:
- 'a' to 'z': 97 to 122
- 'A' to 'Z': 65 to 90
- '0' to '9': 48 to 57

5. Character Frequency Counter (including uppercase, lowercase, and digits):

```python
def count_all_chars():
    s = input("Enter string: ")
    # Create frequency array for all possible characters
    freq = [0] * 128  # for ASCII characters
    
    # Count frequency
    for char in s:
        freq[ord(char)] += 1
    
    # Print frequencies for letters and digits
    print("\nLowercase letters:")
    for i in range(97, 123):  # a to z
        if freq[i] > 0:
            print(f"{chr(i)}: {freq[i]}")
    
    print("\nUppercase letters:")
    for i in range(65, 91):   # A to Z
        if freq[i] > 0:
            print(f"{chr(i)}: {freq[i]}")
    
    print("\nDigits:")
    for i in range(48, 58):   # 0 to 9
        if freq[i] > 0:
            print(f"{chr(i)}: {freq[i]}")

# Example usage
count_all_chars()
```

Here's a sample output when input is "Hello123WORLD":
```
Lowercase letters:
e: 1
l: 2
o: 1

Uppercase letters:
H: 1
L: 1
O: 1
R: 1
W: 1
D: 1

Digits:
1: 1
2: 1
3: 1
```

Regarding memory:
- A char takes 1 byte (8 bits) of memory
- Can represent 256 different values [0, 255]
- Boolean theoretically needs only 1 bit, but computers typically allocate 1 byte as it's the smallest addressable unit of memory
- This is why boolean in most programming languages still uses 1 byte despite only needing 1 bit
