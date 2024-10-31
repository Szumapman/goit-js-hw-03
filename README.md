# Zadanie domowe #3 - JavaScript

* Utwórz repozytorium `goit-js-hw-03`.
* Utwórz osobny plik z rozszerzeniem `.js` dla każdego z zadań 1-3.
* Przeczytaj każde zadanie i wykonaj je w edytorze kodu.
* Upewnij się, że kod jest sformatowany przy użyciu `Prettier` i że po otwarciu aktywnej strony zadania w konsoli nie ma żadnych błędów ani ostrzeżeń.
* Prześlij swoje zadanie domowe do sprawdzenia

### Zadanie 1. Generator slug

Zanim rozwiążemy ten problem, zdefiniujmy nowy termin!

Termin **slug** — to czytelny dla człowieka unikalny identyfikator używany w tworzeniu stron internetowych do tworzenia czytelnych adresów URL.


Na przykład, zamiast wyświetlać użytkownikowi `mysite.com/posts/1q8fh74tx`, w pasku adresu, możesz utworzyć `slug` z tytułu artykułu. W rezultacie adres będzie przyjemniejszy w odbiorze: `mysite.com/posts/arrays-for-beginners`.


**Slug** jest zawsze ciągiem małych liter, z wyrazami oddzielonymi myślnikami.

Czy to jest jasne? Zatem wykonajmy zadanie!


Napisz funkcję `slugify(title)`, która przyjmuje tytuł artykułu, parametr `title` i zwraca `slug` utworzony z tego ciągu.

* Wartością parametru `title` będą ciągi, których słowa są oddzielone tylko spacjami.
* Wszystkie znaki `slug` muszą być pisane małymi literami.
* Wszystkie słowa `slug` muszą być oddzielone myślnikami.


Weź poniższy kod i wstaw go po deklaracji swojej funkcji, aby sprawdzić, czy działa poprawnie. Konsola wyświetli wyniki jego działania.
```
console.log(slugify("Arrays for begginers")); // "arrays-for-begginers"
console.log(slugify("English for developer")); // "english-for-developer"
console.log(slugify("Ten secrets of JavaScript")); // "ten-secrets-of-javascript"
console.log(slugify("How to become a JUNIOR developer in TWO WEEKS")); // "how-to-become-a-junior-developer-in-two-weeks"
```

### Zadanie 2. Kompozycja tablic

Napisz funkcję o nazwie `makeArray`, która przyjmuje trzy parametry: `firstArray` (tablica), `secondArray` (tablica) i `maxLength` (liczba). Funkcja musi utworzyć nową tablicę zawierającą wszystkie elementy z `firstArray`, a następnie wszystkie elementy z `secondArray`.


* Jeśli liczba elementów w nowej tablicy przekracza `maxLength`, funkcja musi zwrócić kopię tablicy o długości elementów `maxLength`.
* W przeciwnym razie funkcja powinna zwrócić całą nową tablicę.


Weź poniższy kod i wstaw go po deklaracji swojej funkcji, aby sprawdzić poprawność jej działania. Konsola wyświetli wyniki jego działania.
```
console.log(makeArray(["Mango", "Poly"], ["Ajax", "Chelsea"], 3)); // ["Mango", "Poly", "Ajax"]
console.log(makeArray(["Mango", "Poly", "Houston"], ["Ajax", "Chelsea"], 4)); // ["Mango", "Poly", "Houston", "Ajax"]
console.log(makeArray(["Mango"], ["Ajax", "Chelsea", "Poly", "Houston"], 3)); // ["Mango", "Ajax", "Chelsea"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 2)); // ["Earth", "Jupiter"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 4)); // ["Earth", "Jupiter", "Neptune", "Uranus"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus", "Venus"], 0)); // []
```

### Zadanie 3. Filtrowanie tablicy liczb

Napisz funkcję `filterArray(numbers, value)`, która jako parametry przyjmuje tablicę liczb (`numbers`) i wartość (`value`). Funkcja powinna zwrócić nową tablicę zawierającą tylko te liczby z tablicy `numbers`, które są większe niż `value`.


Wewnątrz funkcji:

* Utwórz pustą tablicę, do której będziesz dodawać pasujące liczby.
* Użyj pętli do iteracji przez każdy element tablicy `numbers`.
* Użyj warunkowej instrukcji `if` wewnątrz pętli, aby sprawdzić każdy element i dodać go do tablicy.
* Zwróć nową tablicę z pasującymi liczbami jako wynik.


Weź poniższy kod i wstaw go po deklaracji funkcji, aby sprawdzić, czy działa poprawnie. Konsola wyświetli wyniki jego działania.
```
console.log(filterArray([1, 2, 3, 4, 5], 3)); // [4, 5]
console.log(filterArray([1, 2, 3, 4, 5], 4)); // [5]
console.log(filterArray([1, 2, 3, 4, 5], 5)); // []
console.log(filterArray([12, 24, 8, 41, 76], 38)); // [41, 76]
console.log(filterArray([12, 24, 8, 41, 76], 20)); // [24, 41, 76]
```
