# php-best-practices

## PHP
 * Use named constructor even if you have only one http://verraes.net/2014/06/named-constructors-in-php/
 * Finals classes by default https://matthiasnoback.nl/2018/09/final-classes-by-default-why/
 * Classify yours exceptions http://37steps.com/2700/exception-classification/. For example, throw \RuntimeException (or parent class) for failures caused by external, unpredictable things and throw \LogicException (or parent class) for programming mistakes.
 * Avoid setter injection and validate property on initialization to ensure object consistency https://www.brandonsavage.net/avoiding-setter-injection/
 
 ## Symfony
 * Use autowiring for your services
 * Validate your entities
 * If you use annotations, compose your entities with traits https://medium.com/@galopintitouan/using-traits-to-compose-your-doctrine-entities-9b516335119b
 
 ## Api Platform
 
WIP

 ## Doctrine2
 
 * Avoid bidirectionnals associations. Use DQL trick for your complex queries instead https://tideways.com/profiler/blog/5-doctrine-orm-performance-traps-you-should-avoid
 * Repositories don't respect ISP. Use Query Function
 * Use iterable type on Doctrine's collection methods
 * Doctrine doesn't require getter or setter. Don't expose them if you don't need it (Immutables properties for example)
 * Use UUID instead of auto incremented ids https://medium.com/@galopintitouan/auto-increment-is-the-devil-using-uuids-in-symfony-and-doctrine-71763721b9a9
 * Inject your repositories instead of entity manager https://matthiasnoback.nl/2014/05/inject-a-repository-instead-of-an-entity-manager/
 * Use annotations (YAML configuration has been deprecated)
 * Avoid composite primary key https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/tutorials/composite-primary-keys.html
 * Use fixtures in development
 
 ### Coming in doctrine3
 * Final methods will be possible in Doctrine3
 
 ### Sources
   * http://talks.nekland.fr/Doctrine/#/ (French slides)
   * https://ocramius.github.io/doctrine-best-practices/#/
   * https://ocramius.github.io/blog/doctrine-orm-optimization-hydration/
 
 ## PHPUnit
  * Use PHPUnit Mocks instead of Prophecy https://medium.com/@IvanChepurnyi/native-mocking-and-stubbing-in-php-ad11a32596e4
  * Isolate your functionals tests thank to a group annotation (@group functional)
  * Never mock the class / trait / interface you are testing on its test class. For a trait or interface, use a DummObject which `implements` the interface or `uses` the trait
  * Don't test your privates methods unless they are complex 
