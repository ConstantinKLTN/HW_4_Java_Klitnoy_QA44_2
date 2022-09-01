## Домашнее задание к занятию "Система сборки Maven, управление зависимостями, автотесты на JUnit5"

### Задание 2. Читаем логи

Исправил ошибки в коде, программа работает, но ошибка при запуске команды "mvn clean compile spotbugs:check" все равно появляется. 


**Мои шаги**

* Скачал прикреплёный архив
* Открыл проект в IDEA
* Запустил команду Maven*: mvn clean compile spotbugs:check
* Проанализировал логи, нашел там ошибку "*class org.codehaus.groovy.runtime.callsite.PlainObjectMetaMethodSite cannot access a member of class java.util.Collections$UnmodifiableCollection (in module java.base) with modifiers "public"*", что означает что один класс не может получить доступ к классу «public» в модуле java.base.
* Прочитал статьи про "*Модификаторы доступа и инкапсуляция*"
* Java (IDEA) показывала ошибку "*Return value of the method is never used*".
* Я ее исправил добавив в Main.jawa в строку 8 "*long bonus = ...*" и в 9 строку "*System.out.println(bonus);*"

Программа работает, но ошиька при запуске комманды "mvn clean compile spotbugs:check" все равно появляется.
    
    Подскажите пожалуйста что не так?