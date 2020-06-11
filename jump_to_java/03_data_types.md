# [03] 자료형

## 1. 문자열

- 문자열에서는 ==를 쓰지 않음 → 자료형이 같냐고만 사용
- a.equals(b)로 물어봄

![03%2034e19dc0660a4ed9bf79f1a29e02c65c/_2020-06-04__9.01.08.png](03%2034e19dc0660a4ed9bf79f1a29e02c65c/_2020-06-04__9.01.08.png)

## 2. StringBuffer

- 문자열을 추가하거나 변경할때 쓰는 자료형

```java
public class Test {
    public static void main(String[] args) {
        StringBuffer sb = new StringBuffer();
        sb.append("hello");
        sb.append(" ");
        sb.append("jump to java"); //현재까지 sb는 StringBuffer
        System.out.println(sb.toString()); //toString()메소드로 문자로 변경
    }
}
>>> hello jump to java
```

## 3. 배열

```java
int[] int_arr = {1,2,3,4}
String[] string_arr = {"월", "화"}
///////////////
```

- 배열의 길이는 고정되어있음

```java
String[] string_arr = new String[7]
string_arr[0] = "월"
weeks[1] = "화";
weeks[2] = "수";
weeks[3] = "목";
weeks[4] = "금";
weeks[5] = "토";
weeks[6] = "일";
```

- 반드시 초기 값 없이 배열을 만들 때는 길이값이 필요함

```java
String[] weeks = new String[];    // 길이값이 없으므로 컴파일 오류가 발생한다.
```

- 배열이 만들어졌다면 십중팔구 for문으로 배열값을 돌림
- 배열의 길이만큼 for문 돌리는게 중요

```java

String[] week = {"월", "화", "수", "목", "금", "토", "일"};
for (int i=0; i < weeks.length; i++){
	System.out.println(weeks[i]);
}

```

## 4. 리스트 (list)

- 배열과 비슷한 자바의 자료형 → 배열보다 편리한 기능
- 명확한 크기를 알 수 없을 떄 (ArrayList,

```java
ArrayList arr_lst = new ArrayList();
arr_lst.add("138");
arr_lst.add("129");
arr_lst.add("142");

arr_lst.add(0, "133"); //첫번째 위치에 133 삽입
add_lst.add(1,"133");

//2번쨰 값을 알고 싶으면
System.out.println(arr_lst.get(1+1));
//size return
System.out.println(arr_lst.size());
//contain
System.out.println(arr_lst.conatain("142");
>>> true
//remove(obj)
arr_lst.remove("129"); //삭제하고 삭제한 결과를 리턴
>>> true
//remove(idx)
arr_lst.remove(idx); //삭제하고, 삭제한 거 리턴
>>>138
```

```java
import java.util.ArrayList;

public class TestList {
    public static void main(String[] args) {
        ArrayList<String> pitches = new ArrayList<String>();
        pitches.add("138");
        pitches.add("129");
        pitches.add("142");

        System.out.println(pitches.get(1));
        System.out.println(pitches.size());
        System.out.println(pitches.contains("142"));

        System.out.println(pitches.remove("129"));
        System.out.println(pitches.size());
        System.out.println(pitches.remove(0));
    }
}
```

## 5.map

-파이썬의 딕셔너리 같은

### put

- 자바의 맵중 가장 간단한 HashMap
    - HashMap, LinkedHashMap, TreeMap

```java
HashMap<String, String> map = new HashMap<String, String>();
//k,v가 str인 hashmap 
map.put("people", 사람);
map.put("baseball", 야구);
//해쉬맵역시 제네리스를 이용하는데 k,v가 모두 str타입이라는 것 

///Get
map.get("people");

//containsKey
map.containsKey("people");
>>>true

//remove
map.remove("people");

//size
map.size();
```

```java
import java.util.HashMap;

public class TestMap {
    public static void main(String[] args) {
        HashMap<String, String> map = new HashMap<String, String>();
        map.put("people", "사람");
        map.put("baseball", "야구");

        System.out.println(map.get("people"));
        System.out.println(map.containsKey("people"));
        System.out.println(map.remove("people"));
        System.out.println(map.size());
    }
}
```

- map은 순서에 의존하지 않는데
- 순서대로 데이터를 가져오고 싶으면 key에 의해 sort된 데이터를 가져고오고싶으면
    - → LinkedHashMap, TreeMap을 이용하면 된다.