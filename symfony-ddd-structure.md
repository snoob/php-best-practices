```
src/
  Domain/
    Common/
      Exception/
        DomainExceptionInterface.php
    [EntityClass]
      Exception/
      Model/
      Query/
         QueryFunction.php
      Action/
        InvokableClassAction.php
 ```
 
* Exclude Model and Exception directories from services autowiring
* For InvokableClassAction.php, use [DunglasActionBundle](https://dunglas.fr/2016/01/dunglasactionbundle-symfony-controllers-redesigned)
