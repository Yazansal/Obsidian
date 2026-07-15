# Time Complexity
### 1. Time
- Best case
- Avg case
- Worst case
![[Drawing 2026-07-13 23.24.47.excalidraw]]

==O(1): العمليات الحسابية وهي اسرع اشي== 
1. 
```java
 int x=10
  x+x
  return x
```
2. 
```java
for(int i=1;i<=10;i++){
sout(i);
}
```

### 2. Space(not that important)


---

## BigO Time Complexity

![[1_q_MJ6WJmEzbcaAT51n27_g.jpg.jpg|256]]

---

### Time Complexity Examples

![[Drawing 2026-07-13 23.37.06.excalidraw]]




---

# ArrayList

```java
code:  ArrayList list = new ArrayList();
```

- ### اذا بدي اطبع نوع بيانات محدد من ارري لست متعددة البيانات (بدي اجمع الانتجر في الارري ليست)
```java
import java.util.ArrayList;  
  
public class Main {  
    public static void main(String[] args) {  
        ArrayList list = new ArrayList();  
  
        list.add(10);  
        list.add(true);  
        list.add("java");  
        list.add(20.0);  
        int sum = 0;  
        for (int i = 0; i < list.size(); i++) {  
            if (list.get(i) instanceof Integer) {  
                sum += (int) list.get(i);  
            }  
        }  
    }  
}
```

- ### لو بدي احدد نوع بيانات معين للاري ليست 
```java
ArrayList<String> list = new ArrayList<>();
```

- ### ازالة عنصر او اندكس غير موجود في المصفوفة
```java
list.remove(Object) //no error just blank
list.remove(index) //error
```

- ### لو بدي امسح اوبجكت لازم اعمل كاستنج اذا صار في تداخل بين الانتجر الاوبجكت والاندكس
```java
import java.util.ArrayList;  
  
public class Main {  
    public static void main(String[] args) {  
        ArrayList<Integer> list = new ArrayList<>();  
  
        list.add(10);  
        list.add(20);  
        list.add(30);  
        list.add(40);  
  
        list.remove((Integer) 10);//option 1  
        list.remove((Object) 10);//option 2  
    }  
}
```

- ### عمل swap اول واخر عنصر
```java
import java.util.ArrayList;  
  
public class Main {  
    public static void main(String[] args) {  
        ArrayList<Integer> list = new ArrayList<>();  
  
        list.add(10);  
        list.add(20);  
        list.add(30);  
  
        int temp = list.get(0);  
        list.set(0, list.get(list.size() - 1));  
        list.set(list.size() - 1, temp);  
        System.out.println(list);  
    }  
}

```

  ==الاوتبوت==
```java
[30, 20, 10]
```


---

## Difference between static Array & ArrayList in time complexity

| Complexity | Static Array | ArrayList |
| ---------- | ------------ | --------- |
| Access     | O(1)         | O(1)      |
| Search     | O(n)         | O(n)      |
| Insertion  | O(n) (N/A)   | O(n)      |
| Apending   | O(n) (N/A)   | O(1)      |
| Deletion   | O(n) (N/A)   | O(n)      |

---

## Examples on common time complexity

Finding all subsets of a set O(2^n)
Finding all permutations of a String O(n!)
Binary search O(n * log(n))
Iterating over all the cells in a matrix of size n by m O(nm)

---
