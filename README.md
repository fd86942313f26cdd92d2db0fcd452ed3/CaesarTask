Хитрый цезарь зашифровал с помощью своего шифра описание египестких богов.
Причём для каждого бога (для каждой строки) был использован разный сдвиг.

Нашей задачей будет расшифровать его тайные письмена.

https://ru.wikipedia.org/wiki/Шифр_Цезаря  
Шифр Цезаря один из наиболее древнейших известных шифров. Схема шифрования очень проста — используется сдвиг буквы алфавита на фиксированное число позиций. Используемое преобразование обычно обозначают как ROTN, где N — сдвиг, ROT — сокращение от слова ROTATE, в данном случае «циклический сдвиг».

Алфавит действительно зацикливается, то есть буквы в конце алфавита преобразуются в буквы начала алфавита. Например, обозначение ROT2 обозначает сдвиг на 2 позиции, то есть, «а» превращается в «в», «б» в «г», и так далее, и в конце «ю» превращается в «а» а «я» — в «б». Число разных преобразований конечно и зависит от длины алфавита. Для русского языка возможно 33 разных преобразования (преобразования ROT0 и ROT34 сохраняют исходный текст, а дальше начинаются уже повторения). В связи с этим шифр является крайне слабым и исходный текст можно восстановить просто проверив все возможные преобразования. (Буквы е и ё рассматривать как две разные буквы)

Неалфавитные символы — знаки препинания, пробелы, цифры — не меняются.

---

# Входные данные:
Файл `SecretMessage.txt`

# Выходные данные:
Множество файлов,  
Где,  имя бога - има файла,
      описание - тело файла.
т.е. Если на вход была получена строка:  
`Жэ – ицк уыхг. Чшмлщъзйужущж й цишзпм ямуцймтз ыймхязххцкц уыххгф лрщтцф р уыххгф щмшчцф.`  
То в результате сдвига на 25 позиций алфавита, будет получена строка:  
`Ях – бог луны. Представлялся в образе человека увенчанного лунным диском и лунным серпом.`  
То необходимо сохранить текст
```
Бог луны. Представлялся в образе человека увенчанного лунным диском и лунным серпом.
```
Внутри файла `Ях.txt`

# Условия  

В корректно расшифрованной строке обязательно будет присутствовать текст `бог`, я гарантирую это  

Не использовать встроенные функции ord() и chr()  

---

# Материалы для самостоятельного изучения

## Работа с файлами  

https://metanit.com/python/tutorial/4.1.php  
https://metanit.com/python/tutorial/4.2.php  

## Коллекции
https://docs.python.org/3/library/collections.html#deque-objects  
^ Русицифированный вариант https://pythonworld.ru/moduli/modul-collections.html  
п.с. обрати внимание на метод **.rotate()**

### Дикие хинты, не читай ниже, пока не отчаялся.

Статья "Если бы у Цезаря был Питон в 50 году до н.э."  
https://impythonist.wordpress.com/2014/09/11/alas-julius-caesar-doesnt-have-python-in-50-bc/  
Статья содержит реализацию функций, когда сдвиг известен.

Статья с более подробным разбором задачи, но с использованием ASCII таблиц.  
http://inventwithpython.com/chapter14.html  
Тут может быть интересна функция по BruteForce атаке.
