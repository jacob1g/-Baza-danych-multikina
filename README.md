# 🎬 Projekt bazy danych — Multikino

**Autor:** Kuba Pietrzykowski  
**Technologia:** Microsoft SQL Server (T-SQL)  
**Typ projektu:** Projekt studencki  

---

## 📌 Cel projektu

Projekt przedstawia relacyjną bazę danych służącą do przechowywania i przetwarzania informacji związanych z działalnością multikina.  
Baza umożliwia zarządzanie danymi o filmach, salach kinowych, seansach oraz sprzedanych biletach, a także analizę sprzedaży i dochodów.

---

## 📋 Wymagania projektowe

Projekt został wykonany zgodnie z wymaganiami uczelni:

- Minimum **6 tabel** (projekt jednoosobowy)
- Minimum **2 ograniczenia CHECK**
- Relacje między tabelami przy użyciu **FOREIGN KEY**
- Minimum **2 widoki**, w tym przynajmniej jeden agregujący
- Opis tabel, widoków oraz diagram ERD
- Temat: **Baza danych multikina**
- Przechowywanie informacji o:
  - filmach  
  - salach  
  - seansach  
  - sprzedanych biletach  

---

## 🗂️ Struktura bazy danych

Projekt zawiera następujące tabele:

### 🎞️ Filmy
Przechowuje informacje o filmach, takie jak tytuł, gatunek, czas trwania oraz rok produkcji.  
Zastosowano ograniczenia CHECK zapewniające poprawność danych.

### 🏛️ Sale
Zawiera dane o salach kinowych, w tym nazwę sali, liczbę miejsc oraz informację o obsłudze projekcji 3D.

### 📅 Seanse
Przechowuje informacje o zaplanowanych seansach, przypisując film do sali i daty projekcji.  
Tabela powiązana z **Filmy** i **Sale** poprzez klucze obce.

### 🎟️ Bilety
Zawiera informacje o sprzedanych biletach, numerach miejsc oraz osobach kupujących.  
Zastosowano ograniczenie zapobiegające sprzedaży dwóch biletów na to samo miejsce w ramach jednego seansu.

### 👨‍💼 Pracownicy
Przechowuje dane pracowników kina, takie jak imię, nazwisko, stanowisko oraz wynagrodzenie.

---

## 🔗 Relacje między tabelami

- **Seanse → Filmy** — każdy seans dotyczy jednego filmu  
- **Seanse → Sale** — każdy seans odbywa się w jednej sali  
- **Bilety → Seanse** — każdy bilet przypisany jest do konkretnego seansu  

---

## 🔐 Ograniczenia i spójność danych

W projekcie zastosowano:

- PRIMARY KEY  
- FOREIGN KEY  
- CHECK (np. dodatnia cena biletu, dodatnie wynagrodzenie, dodatni czas trwania filmu)  
- UNIQUE (blokada sprzedaży dwóch biletów na to samo miejsce)

Dzięki temu baza zachowuje spójność i ogranicza możliwość wprowadzania błędnych danych.

---

## 👁️ Widoki

### 📄 `SzczegolySeansow`
Wyświetla szczegóły seansów wraz z:
- tytułem filmu  
- nazwą sali  
- datą seansu  
- ceną biletu  

Widok ułatwia przegląd repertuaru kina.

---

### 📊 `SprzedazBiletow` (widok agregujący)
Pokazuje:
- liczbę sprzedanych biletów na każdy seans  
- łączny dochód z danego seansu  

Widok wykorzystuje funkcje agregujące i służy do analizy sprzedaży.

---

## 🗺️ Diagram ERD

Diagram relacji między tabelami został przygotowany w Microsoft SQL Server Management Studio i przedstawia powiązania pomiędzy encjami.

---

## 📂 Zawartość repozytorium

