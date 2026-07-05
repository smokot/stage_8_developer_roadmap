# stage_8_developer_roadmap *PHP*

* Основы PHP
  - Основы синтаксиса
  - Переменные
  - Типы данных
  - Операции в PHP
  - Конструкция if..else и тернарная операция
  - Конструкции switch и match
  - Циклы
  - Массивы
  - Ассоциативные массивы
  - Многомерные массивы
  - Функции
  - Параметры функции
  - Возвращение значений и оператор return
  - Анонимные функции
  - Замыкания / Closure
  - Стрелочные функции
  - Генераторы
  - Ссылки
  - Область видимости переменной
  - Константы
  - Проверка существования переменной
  - Получение и установка типа переменной. Преобразование типов.
    ```
    gettype()
    is_integer()
    settype()
    (int)$boolVar;
    ```
  - Операции с массивами
    - is_array
    - count/sizeof
    - shuffle
    - compact
    - Сортировка массивов (krsort, asort, arsort, krsort, natsort)
  - Отправка данных на сервер
    - Получение данных из строки запроса
    - Отправка форм
    - Безопасность данных
    - Отправка массивов
    - Работа с полями ввода форм
* ООП
  - Объекты и классы
  - Конструкторы и деструкторы
  - Анонимные классы
  - Наследование.  parent::__construct($name); parent::method($arg);
  - $tom instanceof Employee;  // true
  - Запрет наследования и оператор final
  - Модификаторы доступа
  - Статические методы и свойства
  - Интерфейсы
  - Абстрактные классы и методы
  - Traits
  - Копирование объектов классов.
    ```$bob = clone $tom; function __clone() { $this->company = clone $this->company; }```
  - Свойства и классы для чтения. ```readonly```
* Базовые возможности PHP
  - Подключение внешних файлов
    - Инструкция include
    - Инструкция include_once - чтобы исключить повторное подключение файла
    - Инструкции require и require_once - если файл не будет найден, действие программы прекратится
    - Функция spl_autoload_register("my_autoloader"); - эта функция автоматически вызывается, когда в программе начинает использоваться неизвестный класс или интерфейс
   
* Пространства имен
  - Определение пространства имен
  - Обращение к пространству имен
  - Вложенные пространства имен
  - Псевдонимы
  - Подключение констант и функций
    ```
    use \base\classes\Person;
    use const \base\classes\adminName;
    use function \base\classes\printPerson;
    ```
* Типизация данных
* Работа со строками
* Работа с cookie
  - Сохранение cookie - ```bool setcookie(string $name, string $value, int $expire, 
                           string $path, string $domain, bool $secure, bool $httponly);```

  - Получение cookie - ```$_COOKIE["name"]```
  - Удаление cookie - ```setcookie ("name", "", time() - 3600);``` / Для удаления cookie достаточно в качестве срока действия указать какое-либо время в прошлом:
* Сессии'
  - session_start();
  - ```	$_SESSION["имя_переменной"] = значение; ```
  - ``` unset($_SESSION["имя_переменной"]);```
  - session_destroy();
* Обработка исключений
  - Конструкция ```try catch(Error $ex) finally```
  - Генерация исключений ```throw new Exception("waawawwa");```
* Работа с файловой системой
  - Чтение и запись файлов
    - fopen(string $filename, string $mode)
    - ```while(!feof($fd)) { (fgets($fd)); } ``` / ```fread($fd, 600)```
    - fwrite($fd, $str);
    - fputs($fd, $str);
    - ```int fseek (resource $handle , int $offset [, int $whence = SEEK_SET ] )```
    - fclose($fd);
    - file_get_contents()
    - file_put_contents()
* Управление файлами и каталогами
  - Перемещение файла ```rename("hello.txt", "subdir/hello.txt")```
  - Копирование файла ```copy("hello.txt", "hello_copy.txt")```
  - Удаление файла ```unlink("hello_copy.txt")```
  - Создание каталога ```mkdir("newdir")```
  - Удаление каталога ```rmdir("newdir")```

    
