# 18.11.22
## 1. When provided with a String, capitalize all vowels

For example:

Input : "Hello World!"

Output : "HEllO WOrld!"

Note: Y is not a vowel in this kata.

[Task link](https://www.codewars.com/kata/5831c204a31721e2ae000294/train/java)
___
### Мое рещение 
```java

public class Kata {
    public static String swap(String st){
      st = st.replace('a','A');
      st = st.replace('e','E');
      st = st.replace('i','I');
      st = st.replace('o','O');
      st = st.replace('u','U');
      return st;
    }
}

```

### Понравившееся решение
```java

public class Kata {
    public static String swap(String st){
      return st.replace("a","A").replace("e","E").replace("i","I").replace("o","O").replace("u","U");
    }
}

```
## 2. Welcome. In this kata, you are asked to square every digit of a number and concatenate them.

For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.

Note: The function accepts an integer and returns an integer
[Task link](https://www.codewars.com/kata/546e2562b03326a88e000020/train/java)
### Мое рещение 
```java

public class SquareDigit {

  public int squareDigits(int n) {
      if (n < 10) return n * n;
      else {
        int h = squareDigits(n / 10);
        int l = n % 10;
        return Integer.parseInt(h + "" + l * l);
      }
  }

}

```

### Понравившееся решение
```java

public class SquareDigit {

  public int squareDigits(int n) {
    String s = n + "";
    String[] digits = s.split("");
    String output = "";
    
    for (String str : digits) {
      int i = Integer.parseInt(str);
      output +=  i * i;
    }
    
    return Integer.parseInt(output);
  }

}

```
