### 0125 Valid Palindrome

#### Character 클래스
- `Character.isLetterOrDigit`: 원시자료형 char를 입력값으로 하여 영숫자인지 판별합니다.
- `Character.toLowerCase`: 원시자료형 char를 입력값으로 하여 소문자로 변경합니다.

#### String 클래스
- `charAt(int index)`: 리턴타입은 문자의 원시자료형 char입니다.

#### 사용한 자료구조 혹은 자료형
- 문자열에서 문자를 하나씩 추출하여 비교합니다.

### 0937 Reorder Data in Log Files

#### Character 클래스
- `Character.isDigit`: 원시자료형 char를 입력값으로 하여 숫자인지 판별합니다.

#### String 클래스
- `split`: 두 번째 인자의 숫자는 배열의 길이입니다.
- `compareTo`: 호출하는 문자열과 매개변수로 전달된 다른 문자열을 비교 후 사전순으로 정렬합니다.
- 첫 번째 문자열이 두 번째 문자열보다 앞설 경우 음수, 같을 경우 0, 뒤따를 경우 양수를 반환합니다(=즉 앞으로 와야 할 경우 양수, 뒤에 머물러야 할 경우 -1).

#### List 인터페이스
- `sort`: 정렬 기준은 Comparator 인터페이스를 구현하는 객체를 통해 지정 가능합니다.
-  (*) Comparator인터페이스의 경우 compare라는 추상메소드를 가지고 있고 해당 식에서는 람다 표현식을 통해 직접 구현함 (자바8이전은 compare 함수 @Override필요)
- `addAll`: 호출되는 리스트(letterList)의 끝에 다른 컬렉션(digitList)의 모든 요소를 추가합니다.
- `toArray`: `new String[0]`의 경우, 크기가 0인 String 배열을 생성합니다.

#### 사용한 자료구조 혹은 자료형
- 두 개의 리스트 자료구조를 이용하고, 문자로그와 숫자로그의 정렬방식이 달라 둘을 분리해 다른 리스트에 담은 후 나중에 서로 이어붙입니다.

### 0049 Group Anagrams

#### String 클래스
- `toCharArray`: 문자열을 char 배열로 변환합니다.
- `valueOf`: 다양한 타입의 데이터를 문자열로 변환합니다.

#### Arrays 클래스
- `sort`: int[], long[], Object[] 등 다양한 타입의 배열에 대한 sort 메소드가 존재합니다.
- Arrays 클래스의 `sort` 메소드와 List 인터페이스의 `sort` 메소드는 List 객체를 대상으로 하며 Comparator를 매개변수로 받는 차이가 있습니다.

#### Map 인터페이스
**(*)본 코드에서는 Map 인터페이스를 HashMap 클래스를 통해 구현해 아래의 추상메소드를 사용하였습니다.**
- `containsKey`: Map에 주어진 키가 있는지 확인 후 boolean 값을 반환합니다.
- `put(K key, V value)`: Map에 키-값 쌍을 추가합니다. 이미 존재하는 키에 대해 값을 넣으면 기존 값이 새 값으로 대체됩니다.
- `get(Object key)`: 주어진 키에 연결된 값을 반환합니다.
- `values`: 주어진 키에 연결된 값들을 반환합니다.

#### 사용한 자료구조 혹은 자료형
- 단어를 정렬해 정렬한 단어를 기준으로 값을 저장하기 위해 (즉 하나의 키에 애너그램인 여러 개의 값이 추가될 수 있기 때문에) 리스트를 값으로 두는 맵을 선언합니다.

