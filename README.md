
#0125 valid-palindrome

1.Character 클래스

1) Character.isLetterOrDigit
- 원시자료형 char를 입력값으로 하여 영숫자인지 판별

2) Character.toLowerCase
-원시자료형 char를 입력값으로 하여 소문자로 변경

2.String 클래스

1) charAt(int index)
- 리턴타입은 문자의 원시자료형 char

3.사용한 자료구조 혹은 자료형
- 문자열에서 문자를 하나씩 추출하여 비교

#0937-reorder-data-in-log-files

1.Character 클래스

1) Character.isDigit
- 원시자료형 char를 입력값으로 하여 숫자인지 판별

2.String 클래스

1) split 메소드
- 두번째 인자의 숫자는 배열의 길이

2) compareTo 메소드
- 호출하는 문자열과 매개변수로 전달된 다른 문자열을 비교 후 두 문자열을 사전순으로 비교하여, 첫 번째 문자열이 두 번째 문자열보다 앞설 경우 음수, 같을 경우 0, 뒤따를 경우 양수를 반환합니다.(=즉 앞으로 와야 할 경우 양수, 뒤에 머물러야 할 경우 -1)

3.List 인터페이스
1) sort 메소드
- 정렬 기준의 경우 Comparator 인터페이스를 구현하는 객체를 통해 지정 가능
  (*) Comparator인터페이스의 경우 compare라는 추상메소드를 가지고 있고 해당 식에서는 람다 표현식을 통해 직접 구현함
  (자바8이전은 compare 함수 @Override필요)
2) addAll 메소드
- 호출되는 리스트(letterList)의 끝에 다른 컬렉션(digitList)의 모든 요소를 추가
3) toArray 메소드
- new String[0]의 경우, 크기가 0 인 String배열을 생성 => 반환될 배열의 타입을 지정하기 위한 힌트 역할

4.사용한 자료구조 혹은 자료형
- 두개의 리스트 자료구조를 이용했고 문자로그와 숫자로그의 정렬방식이 달라 둘을 아예 분리해 다른 리스트에 담고 나중에 서로 이어붙이는 전략을 사용함
