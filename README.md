
## Prognozowanie wyników inwestycyjnych z kwantyfikacją ryzyka ##

Projekt zakłada stworzenie aplikacji desktopowej lub webowej o nazwie RiskFolio, służącej do budowania wirtualnego portfela aktywów i symulowania jego przyszłej wartości w oparciu o dane historyczne i prognozowanie metodą Monte Carlo.

---

### Członkowie zespołu ##

* Adam Bagiński
* Aleksandra Dmitruk
* Barbara Gawlik

---

### TO-DO przed poniedziałkiem

#### Adam
- W DataService.java dodać obsługę błędów połączeń sieciowych.
- Interpolacja w MonteCarloEngine.java - zamiast obcinać dane pod spółkę z najkrótszą historią notowań, stosujemy interpolację. Jeśli np. ponad 50% okresu czasowego musimy interpolować, to GUI wyrzuca nam informację o tym. Ponadto, w GUI sobie użytkownik zaznacza, czy chce mieć dane interpolowane, czy obcięte do najkrótszej historii notowań spośród instrumentów.
- Dokumentacja - sekcje 1 / 2 / 3.

#### Basia
- Model ML do wyznaczania parametrów alpha, beta, omega do GARCH. Parametry mają być zależne od rodzaju instrumentu (np. akcje dużego kopro, kryptowaluty, waluty).
- Prezentacja (slajdy)
- Dokumentacja - sekcje 4 / 5 / 6.

#### Ola
- (GUI) Instrumenty - zrobić tak, że wpisujesz nazwę, masz podpowiedzi, klikasz (zamiast wpisywania od A do Z samemu).
- (GUI) Horyzont czasowy jako suwak.
- (GUI) Opisy (czym są instrumenty, wagi, kapitał, horyzont, historia, CVaR, VaR, GARCH, wszystko ogl co tam jest), np. rozwijane gdzieś w rogu - żeby było intuicyjnie, przyjaźnie dla początkujących, bo tak pisaliśmy że będzie w konspekcie.
- (GUI) Na wykresie dodatkowa pozioma linia na wysokości y = kapitał początkowy.
- Dokumentacja - sekcje 7 / 8 / 9.

---

### Z czego składa się dokumentacja?

1. Strona tytułowa (*to oficjalny dokument, powinien dobrze wyglądać*)
2. Opis tematu, co, po co, dla kogo, cel biznesowy
3. Założenia projektowe, funkcjonalne, niefunkcjonalne
4. Schemat systemu jako całości – opis
5. Wykorzystane technologie, biblioteki
6. Opis implementacji (*krótko, ale coś by się przydało*)
7. Instrukcja wdrożeniowa (*Co jest potrzebne aby uruchomić aplikację + Instrukcja jak to zrobić*)
8. Instrukcja użytkownika
9. Podsumowanie i wnioski (*Odnośnie pracy nad projektem + Odnośnie działania*)

---

### Punktacja projektu

| Element                | Punkty |
|------------------------|--------|
| Konspekt               | 4 pkt  |
| Checkpoint             | 10 pkt |
| Praca w repozytorium   | 5 pkt  |
| Implementacja          | 21 pkt |
| Dokumentacja           | 5 pkt  |
| Prezentacja            | 5 pkt  |
| **Razem**              | **50 pkt** |

---

### Poprzednie notatki

#### Plany na kolejne wersje

1. W DataService.java dodać obsługę błędów połączeń sieciowych.
2. Dodać sposób zapisywania danych z DataService.java lokalnie, aby podczas częstego testowania nie wysyłać żądań do strony Stooq
3. W MonteCarloEngine.java zamiast obcinać dane pod spółkę z najkrótszą historią notowań, stosujemy interpolację.
4. W RiskService.java zamiast na sztywno ustawiać alpha, beta, omega, to możemy napisać prosty model ML do ich wyznaczania.
5. W GUI

	a. instrumenty - wpisujesz nazwę, masz podpowiedzi, klikasz
	
	b. horyzont - jako suwak
	
	c. opisy (tzn. czym są instrumenty, wagi, kapitał, horyzont, historia) 
	
	d. dodatkowa pozioma linia na wysokości y = kapitał początkowy
	
#### Odrzucone / do rozważenia

1. Obiektywizacja assetów - brak konkretnej korzyści

#### Dziwne błędy

Błąd przy odpalaniu MainLauncher.java
```
sty 12, 2026 1:59:27 PM com.sun.javafx.application.PlatformImpl startup
WARNING: Unsupported JavaFX configuration: classes were loaded from 'unnamed module @37c82957'
```
---

Więcej infromacji wstępnych znajduje się w pliku [Konspekt projektu](https://bitbucket.org/dmitruka/zpoif_2025_zespol_5/src/main/Projekt_KONSPEKT.pdf)

