# Programowanie II - Lab 2

**Legenda**

馃摉 - prosz臋 przeczyta膰

馃摑 - warte zapami臋tania / zanotowania

鈿狅笍 - zwr贸膰 uwag臋

鉁忥笍 - zadanie do wykonania

馃攳 - poszukaj w internecie

## Wprowadzenie
Klasa to zdefiniowany zbi贸r atrybut贸w i funkcji (metod). Nowy obiekt stworzony z danej klasy nazywamy **instancj膮**. Interakcja z pozosta艂ymi obiektami odbywa si臋 przez wcze艣niej zdefiniowane metody.

### minimalna definicja klasy
Aby zdefiniowa膰 klas臋 nale偶y u偶y膰 s艂owa kluczowego `class`, dowoln膮 nazw臋 (najlepiej zaczynaj膮c膮 si臋 z du偶ej litery) oraz dwukropek.
```python
class Nazwa:
    pass
```

S艂owo kluczowe `pass` odgrywa tutaj kluczow膮 rol臋, w Pythonie nie ma mo偶liwo艣ci pozostawienia pustej definicji klasy/funkcji oraz bloku instrukcji sterowania.

### Tworzenie instacji z klasy

przyk艂ad:
```python
# Definicja klasy
class Person:
    name = None

# Tworzenie nowego obiektu (nowej instancji)
p1 = Person()
p2 = Person()

# Przypisanie warto艣ci do zmiennej name dla obiektu p1
p1.name = 'Jordan'

# Przypisanie warto艣ci do zmiennej name dla obiektu p2
p2.name = 'Kevin'

print(f"{p1.name}, {p2.name}")
```

### Konstruktor
Bardzo wa偶nym elementem tworzenia klasy jest konstruktor. Konstruktor jest to metoda `__init__` kt贸ra definiuje jakie parametry przyjmuje nasza klasa. 
Metoda `__init__` (oraz wi臋kszo艣膰 metod definiowanych w klasie) zawsze powinna posiada膰 przynajmniej jeden argument `self`, umieszczony na pocz膮tku listy arugment贸w.

Argument `self` jest referencj膮 do instancji obiektu (do samego siebie). Poprzez `self` uzyskujemy dost臋p do zmiennych i innych metod danego obiektu.

przyk艂ad:
```python
# Definicja klasy
class Person:
    def __init__(self, name):
        self.name = name
    

# Tworzenie nowego obiektu (nowej instancji)
p1 = Person('Jordan')
p2 = Person('Kevin')

print(f"{p1.name}, {p2.name}")
```


#### Definiowanie metod klasy

Przyk艂ad:
```python
# Definicja klasy
class Student:
    def __init__(self, name, gpa):
        self.name = name
        self.gpa = gpa
    def introduce(self):
        print(f"Hello! My name is {self.name} and my GPA is {self.gpa}/4.0 .")

# Tworzenie nowego obiektu
s1 = Student()
# Przypisanie warto艣ci dla zmiennej name "znajduj膮cej si臋" w obiekcie s1
s1.name = 'Paul'
s1.gpa = 5
# Wywo艂anie funkcji (metody) obiektu s1
s1.introduce()
```


przyk艂ad:
```python
# Definicja klasy
class Person:
    def __init__(self, name):
        self.name = name
    
    def change_name(self, new_name):
        self.name = new_name
        
    def print_name(self):
        print(f"My name is {self.name}")
        
    def __str__(self):
        return self.name
    

# Tworzenie nowego obiektu (nowej instancji)
p1 = Person('Jordan')
p2 = Person('Kevin')

p2.print_name()

p1.change_name('Kenny')

print(f"{p1}, {p2}")
```

## Zadania

### Zadanie 1


Zaimplementuj klas臋 w Pythonie zgodnie z ustaleniami z poprzednich zaj臋膰:

![kosmita](./img/kosmita.png)

* Kosmita powinien posiada膰 zmienn膮 `name` do przechowywania jego imienia.
* Kosmita powinien posiada膰 zmienn膮 `age` do przechowywania jego wieku.
* Kosmita powinien posiada膰 zmienn膮 `planet` do przechowywania numeru planety na kt贸rej 偶yje (licz膮c od s艂o艅ca).

### Zadanie 2

Zaimplementuj klas臋 w Pythonie zgodnie z ustaleniami z poprzednich zaj臋膰:

![rakieta](./img/rakieta.png)

* Rakieta powinna posiada膰 zmienn膮 `mass`.
* Rakieta powinna posiada膰 zmienn膮 `fuel`.
* Rakieta powinna definiowa膰 funkcj臋 kt贸ra policzy ile paliwa zostanie zu偶yte aby wzbi膰 si臋 na wysoko艣膰 `h`.

### Zadanie 3

Zaimplementuj klas臋 w Pythonie zgodnie z ustaleniami z poprzednich zaj臋膰:

![pudelko](./img/pudelko.png)

* Pude艂ko powinno posiada膰 zmienn膮 `size` do przechowywania jego rozmiaru (w formie krotki: LENGTH, WIDTH, HEIGHT).
* Ilo艣膰 obiekt贸w przechowywana przez pude艂ko, powinna by膰 ograniczona przez jego rozmiar (zmienna `size`). 
* Dodaj metod臋 `put_in` z parametrem `other_box`, metoda `put_in` powinna sprawdza膰 czy rozmiar pude艂ka kt贸re chcemy umie艣ci膰 wewn膮trz jest mniejszy od wolnej przestrzeni.


### 馃専 Zadanie 4

Utw贸rz klas臋 `CrazyStrings` kt贸ra b臋dzie udost臋nia膰 nast臋puj膮ce metody:
* `__init__` z parametrem `text`.
* `leet` kt贸ra wy艣wietli tekst w stylu Leet. (https://pl.wikipedia.org/wiki/Leet_speak).
* `poke` kt贸ry wy艣wietli tekst naprzemiennie zmieniaj膮c litery na ma艂e i du偶e. 
* `random` kt贸ra wy艣wietli tekst w losowym stylu (dw贸ch powy偶szych).
*  Dodaj w艂asny styl.

