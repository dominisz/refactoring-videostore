# Refactoring `videostore`

## Źródło
Zadanie utworzone na podstawie zadania https://github.com/unclebob/videostore

> The videostore example from Episode 3 of cleancoders.com. Based upon, but not identical to, the first chapter of Martin Fowler's classic book: Refactoring.

## Aplikacja

Aplikacja do obsługi wypożyczalni filmów zawiera następujące klasy:
- `Movie` - przechowuje informacje o filmie, istnieją trzy rodzaje filmów `REGULAR`, `NEW_RELEASE`, `CHILDRENS`, które są odmiennie traktowane
- `Rental` - przechowuje informacje o wypożyczonym filmie
- `Customer` - przechowuje informacje o kliencie

W klasie `Customer` znajduje się metoda `statement`, która tworzy podsumowanie zawierające informacje o tym jaki jest koszt wypożyczonych filmów oraz ile klient uzyskał punktów za wypożyczenia.

## Zadanie

Celem zadania jest refaktoryzacja aplikacji. W tym celu należy:
- utworzyć zestaw testów jednostkowych, szczególnie do metody `statement`
- tworzenie podsumowania `statement` przenieść do innej klasy
- zaktualizowac testy jednostkowe
- zaproponować mechanizm wygodnego zliczania `totalAmount` oraz `frequentRenterPoints` uwzględniając, że w przyszłości moga pojawić się nowe rodzaje filmów.