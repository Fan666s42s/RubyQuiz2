##1.宣告變數a，把1指派給變數a
##  宣告實例變數a，把2指派給實例變數a
##  宣告類別變數a，把5指派給類別變數a
##  宣告一個名稱為user的User類別物件
##  取得User類別的事例變數name
##  更改User類別的的實例變數name為"Joe"
##2.module是一種包著方法的區塊，不能夠new出物件，但能夠被不同的class使用
```ruby
module Swim
  def swim
    puts "It can swim."
  end
end

module Fly
  def fly
    puts "It can fly."
  end
end

class Animal 
end

class Duck < Animal
  include Swim
  include Fly
end

class Turtle < Animal
  include Swim
end

duck = Duck.new
duck.Swim
duck.Fly

```
##3.類別變數宣告：@@name，實例變數宣告：@name
##  類別變數呼叫只要class名稱.類別變數，實例變數呼叫要new一個class物件，物件.實例變數
##4.類別方法定義及呼叫:
```ruby
class Test
  def self.Hello
  end
end

Test.Hello
```
##  實例方法定義及呼叫:
```ruby
class Test
  def Hello
  end
end

test = Test.new
test.Hello
```
##5.
```ruby
class User

  attr_accessor :name, :gender, :occupation

  def initialize(name, gender, occupation)
  @name = name
  @gender = gender
  @occupation = occupation
  end
end
```
##6.A指向class自己，B指向呼叫方法的物件的記憶體位址
##7.attr_accessor可以自動幫我們做到getter和setter功能，
##  而attr_reader只能產生出getter功能，attr_writer只能產生setter功能
##8.public method可以被外部呼叫，private method只能再class內部被呼叫。
##9.子類別繼承父類別會擁有付類別中所有得方法及變數，module則是可以被很多不同類別所使用的工具箱，
##  例如:烏龜和鴨子都是動物，繼承動物這個父類別，鴨子會飛，而烏龜不會飛，
##  所以飛這個能力並不屬於所有動物，它必須被特別拿出來等到有需要得地方才安排進去。
##10.Parent並不會有Sub class的方法，所以Parent不能使用該module中之method，
##  但是Sub class會有Parent的所有方法變數，所以該class的Sub class可以使用module中的method
##11.關聯是資料庫就是將不同的資料表之間的Key互相做關聯，這種方法可以更明確知道不同table間的關係，
##  而且table和table之間是獨立的，修改一個table的資料不會影響到其他table的資料。
##  SQL是一種專門用來操作資料的的程式語言，包括創建table，對table內資料的新增，修改，刪除，查詢。

