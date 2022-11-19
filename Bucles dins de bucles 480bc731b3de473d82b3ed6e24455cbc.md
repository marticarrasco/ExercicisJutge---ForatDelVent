# Bucles dins de bucles

# **[Bucles dins de bucles](https://jutge.org/problems#)**

[P79817](https://jutge.org/problems/P79817_en) Powers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        
        int a, b;

        while(input.hasNextInt()){
            a = input.nextInt();
            b = input.nextInt();
            System.out.println(Math.round(Math.pow(a, b)));
        }
    }  

}
```

---

[P90133](https://jutge.org/problems/P90133_en) Logarithms

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        
        int a, b;

        while(input.hasNextInt()){
            a = input.nextInt();
            b = input.nextInt();
            if(a == 10 && b > 10)   System.out.println((int) Math.log10(b));
            else    System.out.println((int) log(b, a));
        }
    }  

    public static double log(int x, int b) {
        return Math.log(x) / Math.log(b);
    }
}
```

---

[P33839](https://jutge.org/problems/P33839_en) Sum of digits

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        
        int a, a_;

        while(input.hasNextInt()){
            a = input.nextInt();
            a_ = a;
            
            int s = 0;

            while(a > 9){
                s = s + a%10;
                a = a/10;
            }
            
            s = s + a;

            System.out.println("The sum of the digits of " + a_ + " is " + s + ".");
            
        }
    }  
}
```

---

[P29973](https://jutge.org/problems/P29973_en) Triangle

```java

```

---

[P72484](https://jutge.org/problems/P72484_en) Rhombus

```java

```

---

[P42280](https://jutge.org/problems/P42280_en) Chess board (1)

```java

```

---

[P13623](https://jutge.org/problems/P13623_en) Chess board (2)

```java

```

---

[P19991](https://jutge.org/problems/P19991_en) Chess board (3)

```java

```

---

[P80660](https://jutge.org/problems/P80660_en) The sequence of Collatz

```java

```

---

[P24080](https://jutge.org/problems/P24080_en) Squares (1)

```java

```

---

[P34080](https://jutge.org/problems/P34080_en) Squares (2)

```java

```

---

[P39359](https://jutge.org/problems/P39359_en) Squares (3)

```java

```

---

[P35080](https://jutge.org/problems/P35080_en) Squares (4)

```java

```

---

[P61061](https://jutge.org/problems/P61061_en) Product of digits

```java

```

---