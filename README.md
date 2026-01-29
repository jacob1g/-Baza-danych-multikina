Typ projektu: Projekt studencki (Microsoft SQL Server)


Cel projektu

Projekt przedstawia relacyjną bazę danych służącą do przechowywania i przetwarzania informacji związanych z działalnością multikina.
Baza umożliwia zarządzanie danymi o filmach, salach kinowych, seansach oraz sprzedanych biletach, a także analizę sprzedaży i dochodów.

Zakres projektu

Baza danych została wykonana w Microsoft SQL Server i spełnia wymagania projektu studenckiego.
Zawiera tabele powiązane relacjami kluczy obcych, ograniczenia zapewniające spójność danych oraz widoki ułatwiające raportowanie.

Projekt obejmuje przechowywanie informacji o:

filmach,

salach kinowych,

seansach,

sprzedanych biletach,

pracownikach kina.

Struktura bazy danych
Tabela Filmy

Przechowuje informacje o filmach, takie jak tytuł, gatunek, czas trwania oraz rok produkcji.
Zastosowano ograniczenia CHECK zapewniające poprawność danych (np. dodatni czas trwania).

Tabela Sale

Zawiera dane o salach kinowych, w tym nazwę sali, liczbę miejsc oraz informację o obsłudze projekcji 3D.

Tabela Seanse

Przechowuje informacje o zaplanowanych seansach, przypisując film do konkretnej sali oraz daty projekcji.
Tabela jest powiązana z tabelami Filmy i Sale za pomocą kluczy obcych.

Tabela Bilety

Zawiera informacje o sprzedanych biletach, numerach miejsc oraz osobach kupujących.
Zastosowano ograniczenie uniemożliwiające sprzedaż dwóch biletów na to samo miejsce w ramach jednego seansu.

Tabela Pracownicy

Przechowuje dane pracowników kina, w tym imię, nazwisko, stanowisko oraz wynagrodzenie.

Ograniczenia i spójność danych

W projekcie wykorzystano:

klucze główne (PRIMARY KEY),

klucze obce (FOREIGN KEY),

ograniczenia CHECK (np. dodatnia cena biletu, dodatnie wynagrodzenie),

ograniczenia UNIQUE zapobiegające duplikacji miejsc na seansach.

Dzięki temu baza zachowuje integralność i minimalizuje ryzyko błędnych danych.

Widoki
Widok SzczegolySeansow

Wyświetla listę seansów wraz z tytułem filmu, nazwą sali, datą seansu oraz ceną biletu.
Widok ułatwia przegląd repertuaru kina.

Widok SprzedazBiletow

Przedstawia liczbę sprzedanych biletów dla każdego seansu oraz oblicza łączny dochód.
Widok wykorzystuje funkcje agregujące i służy do analizy sprzedaży.

Diagram bazy danych

Diagram relacji między tabelami został przygotowany w Microsoft SQL Server Management Studio i przedstawia powiązania pomiędzy encjami.

Podsumowanie

Projekt przedstawia prostą, ale spójną bazę danych spełniającą wymagania studenckie.
Struktura została zaprojektowana w sposób umożliwiający dalszą rozbudowę, np. o system rezerwacji, typy biletów lub dodatkowe raporty.
