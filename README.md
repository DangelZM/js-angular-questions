## Вопросы JS

###1. Какие типы данных есть в JS?

###2. Что вы можете сказать о специальном типе данных char в JS?

###3. Какая разница между операторами == и === в JS?
  
###4. Дать ответы.
    
    abc  == false;	        // проверка вернула true, каким значением может быть abc
    abc === false;          // проверка вернула true, каким значением может быть abc
    
    new Number(5)  == 5;	// какой будет результат
    new Number(5)  === 5;	// какой будет результат

    var a = {};
    a  == {};	// какой будет результат
    a === {};	// какой будет результат
    a  == a;	// какой будет результат
    a === a;	// какой будет результат
    

###5. Какие способы есть в JS что бы создать объект?

###6. Чем отличаеться .call от .apply?

###7. Рассказать про замыкание (Closure) в JS?

###8. Рассказать про подъем (Hoisting) в JS?

###9. Что будет результатом выполнения, и какая разница в таких вызовах:
 
    var t1 = +new Date();
    var t2 = Date.now();

###10. Что произойдет при вызове функции, внутри которой:

    foo(); 
    bar();
    baz();
    spam();
     
    var foo = function () {};
    function bar() {};
    var baz = function spam() {};
    
###11. Что будет в результате выполнения кода:
    
    var fullname = 'John Doe';
    var obj = {
       fullname: 'Colin Ihrig',
       prop: {
          fullname: 'Aurelio De Rosa',
          getFullname: function() {
             return this.fullname;
          }
       }
    };

    console.log(obj.prop.getFullname());

    var test = obj.prop.getFullname;

    console.log(test());
    
###12. Что такое Lexical Environment в JS?
  
###13. Определить [repeatify](http://jsfiddle.net/DangelZM/gro79to1/) функцию объекта String.
Функция принимает целое число, определяющее, сколько раз строка должна быть повторена.  
Функция возвращает строку которая повторяется указанное число раз.
Например:

    console.log ('hello'.repeatify(3));
    
Результат должен быть: hellohellohello.  

###14. Делегирование событий
*   Рассказать про делегирование событий
*   Решить [задачу](http://jsfiddle.net/DangelZM/caab0a4n/)


    Задание: При нажатии на ссылку в меню, алертом выводить href данной ссылки
    и прерывать переход по даной ссылке

###15. Какой способ наследование предлагаеться в JS?


## Вопросы AngularJS

###1. Может ли в приложении созданном с AngularJS быть одновременно более 1 контроллера?

###2. За отвечает директива ngModel?

###3. Как можно заменить цикл for или foreach с помощью AngularJS?


###4. Что будет выведено на экран после запуска такого приложения?

    <!doctype html> 
    <html lang="en" ng-app> 
        <head> 
        <meta charset="utf-8"> 
        <title>My HTML File</title> 
        <script src="lib/angular/angular.js"></script> 
    </head> 
    <body> 
        <p>Nothing here {{2+5}}</p> 
    </body> 
    </html> 

###5. Какую директиву нужно использовать вместо ng-YYY чтобы напечатать "Hello, AngularJS" на странице?

    <div ng-app="" ng-init="firstName='AngularJS'"> 
    <p>Hello, <span ng-YYY=" firstName"></span></p> 
    </div> 

###6. Можно ли использовать несколько директив в одном элементе? К примеру

    <div ng-show="" ng-repeat="">


###7. Какое значение параметра restrict необходимо указать, чтобы директива использовалась, как имя элемента

###8. Что будет напечатано на странице?
      <div ng-app="" ng-controller="personController"> 
      {{firstName + " " + lastName}} 
      </div> 
      <script> 
      function personController() { 
          firstName = "Mike", 
          lastName = "Barkly" 
      } 
      </script> 
      
###9. Как правильно применить фильтр currency к выражению.

    <p>the best price: {{ discountPrice }} </p>
    
###10. Для чего используется директива ngCloak?

###11. Что будет напечатано на странице?
      
      <body ng-app="myTestApp"> 
          <div ng-controller="scopeCtrl"> 
              <h1>{{data.brand}}</h1> 
          </div> 
          <div> 
              <h1>{{data.model}}</h1> 
          </div> 
      </body> 
      angular.module('myTestApp',[]) 
       
          .controller('scopeCtrl',['$scope',function($scope){ 
              $scope.data = { 
                  brand: "mitsubishi", 
                  model: "lancer" 
              } 
          }]); 
_
