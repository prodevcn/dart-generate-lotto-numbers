# dart-generate-lotto-numbers

```bash
List<int> createRandomSixNumbers() {
  return (List<int>.generate(45, (i) => i+1)..shuffle()).sublist(0, 6);
}

void checkNumber(lottoList, myList) {
  int match = 0;
  
  for(int lotto in lottoList) {
    for(int myNum in myList) {
      if(lotto == myNum) {
        match ++;
        print('Awared Number: $myNum');
      }
    }
  }
  print('You are awared with $match numbers');
}

void main() {
  List<int> lottoNumbers = createRandomSixNumbers();
  List<int> myNumbers = createRandomSixNumbers();
  
  print('Lotto Numbers: $lottoNumbers');
  print('My Numbers: $myNumbers');

  checkNumber(lottoNumbers, myNumbers);
}
```
