## Вопросы JS

###1. Разница между операторами == и === ?
  
###2. Дать ответ.
    
    abc  == false;	        // проверка вернула true, каким значением может быть abc
    abc === false;          // проверка вернула true, каким значением может быть abc
    
    new Number(5)  == 5;	// какой будет результат
    new Number(5)  === 5;	// какой будет результат

    var a = {};
    a  == {};	// какой будет результат
    a === {};	// какой будет результат
    a  == a;	// какой будет результат
    a === a;	// какой будет результат
    

###3. Как создать обекты в js ?

###4. Чем отличаеться .call от .apply ?

###5. Что такое замыкание в js ?

###6. Что произойдет при выполнении: +new Date(); ?

###7. Что произойдет при выполнении: Date.now(); ?

###8. Что произойдет если внутри функции написать:

    foo(); 
    bar();
    baz();
    spam();
     
    var foo = function () {};
    function bar() {};
    var baz = function spam() {};
    
###9. Что будет в результате выполнения кода:
    
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
  
###10. Определить repeatify функцию объекта String.
Функция принимает целое число, определяющее, сколько раз строка должна быть повторена.  
Функция возвращает строку повторяется число раз, указанное.  
Например:

    console.log ('hello'.repeatify(3));
    
Результат должен быть: hellohellohello.  

###11. Делегирование событий
*   Рассказать про делегирование событий
*   Решить [задачу](http://jsfiddle.net/DangelZM/caab0a4n/)


    Задание: При нажатии на ссылку в меню, алертом выводить href данной ссылки
    и прерывать переход по даной ссылке

###12. Наследование
 Создайте класс Animal, создайте класс Duck, Rabbit с наследдованием от Animal
 все животные будут иметь имена, реализуйте создание животных с указанием имени.  
 все животный будут передвигатся со своей скоростью и каждый по своему,
 и при этом сообщать о том "Я начал двигаться со скоростью ... " и двигаться по своему.  
 
Как вы реализуете такое поведение?  


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
