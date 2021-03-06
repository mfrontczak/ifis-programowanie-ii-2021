# Programowanie II - Lab 3

**Legenda**

📖 - proszę przeczytać

📝 - warte zapamiętania / zanotowania

⚠️ - zwróć uwagę

✏️ - zadanie do wykonania

🔍 - poszukaj w internecie

## Zadanie

Stwórz skrypt do obsługi Banku.

Skrypt powinien implementować następujące klasy:

* `Bank` - do przechowywania informacji o kontach bankowych (klasa Account), oraz nazwy banku.
* `Account` - do przechowywania informacji o użytkowniku konta np. imię i nazwisko, numer konta bankowego (powinien być unikalny), oraz saldo.
* `WireTransfer` - do przechowywania informacji o przelewach np. identyfikator porządkowy dla całego banku, z jakiego numeru konta, na jaki numer konta i kwota na jaką został dokonany przelew.

**Przykład do użycia:**

Zaimplementuj:

* Klasa `Bank` powinna implementować metodę `deposit` która będzie wyliczać sumę wszystkich depozytów jakie znajdują się na kontach klientów.
* Klasa `Account` powinna posiadać historię przelewów z/na konto.
* Klasa `Account` powinna implementować metodę `verify_balance` która sprawdzi czy kwota na koncie zgadza się z sumą przelewów z/na konta.

⚠️ Klasy mogą potrzebować jeszcze dodatkowych atrybutów i funkcji - zastanów się jakie.
