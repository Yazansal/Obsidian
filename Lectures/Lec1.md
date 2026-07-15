## بدي استقبل اي نوع بيانات لنفس الكلاس في طريقتين للحل

1.  **طريقة الاوبجكت**

```java
 public class Main {  
    public static void main(String[] args) {  
  
        Box b = new Box();  
        b.setVal("java");  
        String s = (String) b.getVal();  
  
    }  
}
```

```java
public class Box  
{  
    Object val;  
  
  
    public Object getVal() {  
        return val;  
    }  
  
    public void setVal(Object val) {  
        this.val = val;  
    }  
}
```

==الاوبجكت هو حل من الحلول لكن مش افضل اشي لانو بلزم نعمل كاست كل مرة==

2. **طريقة (Generic Methods &Classes)**

```java
  
public class Main {  
    public static void main(String[] args) {  
  
        //مرر النوع الي بدك اياه بين الاقواس  
        //rubber classes only!!! (Integer,String,etc...) ,int will not work  
        Box<String> b = new Box<>();  
        b.setVal("java");  
        String s = (String) b.getVal();  
  
    }  
}
```

```java
public class Box<T>//T is just a random letter but it's what people use  
{  
    //مكان كل T بتحول النوع الي بدي اياه من البيانات  
    T val;  
  
  
    public T getVal() {  
        return val;  
    }  
  
    public void setVal(T val) {  
        this.val = val;  
    }  
}
```

==افضل حل لهذه الحالة هو استعمال الجنرك==

