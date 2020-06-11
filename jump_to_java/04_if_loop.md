# [04]제어문

```java
int money = 2000;
boolean hashCard = true;

if (money >= 3000 || hashCard){
	System.out.println("택시를 타고 가라");
} else {
	System.out.println("걸어가라");
}
```

```java
ArrayList<String> pocket = new ArrayList<String>();
pocket.add("paper")
pocket.add("handphone")
pocket.add("money")

if (pocket.contains("money")){
	System.out.println("택시를 타고 가라");
} else{
	**System.out.println("걸어가라");
}
```

```java
boolean hasCard = true;
ArrayList<String> pocket = new ArrayList<String>();
pocket.add("paper");
pocket.add("handphone");

if (pocket.contains("money")) {
    System.out.println("택시를 타고 가라");
}else if(hasCard) {
    System.out.println("택시를 타고 가라");
}else {         
    System.out.println("걸어가라");
}
```

```java
public class SwitchDemo{
	public static void main(String[] args){
		int month = 8;
		String monthString = "";
		switch (month) {
			case 1: monthString = "Jan";
							break;
			case 2: monthString = "Feb";
							break
			}
		
```

```java
int treeHit = 0;
while (treeHit < 10){
	treeHit ++;
	System.out.println("나무를 " + treeHit + "번 찍었습니다.");
	if (treeHit == 10){
		System.out.println("나무 넘어갑니다");
	}
}
```

```java
// for(초기치, 조건, 증가치)
String[] numbers = {"one", "two", "three"};
for(int i=0; i < numbers.length; i++){
	System.out.println(numbers[i]);
)
```

```java
int[] marks = {90, 25, 67, 45, 80};
for(int=0; i < makrs.length; i++){
	if(marks[i] > =60){
		System.out.println((i+1) + "번 학생은 합격입니다.");
	}else{
		System.out.println((i+1) + "번 학생은 불합격입니다.");
	}
}
```

```java
for(int i = 2; i <10; i++){
	for(int j =1; j<10; j++{
	System.out.println(i*j +" ");
}

```

```java
String[] numbers = {"one", "two", "three"};
for(String num: numbers){
	System.out.println(num);
}
```

```java
ArrayList<String> numbers = new ArrayList<String>();
nubmers.add("one");
nubmers.add("two");
nubmers.add("three");

for(String num: numbers){
	System.out.println(num);
}
```