# 아이템13. Unit?을 리턴하지 말라

마치 Boolean이 true/false인 것처럼, Unit?은 Unit 또는 null 을 가질 수 있기 때문에 Boolean와 Unit? 타입은 서로 바꿔서 사용할 수 있다.

(그렇게 치면 다른 것들도 nullable이면 되는거 아닌가? 예를 들어서 Int? 면 Int 또는 null을 가질 수 있잖아..?) → Unit 이 true, false 가 들어갈 수 있으니 true?, false? 가 될수있으니까 한 번 더 가공해야하니까..그게 안되는것!

Unit?으로 bool 을 표현하는 것은 오해의 소지가 있으니 아예 bool 형태로 변경하거나 Unit?을 리턴해서 사용하는 것이 좋고 Unit?을 기반으로 연산하지 않는 것이 좋다.

1. Unit? 자체를 리턴하지 말고
2. 리턴된걸 재연산해서 처리하지 말고
