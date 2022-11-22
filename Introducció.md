# Introducció

# **[Introducció](https://jutge.org/problems#)**

![Comprovant Exercicis Jutge CURS ESTIU - INTRODUCCIÓ.png](comprovant/Comprovant_Exercicis_Jutge_CURS_ESTIU_-_INTRODUCCIO.png)

[P68688](https://jutge.org/problems/P68688_en) Hello world!

```java
public class Main {
    public static void main(String args[]){
        System.out.println("Hello world!");   
    }
}
```

---

[P57548](https://jutge.org/problems/P57548_en) Sum of two integer numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int b = input.nextInt();
        
        System.out.println(a+b);
    }
}
```

---

[P41221](https://jutge.org/problems/P41221_en) Sum of three integer numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int b = input.nextInt();
        int c = input.nextInt();
        
        System.out.println(a+b+c);
    }
}
```

---

[P56118](https://jutge.org/problems/P56118_en) Maximum of two integer numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int b = input.nextInt();
        
        if(a>b) System.out.println(a);
        else System.out.println(b);
    }
}
```

---

[P52847](https://jutge.org/problems/P52847_en) Maximum of three different integer numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int b = input.nextInt();
        int c = input.nextInt();
        
        if(a > b && a > c) System.out.println(a);
        else if(b > a && b > c) System.out.println(b);
        else System.out.println(c);
    }
}
```

---

[P90615](https://jutge.org/problems/P90615_en) Maximum of three integer numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int b = input.nextInt();
        int c = input.nextInt();
        
        if(a >= b && a >= c) System.out.println(a);
        else if(b >= a && b >= c) System.out.println(b);
        else if(c >= a && c >= b) System.out.println(c);        
    }
}
```

---

[P15613](https://jutge.org/problems/P15613_en) Temperatures

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        /*
         * hot - >30
         * cold - <10
         */
        int a = input.nextInt();

        if(a > 30){
            System.out.println("it's hot");
            if(a >= 100) System.out.println("water would boil");
        }else if(a < 10){
            System.out.println("it's cold");
            if(a <= 0)   System.out.println("water would freeze");
        }else   System.out.println("it's ok");

    }
}
```

---

[P48107](https://jutge.org/problems/P48107_en) Integer division and remainder of two natural numbers

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int a = input.nextInt();
        int b = input.nextInt();
        System.out.println(a/b + " " + a%b);        
    }

}
```

---

[P37469](https://jutge.org/problems/P37469_en) Time decomposition (1)

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int sec, min, hours;

        sec = input.nextInt();

        min = sec/60;         sec = sec%60;
        hours = min/60;       min = min%60;

        System.out.println(hours + " " + min + " " + sec);
        
    }   
}
```

---

[P34279](https://jutge.org/problems/P34279_en) Add one second

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int h = input.nextInt();
        int m = input.nextInt();
        int s = input.nextInt();

        s++;
        if (s==60) {
            m++;
            s = 0;
        }
        if (m==60) {
            h++;
            m = 0;
        }
        if (h==24) h = 0;
        
        String _min, _hours, _sec;
        
        if(m < 10)    _min = "0" + m; else _min = Integer.toString(m);
        if(h < 10)    _hours = "0" + h; else _hours = Integer.toString(h);
        if(s < 10)    _sec = "0" + s; else _sec = Integer.toString(s);
        
        System.out.println(_hours + ":" + _min + ":" + _sec);
    }   
}
```

---

[P81629](https://jutge.org/problems/P81629_en) Minimum change

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner teclat = new Scanner(System.in);

        int eur = teclat.nextInt();
        int cent = teclat.nextInt();

        cent = cent + eur*100;

        int b500 = cent/50000;   cent = cent%50000;
        int b200 = cent/20000;   cent = cent%20000;
        int b100 = cent/10000;   cent = cent%10000;
        int b50 = cent/5000;     cent = cent%5000;
        int b20 = cent/2000;     cent = cent%2000;
        int b10 = cent/1000;     cent = cent%1000;
        int b5 = cent/500;       cent = cent%500;

        int m2eur = cent/200;    cent = cent%200;
        int m1eur = cent/100;    cent = cent%100;

        int m50 = cent/50;       cent = cent%50;
        int m20 = cent/20;       cent = cent%20;
        int m10 = cent/10;       cent = cent%10;
        int m5 = cent/5;         cent = cent%5;
        int m2 = cent/2;         cent = cent%2;
        int m1 = cent/1;         cent = cent%1;

        System.out.println("Banknotes of 500 euros: " + b500);
        System.out.println("Banknotes of 200 euros: " + b200);
        System.out.println("Banknotes of 100 euros: " + b100);
        System.out.println("Banknotes of 50 euros: " + b50);
        System.out.println("Banknotes of 20 euros: " + b20);
        System.out.println("Banknotes of 10 euros: " + b10);
        System.out.println("Banknotes of 5 euros: " + b5);
        System.out.println("Coins of 2 euros: " + m2eur);
        System.out.println("Coins of 1 euro: " + m1eur);
        System.out.println("Coins of 50 cents: " + m50);
        System.out.println("Coins of 20 cents: " + m20);
        System.out.println("Coins of 10 cents: " + m10);
        System.out.println("Coins of 5 cents: " + m5);
        System.out.println("Coins of 2 cents: " + m2);
        System.out.println("Coins of 1 cent: " + m1);

        
    }
}
```

---

[P61634](https://jutge.org/problems/P61634_en) Leap years

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int c = input.nextInt();

        if(c%100 == 0){
            if (((c/100)%4) == 0)    System.out.println("YES");
            else System.out.println("NO");
            
        }else if(c%4 == 0 && c/10 != 0 && c/100 != 0) System.out.println("YES");
        else System.out.println("NO");        
    }   
}
```

---

[P51126](https://jutge.org/problems/P51126_en) Intervals (1)

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int a1 = input.nextInt();
        int b1 = input.nextInt();
        int a2 = input.nextInt();
        int b2 = input.nextInt();
        
        a1 = Math.max(a1,a2);
        b1 = Math.min(b1,b2);
        if (a1>b1) System.out.println("[]");        
        else System.out.println("[" + a1 + "," + b1 + "]");

    }   
}
```

---

[P56559](https://jutge.org/problems/P56559_en) Intervals (2)

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int a1 = input.nextInt();
        int b1 = input.nextInt();
        int a2 = input.nextInt();
        int b2 = input.nextInt();
        
        if(a1 == a2 && b1 == b2)    System.out.println("=");
        else if(a1 <= a2 && b1 >= b2)   System.out.println("2");
        else if(a1 >= a2 && b1 <= b2)   System.out.println("1");
        else    System.out.println("?");
        
    }   
}
```

---

[P89265](https://jutge.org/problems/P89265_en) Intervals (3)

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        Scanner input = new Scanner(System.in);

        int a1 = input.nextInt();
        int b1 = input.nextInt();
        int a2 = input.nextInt();
        int b2 = input.nextInt();
        
        String s;
        
        if(a1 == a2 && b1 == b2)    s = "= , ";
        else if(a1 <= a2 && b1 >= b2)   s = "2 , ";
        else if(a1 >= a2 && b1 <= b2)   s = "1 , ";
        else    s = "? , ";

        int r1 = Math.max(a1,a2);
        int r2 = Math.min(b1,b2);
        if (r1>r2) System.out.println(s+"[]");        
        else System.out.println(s+"[" + r1 + "," + r2 + "]");
        
    }   
}
```

---

[P58294](https://jutge.org/problems/P58294_en) The answer

```java
import java.util.*;

public class Main {
    public static void main(String args[]){
        System.out.println("42");

    }   
}
```

---
