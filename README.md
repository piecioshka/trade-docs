# Trade Docs — Kompendium wiedzy o tradingu

<!-- npx md-to-pdf README.md -->

> Zbiór notatek edukacyjnych dotyczących tradingu, instrumentów finansowych
> (CFD, ETF, akcje, surowce) oraz praktycznych aspektów inwestowania
> na platformie [XTB](https://www.xtb.com/pl).

📄 Wersja PDF: [piecioshka.github.io/trade-docs/README.pdf](https://piecioshka.github.io/trade-docs/README.pdf)

> **Aktualność danych:** liczby zależne od oferty brokera (spready, swapy, liczba dostępnych instrumentów, limity prowizji, odsetek stratnych rachunków) zmieniają się z czasem. Ostatnia weryfikacja tego dokumentu: sierpień 2026. Przed transakcją sprawdzaj aktualną specyfikację instrumentu na platformie.

---

## Spis treści

### Część I — Podstawy

1. [Budowa świecy](#budowa-świecy)
2. [Co to jest wolumen?](#co-to-jest-wolumen)
3. [Co to jest spot?](#co-to-jest-spot)
4. [Co to jest spread?](#co-to-jest-spread)
   - [Jaki jest spread na metalach?](#jaki-jest-spread-na-metalach)
5. [Co to jest Open Interest, czyli liczba otwartych pozycji?](#co-to-jest-open-interest-czyli-liczba-otwartych-pozycji)
6. [CFD](#cfd)
   - [Co to jest pips / lot?](#co-to-jest-pips--lot)
   - [Co to jest lewar / dźwignia?](#co-to-jest-lewar--dźwignia)
7. [ETF](#etf)
   - [Co to jest ETF? Czym się różni od indeksu?](#co-to-jest-etf-czym-się-różni-od-indeksu)
   - [Co to jest iShares przy ETFach?](#co-to-jest-ishares-przy-etfach)
8. [Technika](#technika)
   - [Co to jest technika hedging?](#co-to-jest-technika-hedging)
9. [Rolowanie](#rolowanie)
   - [Jak działa rolowanie?](#jak-działa-rolowanie)
   - [Co to jest "contango" i "backwardation"?](#co-to-jest-contango-i-backwardation)
10. [Broker](#broker)
    - [Jaki broker?](#jaki-broker)
    - [Jaki broker jest najlepszy?](#jaki-broker-jest-najlepszy)
11. [Wyniki finansowe](#wyniki-finansowe)
    - [Jak się czyta wyniki finansowe?](#jak-się-czyta-wyniki-finansowe-jak-je-rozumieć-np-eps)
    - [Dlaczego gdy są dobre wyniki to spółka nie rośnie?](#dlaczego-gdy-są-dobre-wyniki-finansowe-to-spółka-nie-rośnie-np-duolingo)
12. [Makler](#makler)
    - [Kto to jest?](#kto-to-jest)
    - [Czym się zajmuje?](#czym-się-zajmuje)
    - [Jak można nim zostać?](#jak-można-nim-zostać)
    - [Czy polecacie zdanie egzaminu?](#czy-polecacie-zdanie-egzaminu)
    - [Czy inwestor indywidualny potrzebuje licencji maklerskiej?](#czy-inwestor-indywidualny-potrzebuje-licencji-maklerskiej)
13. [Pre-market i after-market](#pre-market-i-after-market)
    - [Różnice między pre/after-market a regularnym rynkiem](#różnice-między-preafter-market-a-regularnym-rynkiem)
    - [Zalety handlu w pre/after-market](#zalety-handlu-w-preafter-market)
    - [Wady handlu w pre/after-market](#wady-handlu-w-preafter-market)
14. [Sesje rynkowe](#sesje-rynkowe)
15. [Płynność](#płynność)
    - [Co to jest płynność?](#co-to-jest-płynność)
    - [Konsekwencje handlu na rynku o mniejszej płynności](#konsekwencje-handlu-na-rynku-o-mniejszej-płynności)
    - [Czy mniejsza płynność zawsze oznacza większe ryzyko?](#czy-mniejsza-płynność-zawsze-oznacza-większe-ryzyko)
    - [Strategie handlu na rynku o mniejszej płynności](#strategie-handlu-na-rynku-o-mniejszej-płynności)
    - [Różnice między rynkiem o mniejszej a większej płynności](#różnice-między-rynkiem-o-mniejszej-a-większej-płynności)

### Część II — Przewodnik po CFD na XTB

16. [Czym jest CFD? (porównanie z akcjami)](#czym-jest-cfd-porównanie-z-akcjami)
    - [Kluczowe różnice na pierwszy rzut oka](#kluczowe-różnice-na-pierwszy-rzut-oka)
17. [Słownik pojęć CFD](#słownik-pojęć-cfd)
    - [Spread](#spread)
    - [Lot (wielkość pozycji)](#lot-wielkość-pozycji)
    - [Dźwignia finansowa (leverage)](#dźwignia-finansowa-leverage)
    - [Depozyt zabezpieczający (margin)](#depozyt-zabezpieczający-margin)
    - [Swap (punkty swapowe)](#swap-punkty-swapowe)
    - [Przewalutowanie](#przewalutowanie)
    - [Pozycja LONG i SHORT](#pozycja-long-i-short)
    - [Typy zleceń](#typy-zleceń)
    - [Stop Loss (SL)](#stop-loss-sl)
    - [Wielkość pozycji (position sizing)](#wielkość-pozycji-position-sizing)
    - [Take Profit (TP)](#take-profit-tp)
    - [Rolowanie (rollover)](#rolowanie-rollover)
18. [Przykład 1: CFD na ropę naftową (OIL)](#przykład-1-cfd-na-ropę-naftową-oil)
19. [Przykład 2: CFD na spółkę amerykańską (np. AAPL.US)](#przykład-2-cfd-na-spółkę-amerykańską-np-aaplus)
20. [Przykład 3: CFD na spółkę polską (np. KGHM.PL)](#przykład-3-cfd-na-spółkę-polską-np-kghmpl)
21. [Porównanie: ropa vs spółka US vs spółka PL](#porównanie-ropa-vs-spółka-us-vs-spółka-pl)
22. [Najczęstsze błędy początkujących](#najczęstsze-błędy-początkujących)
    - [Ignorowanie dźwigni](#1-ignorowanie-dźwigni)
    - [Brak Stop Loss](#2-brak-stop-loss)
    - [Trzymanie CFD jak akcji](#3-trzymanie-cfd-jak-akcji)
    - [Ignorowanie kosztów (spread + swap)](#4-ignorowanie-kosztów-spread--swap)
    - [Overtrading](#5-overtrading)
    - [Handel bez planu](#6-handel-bez-planu)
    - [Trzymanie lewarowanej pozycji przez weekend lub publikację wyników](#7-trzymanie-lewarowanej-pozycji-przez-weekend-lub-publikację-wyników)
23. [Podatki od CFD i akcji (Polska)](#podatki-od-cfd-i-akcji-polska)
24. [Źródła i przydatne linki](#źródła-i-przydatne-linki)

---

# Część I — Podstawy

## Budowa świecy

Świeca japońska (candlestick) to sposób prezentacji ruchu ceny w danym okresie czasu.
Składa się z:

- **Korpus (body)** — prostokąt między ceną otwarcia a ceną zamknięcia.
  - Świeca zielona/biała — cena zamknięcia wyżej niż otwarcia (wzrost).
  - Świeca czerwona/czarna — cena zamknięcia niżej niż otwarcia (spadek).
- **Górny knot (upper shadow/wick)** — linia powyżej korpusu, pokazuje najwyższą cenę w danym okresie.
- **Dolny knot (lower shadow/wick)** — linia poniżej korpusu, pokazuje najniższą cenę w danym okresie.

Każda świeca zawiera 4 wartości: **Open** (otwarcie), **High** (maksimum), **Low** (minimum), **Close** (zamknięcie) — w skrócie OHLC.

![Budowa świecy japońskiej](assets/candlestick.svg)

## Co to jest wolumen?

Wolumen (volume) to liczba akcji, kontraktów lub jednostek danego instrumentu, które zostały wymienione (kupione/sprzedane) w określonym czasie.

- **Wysoki wolumen** — duże zainteresowanie instrumentem, większa płynność, ruchy cenowe są bardziej wiarygodne.
- **Niski wolumen** — małe zainteresowanie, mniejsza płynność, łatwiej o manipulację ceną.

Wolumen jest często używany do potwierdzania trendów — wzrost ceny przy rosnącym wolumenie sugeruje silny trend wzrostowy.

## Co to jest spot?

Spot (rynek kasowy) to transakcja, w której kupno i sprzedaż instrumentu finansowego odbywa się po bieżącej cenie rynkowej z natychmiastową (lub niemal natychmiastową) dostawą.

- Cena spot to **aktualna cena rynkowa** danego aktywa.
- W przeciwieństwie do kontraktów terminowych (futures), na rynku spot nie ma daty wygaśnięcia.
- Przykład: kupujesz złoto po cenie spot — płacisz bieżącą cenę i otrzymujesz złoto "od razu".

## Co to jest spread?

Spread to różnica między ceną kupna (ask) a ceną sprzedaży (bid) danego instrumentu.

- **Bid** — cena, po której możesz sprzedać instrument (z perspektywy inwestora).
- **Ask** — cena, po której możesz kupić instrument (z perspektywy inwestora).
- **Spread = Ask - Bid** (Ask jest zawsze wyższy niż Bid).

Im mniejszy spread, tym niższy koszt transakcji dla tradera. To, czy spread jest "prowizją brokera", zależy od modelu egzekucji:

- **Market maker** (np. XTB na CFD) - broker sam kwotuje ceny i zarabia na spreadzie; osobnej prowizji zwykle nie ma. Spread jest wtedy de facto prowizją.
- **ECN / STP** - broker przekazuje zlecenia na rynek międzybankowy. Spread jest rynkowy (na EUR/USD często 0-0,5 pipsa), ale dochodzi **osobna prowizja** za każdą transakcję.

Porównując brokerów, licz **całkowity koszt** (spread + prowizja), a nie samą szerokość spreadu.

Więcej na przykładzie xStation: [Spread](#spread) w części II.

### Jaki jest spread na metalach?

Spread na metalach szlachetnych zależy od brokera, pory dnia i płynności rynku. Orientacyjne wartości:

| Metal                  | Typowy spread |
| ---------------------- | ------------- |
| Złoto (GOLD/XAUUSD)    | 0.3–0.5 USD   |
| Srebro (SILVER/XAGUSD) | 0.03–0.05 USD |
| Platyna (PLATINUM)     | 1.5–3.0 USD   |
| Pallad (PALLADIUM)     | 3.0–8.0 USD   |

Uwaga: spread może się znacząco poszerzać w godzinach nocnych, podczas ważnych publikacji makroekonomicznych lub w okresach niskiej płynności.

## Co to jest Open Interest, czyli liczba otwartych pozycji?

Open Interest (OI) to łączna liczba otwartych (nierozliczonych) kontraktów na rynku futures lub opcji.

- Każda transakcja ma kupującego i sprzedającego — jeden kontrakt to jedna pozycja w Open Interest.
- **OI rośnie**, gdy nowy kupujący i nowy sprzedający otwierają pozycje.
- **OI maleje**, gdy obie strony zamykają swoje pozycje.
- **OI nie zmienia się**, gdy jeden trader zamyka pozycję, a drugi ją przejmuje.

Zastosowanie:

- Rosnący OI + rosnąca cena = silny trend wzrostowy.
- Rosnący OI + spadająca cena = silny trend spadkowy.
- Malejący OI = trend słabnie, możliwa zmiana kierunku.

## CFD

### Co to jest pips / lot?

**Pips** (pip, od "price interest point" lub "percentage in point" - obie wersje są w obiegu) — standardowa jednostka zmiany kursu na rynku Forex.

- Dla większości par walutowych 1 pips = 0.0001 (czwarte miejsce po przecinku).
- Dla par z jenem (JPY) 1 pips = 0.01 (drugie miejsce po przecinku).
- Przykład: jeśli EUR/USD zmieni się z 1.1000 na 1.1001 — to zmiana o 1 pips.
- **Pips to nie punkt (point/tick).** Brokerzy kwotują dziś z dodatkowym miejscem po przecinku (1.10005), a ta ostatnia cyfra to **punkt** = 0,1 pipsa. Spread "3 punkty" i "3 pipsy" różnią się dziesięciokrotnie - sprawdzaj, w czym platforma podaje spread. Poza Forexem (indeksy, surowce, akcje) mówi się o punktach lub tickach, nie pipsach.

**Lot** — standardowa jednostka wielkości transakcji.

- **1 lot standardowy** = 100 000 jednostek waluty bazowej.
- **1 mini lot** = 10 000 jednostek.
- **1 mikro lot** = 1 000 jednostek.
- Przykład: kupno 1 lota EUR/USD oznacza kupno 100 000 EUR.

**Ile jest wart 1 pips?** To liczba, którą trzeba znać przed ustawieniem Stop Lossa:

| Wolumen           | Wartość 1 pipsa (EUR/USD) | Ruch o 10 pipsów |
| ----------------- | ------------------------- | ---------------- |
| 1 lot (100 000)   | 10 USD                    | 100 USD          |
| 0,1 lota (10 000) | 1 USD                     | 10 USD           |
| 0,01 lota (1 000) | 0,10 USD                  | 1 USD            |

Wzór: wartość pipsa = wielkość pozycji × 0,0001 (dla par z USD jako walutą kwotowaną). Dla innych par wynik trzeba jeszcze przeliczyć na walutę konta.

Co znaczy 1 lot na ropie, akcjach i indeksach: [Lot (wielkość pozycji)](#lot-wielkość-pozycji) w części II. Jak przeliczyć ryzyko na loty: [Wielkość pozycji (position sizing)](#wielkość-pozycji-position-sizing).

### Co to jest lewar / dźwignia?

Lewar (leverage / dźwignia finansowa) pozwala kontrolować dużą pozycję przy użyciu niewielkiego kapitału własnego (tzw. depozytu zabezpieczającego / margin).

- **Dźwignia 1:10** oznacza, że wpłacasz 1 000 PLN, a kontrolujesz pozycję wartą 10 000 PLN.
- **Dźwignia 1:30** oznacza, że wpłacasz 1 000 PLN, a kontrolujesz pozycję wartą 30 000 PLN.

Korzyści i ryzyka:

- Dźwignia **zwielokrotnia zyski**, ale tak samo **zwielokrotnia straty**.
- Przy dźwigni 1:10 ruch ceny o 1% w Twoją stronę daje 10% zysku, ale ruch o 1% przeciw Tobie to 10% straty.
- W UE maksymalna dźwignia dla klientów detalicznych to 1:30 (regulacje [ESMA](https://www.esma.europa.eu/)).

Limity dźwigni per klasa instrumentu, depozyt zabezpieczający i Margin Stop: [Dźwignia finansowa (leverage)](#dźwignia-finansowa-leverage) i [Depozyt zabezpieczający (margin)](#depozyt-zabezpieczający-margin) w części II.

## ETF

### Co to jest ETF? Czym się różni od indeksu?

**ETF** (Exchange-Traded Fund) — fundusz notowany na giełdzie, który można kupować i sprzedawać jak zwykłe akcje.

- ETF odwzorowuje zachowanie indeksu, sektora, surowca lub innego aktywa.
- Kupując 1 jednostkę ETF, inwestujesz jednocześnie w dziesiątki lub setki spółek.

**Indeks** — to tylko **miara statystyczna**, np. WIG20, S&P 500, NASDAQ-100. Nie można go bezpośrednio kupić.

| Cecha            | Indeks                       | ETF                            |
| ---------------- | ---------------------------- | ------------------------------ |
| Czy można kupić? | Nie (to tylko wskaźnik)      | Tak (notowany na giełdzie)     |
| Koszty           | Brak (nie jest instrumentem) | Opłata za zarządzanie (TER)    |
| Dywidendy        | Nie wypłaca                  | Może wypłacać lub reinwestować |
| Przykład         | S&P 500                      | SPDR S&P 500 ETF (SPY)         |

### Co to jest iShares przy ETFach?

**[iShares](https://www.ishares.com/)** to marka ETF-ów należąca do **[BlackRock](https://www.blackrock.com/)** — największego na świecie zarządzającego aktywami.

- iShares to nie osobny typ ETF, lecz **nazwa handlowa** serii funduszy ETF.
- BlackRock oferuje pod marką iShares ponad 1 300 ETF-ów na całym świecie.
- Przykłady: iShares Core S&P 500 (IVV), iShares MSCI World (IWDA), iShares Core MSCI Emerging Markets (IEMG).
- Inne popularne marki ETF to: [Vanguard](https://www.vanguard.com/), [SPDR](https://www.ssga.com/) (State Street), [Xtrackers](https://etf.dws.com/) (DWS), [Amundi](https://www.amundietf.com/).

## Technika

### Co to jest technika hedging?

Hedging (zabezpieczanie) to strategia polegająca na otwieraniu pozycji przeciwstawnej w celu ograniczenia ryzyka strat.

Przykłady:

- Masz akcje spółki X i boisz się spadków — kupujesz opcję put na tę spółkę. Jeśli cena spadnie, zysk z opcji kompensuje stratę na akcjach.
- Eksporter otrzyma płatność w USD za 3 miesiące — sprzedaje kontrakty futures na USD, by zabezpieczyć się przed spadkiem kursu dolara.
- Posiadasz portfel akcji europejskich — kupujesz ETF short na indeks, by zabezpieczyć się przed ogólnymi spadkami rynku.

Hedging nie eliminuje ryzyka całkowicie, ale **ogranicza potencjalną stratę** kosztem zmniejszenia potencjalnego zysku.

## Rolowanie

### Jak działa rolowanie?

Rolowanie to proces przeniesienia pozycji z wygasającego kontraktu terminowego (futures) na kontrakt z późniejszą datą wygaśnięcia.

Jak to wygląda w praktyce:

1. Zbliża się data wygaśnięcia kontraktu, np. futures na ropę czerwiec 2026.
2. Zamykasz pozycję na kontrakcie czerwcowym.
3. Otwierasz nową pozycję na kontrakcie lipcowym (lub późniejszym).

Dlaczego to ważne:

- Kontrakty futures mają **datę wygaśnięcia** — nie możesz ich trzymać w nieskończoność.
- Przy rolowaniu może wystąpić różnica w cenie między starym a nowym kontraktem.
- U brokerów CFD (np. XTB) rolowanie często odbywa się **automatycznie**, a różnica w cenie jest rozliczana jako korekta na koncie. Jak dokładnie liczona jest korekta i jak sprawdzić ją z wyprzedzeniem: [Rolowanie (rollover)](#rolowanie-rollover) w części II.

### Co to jest "contango" i "backwardation"?

To dwa stany opisujące relację między ceną spot a cenami kontraktów futures.

**Contango** — cena futures jest **wyższa** niż cena spot.

- Sytuacja "normalna" na wielu rynkach (np. surowce), bo przechowywanie towaru kosztuje.
- Rolowanie w contango generuje **stratę** — sprzedajesz tańszy kontrakt, kupujesz droższy.
- Przykład: ropa spot 70 USD, kontrakt na za miesiąc 72 USD.
- Strata nie pojawia się w dniu rolowania, tylko rozkłada się w czasie: nowy kontrakt kupiony po 72 USD będzie "zjeżdżał" do ceny spot w miarę zbliżania się wygaśnięcia (ujemny roll yield). Nawet gdy spot stoi w miejscu, pozycja LONG traci.

**Backwardation** — cena futures jest **niższa** niż cena spot.

- Występuje, gdy rynek oczekuje spadku cen lub jest wysoki popyt na natychmiastową dostawę.
- Rolowanie w backwardation generuje **zysk** — sprzedajesz droższy kontrakt, kupujesz tańszy.
- Przykład: ropa spot 70 USD, kontrakt na za miesiąc 68 USD.

**A co z CFD?** Powyższe dotyczy samodzielnego rolowania futures. Na CFD broker roluje automatycznie i wyrównuje różnicę cen korektą na rachunku, więc sam moment rolowania jest dla Ciebie neutralny (szczegóły w części II, sekcja [Rolowanie (rollover)](#rolowanie-rollover)). Koszt contango nie znika jednak - realizuje się przez stopniowy zjazd ceny nowego kontraktu do spotu, dokładnie tak jak na futures.

![Krzywa terminowa: contango vs backwardation](assets/contango.svg)

## Broker

### Jaki broker?

Wybór brokera zależy od tego, czym chcesz handlować i jakie masz potrzeby. Popularne kategorie:

- **Brokerzy CFD** — oferują kontrakty na różnicę kursową (Forex, indeksy, surowce, akcje). Przykłady: [XTB](https://www.xtb.com/pl), [Plus500](https://www.plus500.com/), [eToro](https://www.etoro.com/).
- **Brokerzy giełdowi** — umożliwiają kupno prawdziwych akcji i ETF-ów. Przykłady: XTB, [DEGIRO](https://www.degiro.pl/), [Interactive Brokers](https://www.interactivebrokers.com/), [mBank](https://www.mbank.pl/) (eMakler), [Bossa](https://bossa.pl/).
- **Brokerzy kryptowalut** — specjalizują się w handlu kryptowalutami. Przykłady: [Binance](https://www.binance.com/), [Kraken](https://www.kraken.com/), [Coinbase](https://www.coinbase.com/).

### Jaki broker jest najlepszy?

Nie ma jednego "najlepszego" brokera — zależy od indywidualnych potrzeb. Na co zwrócić uwagę:

| Kryterium | Co sprawdzić                                                                                                                                                      |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Regulacja | Czy broker jest nadzorowany ([KNF](https://www.knf.gov.pl/), [CySEC](https://www.cysec.gov.cy/), [FCA](https://www.fca.org.uk/), [BaFin](https://www.bafin.de/))? |
| Koszty    | Spread, prowizje, opłaty za przewalutowanie, opłata za brak aktywności                                                                                            |
| Oferta    | Jakie instrumenty są dostępne (akcje, ETF, CFD, Forex)?                                                                                                           |
| Platforma | Czy platforma jest intuicyjna? Czy ma aplikację mobilną?                                                                                                          |
| Wypłaty   | Jak szybko i tanio można wypłacić środki?                                                                                                                         |
| Edukacja  | Czy broker oferuje materiały edukacyjne?                                                                                                                          |

Popularne wybory wśród polskich inwestorów:

- **XTB** — polski broker, 0% prowizji na akcjach i ETF (do 100 000 EUR/mies.), regulowany przez KNF.
- **DEGIRO** — niskie prowizje, szeroka oferta ETF, regulowany w Holandii.
- **Interactive Brokers** — profesjonalny broker, ogromna oferta instrumentów, niskie prowizje, ale bardziej skomplikowana platforma.

## Wyniki finansowe

### Jak się czyta wyniki finansowe? Jak je rozumieć? np. EPS

Najważniejsze wskaźniki w raportach finansowych spółek:

**Rachunek zysków i strat:**

- **Revenue / Sales (przychody)** — ile spółka zarobiła ze sprzedaży.
- **Net Income (zysk netto)** — ile zostało po odjęciu wszystkich kosztów i podatków.
- **EPS (Earnings Per Share)** — zysk netto podzielony przez liczbę akcji. Pokazuje, ile zysku przypada na jedną akcję. Np. zysk netto 1 mld PLN / 500 mln akcji = EPS 2 PLN.

**Porównywanie z oczekiwaniami:**

- Przed publikacją wyników analitycy podają **konsensus** (prognozę).
- Jeśli wynik jest **powyżej konsensusu** = "beat" (pozytywne zaskoczenie).
- Jeśli wynik jest **poniżej konsensusu** = "miss" (rozczarowanie).

**Inne ważne wskaźniki:**

- **P/E (Price to Earnings)** — cena akcji / EPS. Mówi, ile lat zysku płacisz za spółkę.
- **P/S (Price to Sales)** — cena / przychody. Używany dla spółek, które jeszcze nie generują zysku.
- **EBITDA** — zysk operacyjny przed amortyzacją, odsetkami i podatkami. Pokazuje rentowność podstawowej działalności.
- **Free Cash Flow** — wolne przepływy pieniężne. Ile gotówki spółka faktycznie generuje.
- **Guidance** — prognoza spółki na przyszłe kwartały. Często ważniejsza niż same wyniki.

### Dlaczego gdy są dobre wyniki finansowe to spółka nie rośnie? np. Duolingo

To częsty scenariusz i może mieć kilka przyczyn:

1. **"Buy the rumor, sell the news"** — rynek wycenił dobre wyniki z wyprzedzeniem. Inwestorzy kupowali w oczekiwaniu na wyniki, a po publikacji realizują zyski.

2. **Wyniki dobre, ale guidance słabe** — spółka pobiła oczekiwania za ostatni kwartał, ale prognoza na przyszłość rozczarowała. Rynek patrzy w przyszłość, nie w przeszłość.

3. **Wyniki dobre, ale nie wystarczająco dobre** — przy spółkach wzrostowych (jak Duolingo) rynek oczekuje regularnego "podbijania" prognoz. Beat o 1% może nie wystarczyć, gdy wcześniej spółka biła prognozy o 10%.

4. **Zmiana narracji** — nawet przy dobrych wynikach, jeśli pojawią się obawy o model biznesowy, konkurencję, zmiany regulacyjne itp., kurs może spadać.

5. **Wysoka wycena** — spółka z P/E = 100 musi rosnąć bardzo dynamicznie, by uzasadnić cenę. Dobre wyniki mogą nie wystarczyć, jeśli wzrost zwalnia.

6. **Warunki makroekonomiczne** — podwyżki stóp procentowych, recesja, silny dolar — to wszystko może ciągnąć kurs w dół niezależnie od wyników.

## Makler

### Kto to jest?

Makler papierów wartościowych to osoba posiadająca licencję uprawniającą do pośredniczenia w obrocie instrumentami finansowymi na rynku regulowanym.

### Czym się zajmuje?

- Wykonuje zlecenia kupna i sprzedaży papierów wartościowych w imieniu klientów.
- Doradza klientom w zakresie inwestycji (makler z uprawnieniami doradczymi).
- Analizuje rynki i spółki.
- Zarządza portfelami klientów (w ramach usługi asset management).
- Dba o zgodność transakcji z regulacjami (compliance).

### Jak można nim zostać?

1. **Wykształcenie** — nie jest wymagany konkretny kierunek studiów, ale ekonomia, finanse lub matematyka ułatwiają drogę.
2. **Egzamin** — należy zdać egzamin na maklera papierów wartościowych organizowany przez [Komisję Nadzoru Finansowego (KNF)](https://www.knf.gov.pl/).
   - Egzamin składa się z pytań testowych i zadań obliczeniowych.
   - Zakres: prawo rynku kapitałowego, analiza finansowa, instrumenty finansowe, rachunkowość, matematyka finansowa.
   - Zdawalność wynosi ok. 20–30% — egzamin jest trudny.
3. **Licencja** — po zdaniu egzaminu KNF wydaje licencję maklera.
4. **Praca** — zatrudnienie w domu maklerskim, biurze maklerskim banku lub firmie inwestycyjnej.

### Czy polecacie zdanie egzaminu?

Argumenty za:

- Zdobywasz solidną wiedzę o rynkach finansowych, niezależnie od tego, czy będziesz pracować jako makler.
- Licencja otwiera drzwi do pracy w branży finansowej.
- Przygotowanie do egzaminu to intensywny kurs z finansów, prawa i rachunkowości.

Argumenty przeciw:

- Egzamin jest trudny i wymaga kilku miesięcy nauki.
- Jeśli nie planujesz kariery w branży finansowej, licencja nie jest konieczna do inwestowania na własny rachunek.
- Wiedza z egzaminu jest dość teoretyczna — praktyczne umiejętności inwestycyjne zdobywa się na rynku.

### Czy inwestor indywidualny potrzebuje licencji maklerskiej?

Nie. Licencja jest wymagana do pośredniczenia w obrocie w imieniu klientów, a nie do handlu na własny rachunek:

- **Większość inwestorów indywidualnych nie jest maklerami** — do inwestowania na własny rachunek licencja nie jest potrzebna.
- Wielu maklerów pracuje na etacie w domach maklerskich i nie inwestuje aktywnie na własny rachunek (ze względu na regulacje compliance).
- Zdanie egzaminu na maklera jest wartościowe jako potwierdzenie wiedzy, ale nie jest warunkiem koniecznym do skutecznego inwestowania.

## Pre-market i after-market

### Co to jest?

Pre-market i after-market to sesje handlowe odbywające się **poza regularnymi godzinami giełdy**.

- **Pre-market** — handel przed oficjalnym otwarciem giełdy. Na [NYSE](https://www.nyse.com/)/[NASDAQ](https://www.nasdaq.com/): 10:00-15:30 czasu polskiego (4:00-9:30 ET)
- **Regularna sesja** — 15:30-22:00 czasu polskiego (9:30-16:00 ET)
- **After-market (after-hours)** — handel po zamknięciu giełdy. Na NYSE/NASDAQ: 22:00-02:00 czasu polskiego (16:00-20:00 ET)

Uwaga na zmianę czasu: różnica między Polską a Nowym Jorkiem wynosi zwykle 6 godzin, ale USA i UE przestawiają zegary w różnych terminach. Przez ok. 3 tygodnie w roku (druga połowa marca i przełom października/listopada) różnica spada do 5 godzin i regularna sesja zaczyna się o 14:30, a kończy o 21:00 czasu polskiego.

W tych sesjach handel odbywa się na platformach ECN (Electronic Communication Network), a nie na parkiecie giełdowym.

### Różnice między pre/after-market a regularnym rynkiem

| Cecha       | Regularna sesja    | Pre/After-market                                  |
| ----------- | ------------------ | ------------------------------------------------- |
| Płynność    | Wysoka             | Niska                                             |
| Spread      | Niski              | Szeroki                                           |
| Wolumen     | Duży               | Mały                                              |
| Zmienność   | Normalna           | Może być bardzo wysoka                            |
| Typy zleceń | Wszystkie          | Zazwyczaj tylko zlecenia z limitem (limit orders) |
| Uczestnicy  | Wszyscy inwestorzy | Głównie instytucje i aktywni traderzy             |

### Zalety handlu w pre/after-market

- **Reakcja na wyniki finansowe** — spółki często publikują wyniki kwartalne po zamknięciu sesji lub przed jej otwarciem. Pre/after-market pozwala zareagować natychmiast, zamiast czekać na otwarcie
- **Reakcja na wydarzenia globalne** — ważne wiadomości (geopolityka, dane makro z Europy/Azji) pojawiają się poza godzinami regularnej sesji
- **Lepsza cena wejścia** — czasem można kupić/sprzedać po korzystniejszej cenie, zanim rynek otworzy się z luką (gap)

### Wady handlu w pre/after-market

- **Niska płynność** — mniej uczestników oznacza trudności z realizacją zleceń po pożądanej cenie
- **Szersze spready** — koszt transakcji jest wyższy
- **Większa zmienność** — pojedyncze duże zlecenie może znacząco przesunąć cenę
- **Ograniczone typy zleceń** — zazwyczaj tylko zlecenia limit (bez zleceń market)
- **Ryzyko fałszywych ruchów** — ruchy cenowe w pre/after-market nie zawsze odzwierciedlają kierunek, w którym pójdzie cena na regularnej sesji
- **Nie wszyscy brokerzy oferują dostęp** — na XTB dostęp do pre/after-market jest ograniczony do wybranych instrumentów

## Sesje rynkowe

Forex, surowce i indeksy handluje się niemal 24 h w dni robocze, ale płynność nie jest równa przez całą dobę. Rynek "wędruje" za słońcem przez cztery główne centra finansowe (godziny w czasie polskim, orientacyjnie - przesuwają się o godzinę przy zmianach czasu):

| Sesja                  | Godziny (czas polski) | Co jest aktywne                                                                |
| ---------------------- | --------------------- | ------------------------------------------------------------------------------ |
| Sydney                 | 23:00-08:00           | AUD, NZD; niska płynność                                                       |
| Tokio                  | 01:00-10:00           | JPY, indeksy azjatyckie (Nikkei)                                               |
| Londyn                 | 09:00-18:00           | EUR, GBP, złoto, ropa Brent, indeksy europejskie (DAX, FTSE)                   |
| Nowy Jork              | 14:00-23:00           | USD, akcje US, ropa (Brent i WTI), indeksy US (S&P 500, NASDAQ); dane makro US |
| **Nakładka Londyn-NY** | **14:00-17:00**       | Największa płynność i zmienność na świecie - najwęższe spready                 |

Praktyczne wnioski:

- **Najlepszy czas na handel** większością instrumentów to 14:00-17:00 - działają oba największe centra, publikowane są dane z USA (zwykle 14:30), a spready są najwęższe
- **Najgorszy czas** to 22:00-01:00 (między zamknięciem NY a otwarciem Tokio) - spready na CFD potrafią się kilkukrotnie rozszerzyć, a swap nalicza się właśnie wtedy
- **Instrument dopasuj do sesji** - DAX ma sens w godzinach europejskich, a nie w nocy; ropa Brent najbardziej "żyje" po 14:30 (i po środowym raporcie [EIA](https://www.eia.gov/) o zapasach w USA, 16:30)
- **Korelacje między rynkami** - dolar, ropa i indeksy są powiązane: silny USD zwykle ciąży surowcom wycenianym w dolarze (złoto, ropa), a Twój wynik na instrumencie w USD dodatkowo zależy od kursu USD/PLN. Dwie pozycje na skorelowanych instrumentach (np. LONG złoto i LONG srebro albo LONG ropa i SHORT USD/CAD - kanadyjski dolar rośnie razem z ropą) to często jedno ryzyko w dwóch ticketach, nie dywersyfikacja

## Płynność

### Co to jest płynność?

Płynność (liquidity) to łatwość, z jaką można kupić lub sprzedać instrument finansowy **bez znaczącego wpływu na jego cenę**.

- **Wysoka płynność** — dużo kupujących i sprzedających, wąski spread, szybka realizacja zleceń. Przykłady: EUR/USD, akcje Apple, złoto
- **Niska płynność** — mało uczestników, szeroki spread, trudności z realizacją dużych zleceń. Przykłady: akcje małych spółek na GPW, egzotyczne pary walutowe, pallad

### Konsekwencje handlu na rynku o mniejszej płynności

- **Szerszy spread** — większy koszt wejścia i wyjścia z pozycji
- **Poślizg cenowy (slippage)** — zlecenie realizowane po gorszej cenie niż oczekiwana. Chcesz kupić po 150 PLN, a zlecenie wykonuje się po 150,50 PLN
- **Trudność z zamknięciem pozycji** — w skrajnych przypadkach możesz nie znaleźć drugiej strony transakcji
- **Większa zmienność** — pojedyncze duże zlecenie może gwałtownie przesunąć cenę
- **Manipulacja ceną** — przy niskiej płynności łatwiej o „sztuczne" ruchy cenowe

### Czy mniejsza płynność zawsze oznacza większe ryzyko?

Nie zawsze, ale zazwyczaj tak. Zależy od kontekstu:

- **Większe ryzyko** — gdy handlujesz krótkoterminowo (daytrading, scalping). Slippage i szeroki spread zjedzą Twój zysk
- **Mniejsze znaczenie** — gdy inwestujesz długoterminowo w fundamentalnie dobrą spółkę. Niższa płynność oznacza gorszy spread przy wejściu/wyjściu, ale przy horyzoncie lat nie ma to dużego znaczenia
- **Szansa** — mniej płynne rynki bywają mniej efektywne, co oznacza, że ceny mogą odbiegać od wartości fundamentalnej. Cierpliwy inwestor może znaleźć okazje, których rynek jeszcze nie wycenił

### Strategie handlu na rynku o mniejszej płynności

- **Używaj zleceń z limitem (limit orders)** — nigdy zleceń market. Zlecenie limit gwarantuje, że nie kupisz/sprzedasz po gorszej cenie niż ustalona
- **Handluj w godzinach największej aktywności** — na GPW notowania ciągłe trwają 9:00-16:50 (największa aktywność tuż po otwarciu i przed zamknięciem), na rynkach US to godziny otwarcia i zamknięcia sesji
- **Zmniejsz wielkość pozycji** — duże zlecenie na mało płynnym rynku samo przesuwa cenę przeciwko Tobie
- **Dziel duże zlecenia** — zamiast jednego zlecenia na 1000 akcji, złóż 5 zleceń po 200 akcji w odstępach czasowych
- **Poszerzaj Stop Loss** — na mało płynnym rynku knoty świec są dłuższe, więc SL ustawiony zbyt blisko zostanie łatwo aktywowany
- **Unikaj handlu przy niskiej płynności** — poniedziałkowe poranki, piątkowe popołudnia, okres świąteczny, przerwy w sesji
- **Sprawdzaj arkusz zleceń (order book)** — jeśli broker udostępnia głębokość rynku (Level 2), sprawdź ile zleceń czeka na realizację po obu stronach

### Różnice między rynkiem o mniejszej a większej płynności

| Cecha             | Wysoka płynność            | Niska płynność                     |
| ----------------- | -------------------------- | ---------------------------------- |
| Spread            | Wąski (np. 0,01 USD)       | Szeroki (np. 0,50 USD)             |
| Slippage          | Minimalny                  | Może być znaczący                  |
| Realizacja zleceń | Natychmiastowa             | Może trwać dłużej                  |
| Zmienność         | Stabilniejsza              | Gwałtowne skoki                    |
| Wielkość pozycji  | Duże zlecenia bez problemu | Duże zlecenia przesuwają cenę      |
| Przykłady         | EUR/USD, S&P 500, Apple    | Małe spółki GPW, egzotyczne waluty |

---

# Część II — Przewodnik po CFD na XTB

> Przewodnik dla osoby, która ma doświadczenie w kupowaniu akcji, ale nigdy nie
> handlowała kontraktami CFD. Wszystko wyjaśnione przystępnym językiem, na
> przykładach z platformy XTB.

> **Uwaga:** Kontrakty CFD są złożonymi instrumentami i wiążą się z dużym
> ryzykiem szybkiej utraty środków pieniężnych z powodu dźwigni finansowej.
> Według danych XTB, **75% rachunków inwestorów detalicznych odnotowuje straty**
> w wyniku handlu kontraktami CFD. Upewnij się, że rozumiesz, jak działają CFD
> i czy możesz pozwolić sobie na wysokie ryzyko utraty pieniędzy.

---

## Czym jest CFD? (porównanie z akcjami)

### Akcje — to co już znasz

Kupujesz akcje np. CD Projektu na [GPW](https://www.gpw.pl/). Stajesz się współwłaścicielem spółki.
Masz prawo głosu na walnym zgromadzeniu, dostajesz dywidendy. Żeby kupić
10 akcji po 200 zł, potrzebujesz 2000 zł. Proste.

### CFD — kontrakt na różnicę kursową

CFD (_Contract for Difference_) to **umowa między Tobą a brokerem** (w tym
przypadku XTB). Nie kupujesz akcji, ropy ani złota — stawiasz na to, czy cena
**wzrośnie** czy **spadnie**. Twój zysk lub strata to różnica między ceną
otwarcia a zamknięcia pozycji.

### Kluczowe różnice na pierwszy rzut oka

| Cecha                 | Akcje (rzeczywiste)                               | CFD                                                                                                                                                               |
| --------------------- | ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Własność**          | Stajesz się właścicielem                          | Nie — to tylko kontrakt                                                                                                                                           |
| **Prawo głosu**       | Tak                                               | Nie                                                                                                                                                               |
| **Dywidendy**         | Otrzymujesz                                       | Korekta dywidendowa (dodatnia przy LONG, ujemna przy SHORT)                                                                                                       |
| **Kierunek**          | Tylko kupno (LONG)                                | Kupno (LONG) **i** sprzedaż (SHORT)                                                                                                                               |
| **Dźwignia**          | Brak — płacisz 100%                               | Tak — płacisz np. 10-50% wartości                                                                                                                                 |
| **Koszty utrzymania** | Brak (trzymasz ile chcesz)                        | Swap — opłata za każdą noc                                                                                                                                        |
| **Prowizja na XTB**   | 0% do 100 000 EUR/mies., potem 0,2% (min. 10 EUR) | Spread + ewentualnie swap                                                                                                                                         |
| **Ryzyko**            | Stracisz max tyle, ile zainwestowałeś             | Dźwignia potęguje straty — możesz stracić więcej niż depozyt pod pozycją, ale nie więcej niż saldo konta (ochrona przed ujemnym saldem dla klientów detalicznych) |

### Co to znaczy w praktyce?

Wyobraź sobie, że chcesz „zainwestować" w ropę naftową:

- **Akcje** — nie możesz kupić baryłki ropy na giełdzie tak po prostu
- **CFD** — otwierasz kontrakt na cenę ropy. Jeśli ropa kosztuje 70 USD
  i uważasz, że wzrośnie — klikasz BUY. Jeśli cena wzrośnie do 75 USD —
  zarabiasz na różnicy. Jeśli spadnie do 65 USD — tracisz.

A co jeśli uważasz, że cena **spadnie**? Przy akcjach nie zrobisz nic (no,
chyba że skomplikowana krótka sprzedaż). Przy CFD — po prostu klikasz SELL
i zarabiasz na spadkach.

---

## Słownik pojęć CFD

Zanim przejdziesz dalej, poznaj terminy, które zobaczysz na platformie xStation
(platforma handlowa XTB).

### Spread

**Spread** to różnica między ceną kupna (ASK) a ceną sprzedaży (BID).

Przykład: ropa Brent (OIL) na platformie pokazuje:

- BID: 70,00 USD (cena, po której możesz sprzedać)
- ASK: 70,03 USD (cena, po której możesz kupić)
- **Spread: 0,03 USD**

![Spread: po której cenie kupujesz, a po której sprzedajesz](assets/spread.svg)

Spread to ukryty koszt transakcji — od razu po otwarciu pozycji jesteś „na
minusie" o wartość spreadu. Im niższy spread, tym lepiej dla Ciebie.

**Analogia do akcji:** To jak różnica między ceną kupna i sprzedaży w arkuszu
zleceń na GPW — tylko że na CFD jest to główny koszt transakcji (zamiast
prowizji).

### Lot (wielkość pozycji)

**Lot** to jednostka określająca wielkość Twojej pozycji.

- Na ropie: 1 lot = 1000 baryłek. Dużo? Tak, dlatego na XTB możesz handlować
  **micro lotami** (0,01 lota = 10 baryłek)
- Na akcjach CFD: 1 lot = 1 akcja
- Na forex: 1 lot = 100 000 jednostek waluty bazowej
- W formularzu zlecenia na xStation pole "Wolumen" to właśnie liczba lotów. Minimalny wolumen to zazwyczaj **0,01 lota**, co pozwala zacząć z małymi kwotami

### Dźwignia finansowa (leverage)

Dźwignia pozwala otworzyć pozycję **większą niż Twój kapitał**.

Przykład: dźwignia **1:10** na ropie oznacza, że zamiast wpłacać 70 000 USD
za 1000 baryłek (1 lot), wpłacasz tylko **7 000 USD** jako depozyt
zabezpieczający. Ale uwaga — jeśli cena ropy spadnie o 10%, tracisz **100%**
swojego depozytu!

**Limity dźwigni na XTB** (zgodne z regulacją ESMA dla klientów detalicznych
w UE):

| Instrument                         | Maksymalna dźwignia | Depozyt |
| ---------------------------------- | ------------------- | ------- |
| Główne pary walutowe (np. EUR/USD) | 1:30                | 3,33%   |
| Pozostałe pary walutowe, złoto     | 1:20                | 5%      |
| Główne indeksy (np. S&P 500)       | 1:20                | 5%      |
| Surowce poza złotem (np. ropa)     | 1:10                | 10%     |
| Akcje CFD                          | 1:5                 | 20%     |
| Kryptowaluty                       | 1:2                 | 50%     |

**Dlaczego takie limity?** ESMA (Europejski Urząd Nadzoru Giełd i Papierów
Wartościowych) wprowadziła te ograniczenia w 2018 roku, aby chronić
inwestorów detalicznych. Przed regulacją brokerzy oferowali dźwignię nawet
1:500, co prowadziło do masowych strat. Limity dotyczą klientów detalicznych
w UE — klienci profesjonalni mogą uzyskać wyższą dźwignię, ale muszą spełnić
surowe kryteria (np. portfel powyżej 500 000 EUR, doświadczenie zawodowe
w sektorze finansowym, odpowiednia częstotliwość transakcji).

**Analogia do akcji:** Kupujesz akcje za 100% ceny. Przy CFD z dźwignią 1:5
płacisz tylko 20%. Ale pamiętaj — dźwignia działa **w obie strony**.

### Depozyt zabezpieczający (margin)

To kwota, którą musisz mieć na koncie, żeby utrzymać otwartą pozycję. Nie jest
to opłata — to „kaucja", która jest blokowana na czas trwania transakcji.

Dwa ważne poziomy:

- **Margin Call** (Margin Level ok. 100%) — ostrzeżenie, że Twój depozyt się
  kurczy. Powinieneś dokładać środki lub zamknąć część pozycji
- **Stop Out / Margin Stop** (Margin Level 50%) — XTB automatycznie zamyka
  Twoje pozycje (zaczynając od tej z największą stratą), żebyś nie stracił
  więcej niż masz na koncie

> **Margin Level** = Equity / Used Margin × 100% — wskaźnik „zdrowia" konta.
> Dla bezpieczeństwa warto utrzymywać go znacznie powyżej progów (np. 200–500%).

**Jak działa Margin Stop w praktyce?**

Gdy poziom depozytu zabezpieczającego spadnie do 50%, broker zaczyna
automatycznie zamykać pozycje. Kolejność zamykania:

1. **Najpierw pozycja z największą stratą** — broker zamyka tę pozycję, która
   generuje największą niezrealizowaną stratę (największy ujemny P&L)
2. Jeśli po zamknięciu tej pozycji poziom depozytu nadal jest poniżej 50%,
   zamykana jest kolejna pozycja z największą stratą
3. Proces trwa do momentu, aż poziom depozytu wróci powyżej 50%

**Ważne:** Margin Stop chroni Cię przed ujemnym saldem, ale **nie gwarantuje**
zamknięcia po dokładnej cenie. W warunkach ekstremalnej zmienności (np. flash
crash, luka cenowa po weekendzie) cena wykonania może być gorsza niż poziom
50%. XTB oferuje ochronę przed ujemnym saldem (NBP — Negative Balance
Protection), co oznacza, że nie możesz stracić więcej niż masz na koncie.

### Swap (punkty swapowe)

**Swap** to opłata (lub przychód) za utrzymanie pozycji przez noc. Naliczany
jest codziennie ok. północy czasu platformy (zazwyczaj 22:00–23:59 GMT).

Dlaczego istnieje? Bo CFD to instrument lewarowany — broker „pożycza" Ci
pieniądze na utrzymanie pozycji. Za tę pożyczkę płacisz odsetki.

Przykład (orientacyjny, wartości zmieniają się):

- 1 lot EUR/USD, pozycja LONG: **-19,36 PLN za noc**
- 1 lot EUR/USD, pozycja SHORT: **+0,39 PLN za noc**

Swap może być ujemny (płacisz) lub dodatni (dostajesz) — zależy od
instrumentu i kierunku pozycji.

**Ważne:** W środę swapy są naliczane **potrójnie** (za sobotę i niedzielę).

**Dlaczego akurat w środę?** Rozliczenie transakcji na rynku walutowym (Forex)
odbywa się w cyklu T+2 (dwa dni robocze po zawarciu transakcji). Pozycja
otwarta w środę rozlicza się w piątek, a pozycja „przetrzymana" przez noc
ze środy na czwartek rozlicza się w poniedziałek — czyli obejmuje sobotę
i niedzielę. Stąd potrójny swap.

**Czy u każdego brokera jest tak samo?** Zasada potrójnego swapu w środę
dotyczy rynku Forex i jest standardem branżowym wynikającym z cyklu
rozliczeniowego T+2. Jednak dla innych instrumentów (np. akcji CFD, indeksów,
surowców) dzień naliczania potrójnego swapu **może się różnić** w zależności
od brokera — niektórzy naliczają go w piątek zamiast w środę. Zawsze
sprawdzaj specyfikację instrumentu u swojego brokera.

**Analogia do akcji:** Trzymając akcje, nie płacisz za ich przechowywanie
(no, może prowizja za przechowywanie u niektórych brokerów). Przy CFD za każdą
noc płacisz. Dlatego CFD to instrument **krótkoterminowy**, nie do trzymania
miesiącami.

### Przewalutowanie

Jeśli Twój rachunek jest w PLN, a instrument rozlicza się w USD (ropa, AAPL.US)
albo EUR, wynik każdej zamkniętej transakcji jest przeliczany na PLN. XTB
dolicza do kursu wymiany **marżę 0,5%** (tabela opłat i prowizji, stan na
maj 2026) - i to samo dotyczy zakupu prawdziwych akcji lub ETF-ów w obcej
walucie.

Dlaczego to ważne: 0,5% od wyniku brzmi niewinnie, ale przy częstym handlu
sumuje się do kosztu porównywalnego ze spreadem. Przykład: zysk 500 USD na
ropie to ok. 2,50 USD marży przewalutowania - przy 20 takich transakcjach
w miesiącu oddajesz 50 USD samego kosztu wymiany.

Jak ograniczyć: rachunek w walucie instrumentu (XTB pozwala prowadzić
subkonta w USD/EUR), handel instrumentami w PLN (KGHM.PL) albo po prostu
rzadsze, większe transakcje zamiast wielu małych.

### Pozycja LONG i SHORT

- **LONG (kupno)** — stawiasz na wzrost ceny. Kupujesz tanio, sprzedajesz
  drogo. Dokładnie jak z akcjami.
- **SHORT (sprzedaż)** — stawiasz na spadek ceny. „Sprzedajesz" drogo,
  „odkupujesz" tanio. To coś, czego nie masz przy zwykłych akcjach.

### Typy zleceń

Na xStation możesz otworzyć pozycję od razu (po cenie rynkowej) albo zostawić
zlecenie oczekujące, które aktywuje się dopiero przy określonej cenie.

| Typ zlecenia      | Kiedy się wykonuje                                                   | Do czego służy                                                         |
| ----------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Market**        | Natychmiast, po aktualnej cenie Bid/Ask                              | Wejście "teraz"; pewność wykonania, brak pewności ceny (poślizg)       |
| **Buy Limit**     | Gdy cena **spadnie** do zadanego poziomu                             | Kupno taniej niż obecnie, np. na wsparciu                              |
| **Sell Limit**    | Gdy cena **wzrośnie** do zadanego poziomu                            | Sprzedaż drożej niż obecnie, np. na oporze                             |
| **Buy Stop**      | Gdy cena **wzrośnie** do zadanego poziomu                            | Wejście w wybicie w górę (kupujesz drożej, ale z potwierdzeniem ruchu) |
| **Sell Stop**     | Gdy cena **spadnie** do zadanego poziomu                             | Wejście w wybicie w dół                                                |
| **Trailing Stop** | SL podąża za ceną w stałej odległości, cofa się tylko w jedną stronę | Automatyczne "gonienie" trendu bez ręcznego przesuwania SL             |

Jak to się ma do SL i TP: **Stop Loss** to technicznie zlecenie stop (po
aktywacji staje się zleceniem market i wykonuje się po najlepszej dostępnej
cenie), a **Take Profit** to zlecenie limit (wykonuje się po zadanej cenie lub
lepszej). Stąd asymetria: TP nie da się wykonać gorzej niż ustawiłeś, a SL przy
luce cenowej - owszem.

Zasada praktyczna: na płynnym rynku w spokojnych godzinach zlecenie market jest
w porządku. Przy niskiej płynności, w pre/after-market albo tuż po publikacji
danych makro - używaj zleceń oczekujących z limitem, inaczej płacisz poślizgiem.

### Stop Loss (SL)

Automatyczne zlecenie zamknięcia pozycji, gdy strata osiągnie ustalony poziom.

Przykład: kupujesz CFD na ropę po 70 USD. Ustawiasz Stop Loss na 68 USD.
Jeśli cena spadnie do 68 USD — pozycja zostanie automatycznie zamknięta, a Ty
stracisz 2 USD na baryłce zamiast ryzykować dalsze spadki.

**Na co zwracać uwagę przy ustawianiu Stop Loss:**

- **Nie ustawiaj SL zbyt blisko ceny wejścia** — naturalne wahania rynku
  (szum cenowy) mogą „wyrzucić" Cię z pozycji, zanim ruch pójdzie w Twoją
  stronę. Daj pozycji przestrzeń do oddychania
- **Nie ustawiaj SL na okrągłych poziomach** (np. dokładnie 100,00 USD) —
  tam skupia się wiele zleceń, co zwiększa ryzyko „polowania na stop lossy"
  przez dużych graczy
- **Uwzględnij zmienność instrumentu** — na ropie (ATR np. 2 USD dziennie)
  SL o 0,50 USD od ceny wejścia to za mało. Używaj wskaźnika ATR (Average
  True Range) do określenia sensownej odległości SL
- **Zasada 1-2%** — ryzykuj max 1-2% całego kapitału na jedną transakcję.
  Najpierw ustal, ile możesz stracić, a potem dobierz wolumen
- **SL nie jest gwarancją ceny wykonania** — w warunkach luki cenowej (gap)
  zlecenie może zostać zrealizowane po gorszej cenie niż ustawiony poziom.
  Dotyczy to szczególnie otwarcia rynku po weekendzie lub po ważnych
  wydarzeniach

**Analogia do akcji:** Identycznie jak zlecenie stop na GPW — po prostu na CFD
jest to jeszcze ważniejsze ze względu na dźwignię.

### Wielkość pozycji (position sizing)

Zasada "ryzykuj 1-2% kapitału" nic nie daje, dopóki nie przeliczysz jej na
wolumen. Kolejność jest zawsze taka sama: **najpierw poziom SL, potem wielkość
pozycji** - nigdy odwrotnie. SL stawiasz tam, gdzie Twój scenariusz przestaje
mieć sens, a kwotę ryzyka regulujesz wolumenem, nie przysuwaniem stopa.

```
wolumen (loty) = (kapitał × ryzyko %) / (odległość SL × wartość 1 jednostki ceny na 1 lot)
```

Przykłady:

| Instrument  | Kapitał    | Ryzyko 1% | Wejście | SL     | Odległość SL | 1 lot to       | Wolumen                  |
| ----------- | ---------- | --------- | ------- | ------ | ------------ | -------------- | ------------------------ |
| OIL (Brent) | 10 000 USD | 100 USD   | 70      | 68     | 2 USD        | 1 000 baryłek  | 100 / (2 × 1 000) = 0,05 |
| EUR/USD     | 5 000 USD  | 50 USD    | 1,1000  | 1,0975 | 25 pipsów    | 10 USD za pips | 50 / (25 × 10) = 0,2     |
| AAPL.US     | 5 000 USD  | 50 USD    | 200     | 210    | 10 USD       | 1 akcja        | 50 / (10 × 1) = 5        |

Dwie rzeczy, które warto zauważyć:

- **Dźwignia nie występuje we wzorze.** Dźwignia decyduje o tym, ile depozytu
  zablokuje broker, a nie o tym, ile możesz stracić. Ryzyko to odległość SL
  razy wolumen - i tyle
- **Szerszy SL = mniejsza pozycja, nie większa strata.** Jeśli ATR każe
  odsunąć SL na ropie z 2 USD na 4 USD, wolumen spada z 0,05 do 0,025 lota,
  a ryzyko dalej wynosi 100 USD

### Take Profit (TP)

Automatyczne zlecenie zamknięcia pozycji, gdy zysk osiągnie ustalony poziom.

Przykład: kupujesz CFD na ropę po 70 USD. Ustawiasz Take Profit na 75 USD.
Gdy cena dotrze do 75 USD — pozycja się zamknie i zysk zostanie zrealizowany.

**Na co zwracać uwagę przy ustawianiu Take Profit:**

- **Stosunek zysku do ryzyka (R:R)** — TP powinien być co najmniej 2× dalej
  od ceny wejścia niż SL. Jeśli ryzykujesz 2 USD (SL), celuj w minimum
  4 USD zysku (TP). Popularne proporcje to 1:2 lub 1:3
- **Ustawiaj TP na poziomach technicznych** — wsparcia, opory, poziomy
  Fibonacciego, poprzednie szczyty/dołki. Te poziomy mają znaczenie, bo
  wielu traderów na nie patrzy
- **Nie ustawiaj TP zbyt daleko** — nierealistycznie wysoki TP sprawia, że
  rzadko zostaje osiągnięty, a zysk „ucieka", gdy cena się cofa
- **Rozważ częściowe zamykanie** — zamknij np. 50% pozycji na pierwszym
  poziomie TP, a resztę zostaw z przesuniętym SL na poziom wejścia
  (breakeven). Dzięki temu realizujesz część zysku i dajesz reszcie szansę
  na większy ruch
- **Uwzględnij koszty** — spread i swap muszą być pokryte przez Twój TP.
  Jeśli spread wynosi 0,03 USD, a Twój TP to 0,05 USD od ceny wejścia —
  to za mało

### Rolowanie (rollover)

Dotyczy głównie surowców i indeksów. Kontrakty terminowe (futures), na których
bazują CFD, mają datę wygaśnięcia (np. co miesiąc). Gdy kontrakt wygasa, XTB
automatycznie „przerzuca" Twoją pozycję na nową serię kontraktu.

**Jak technicznie przebiega rolowanie?**

1. Broker zamyka Twoją pozycję na wygasającym kontrakcie (np. ropa czerwiec)
   po cenie zamknięcia tego kontraktu
2. Jednocześnie otwiera nową pozycję na kolejnym kontrakcie (np. ropa lipiec)
   po cenie otwarcia nowego kontraktu
3. Różnica cenowa między kontraktami jest kompensowana **korektą na rachunku**
   — jeśli nowy kontrakt jest droższy (contango), dostajesz korektę dodatnią
   (przy LONG) lub ujemną (przy SHORT). Przy backwardation odwrotnie
4. Matematycznie Twój wynik transakcji się nie zmienia — korekta wyrównuje
   różnicę

**Rolowanie jest bezkosztowe** — ewentualna różnica cenowa między starą a nową
serią jest kompensowana korektą na Twoim rachunku.

![Rolowanie CFD: skok ceny i korekta na rachunku](assets/rollover.svg)

**Dlaczego korekta „chwilowo" wpływa na depozyt?**

Korekta przy rolowaniu jest naliczana jako osobna pozycja na rachunku.
Nowy kontrakt może mieć **inną cenę**, a co za tym idzie — **inną wartość
pozycji** i **inny wymagany depozyt zabezpieczający**. Jeśli nowy kontrakt
jest znacząco droższy (contango), wymagany depozyt rośnie, co chwilowo obniża
poziom wolnych środków. Efekt ten jest „chwilowy", bo korekta rachunkowa
kompensuje różnicę cenową — ale sam depozyt zabezpieczający bazuje na
bieżącej cenie instrumentu, a ta się zmieniła.

**Co wpływa na wartość korekty przy rolowaniu?**

Głównym czynnikiem jest **różnica cen między wygasającym a nowym kontraktem
futures**. Ta różnica wynika z:

- **Kosztów przechowywania** (carry costs) — magazynowanie, ubezpieczenie
  towaru (dotyczy surowców fizycznych jak ropa, złoto)
- **Stóp procentowych** — koszt finansowania pozycji do daty wygaśnięcia
- **Oczekiwań rynkowych** — jeśli rynek spodziewa się wzrostu/spadku cen,
  wpływa to na cenę przyszłych kontraktów
- **Sezonowości** — np. ceny gazu naturalnego w kontraktach zimowych są
  wyższe niż w letnich
- **Podaży i popytu** na konkretne serie kontraktów

Nie jest to więc po prostu „różnica między ceną zamknięcia a ceną otwarcia
pozycji" — to różnica między cenami dwóch różnych kontraktów futures,
wynikająca z powyższych czynników.

**Czy istnieje strategia „gry na rolowanie"?**

Tak, niektórzy traderzy próbują wykorzystać przewidywalną strukturę
contango/backwardation:

- **Gra na contango (np. ropa)** — gdy rynek jest w silnym contango (futures
  droższe niż spot), traderzy otwierają pozycje SHORT na kontrakcie
  futures, licząc na to, że cena futures będzie spadać w kierunku ceny spot
  w miarę zbliżania się daty wygaśnięcia (tzw. roll yield). Jest to jednak
  **ryzykowne**, bo cena spot też się zmienia
- **Gra na backwardation** — odwrotnie, pozycja LONG w backwardation może
  przynosić dodatkowy zysk z roll yield
- **Uwaga:** Na CFD strategia ta jest trudniejsza do zastosowania, bo broker
  automatycznie kompensuje różnicę korektą. Gra na rolowanie ma większy
  sens na rynku futures (bezpośrednim), gdzie trader sam decyduje kiedy
  zamknąć stary i otworzyć nowy kontrakt

**Jak sprawdzić, jakie kontrakty są porównywane przy rolowaniu?**

Gdy wiesz, że rolowanie na danym instrumencie nastąpi w konkretnym dniu
(np. 16 kwietnia na ropie Brent / OIL), musisz sprawdzić, z jakiego
kontraktu futures na jaki broker przechodzi. Krok po kroku:

1. **Sprawdź kalendarz rolowań u brokera** — na XTB dostępny jest w zakładce
   „Informacje o instrumencie" przy danym tickerze (np. OIL). Znajdziesz tam
   datę najbliższego rolowania oraz nazwy kontraktów (np. „czerwiec 2026"
   → „lipiec 2026")

2. **Zidentyfikuj kontrakty na giełdzie bazowej** — ropa Brent jest notowana
   na giełdzie [ICE](https://www.ice.com/) (Intercontinental Exchange). Kontrakty futures mają
   oznaczenia składające się z symbolu instrumentu + kodu miesiąca + roku:

   | Kod miesiąca | Miesiąc     |
   | ------------ | ----------- |
   | F            | styczeń     |
   | G            | luty        |
   | H            | marzec      |
   | J            | kwiecień    |
   | K            | maj         |
   | M            | czerwiec    |
   | N            | lipiec      |
   | Q            | sierpień    |
   | U            | wrzesień    |
   | V            | październik |
   | X            | listopad    |
   | Z            | grudzień    |

   Przykład: jeśli rolowanie 16 kwietnia dotyczy przejścia z kontraktu
   czerwcowego na lipcowy 2026, porównujesz kontrakty **BRN M26**
   (Brent czerwiec 2026) i **BRN N26** (Brent lipiec 2026)

3. **Sprawdź ceny obu kontraktów** — możesz to zrobić na stronach takich jak:
   - [ICE](https://www.ice.com/products/219/Brent-Crude-Futures) — oficjalne notowania kontraktów Brent
   - [Investing.com](https://www.investing.com/commodities/brent-oil) — sekcja „Futures" → „Brent Oil"
   - [TradingView](https://www.tradingview.com/) — wpisz symbole kontraktów (np. `BRN1!` dla najbliższego,
     `BRN2!` dla kolejnego)

4. **Oblicz różnicę** — jeśli BRN M26 = 72,50 USD, a BRN N26 = 73,10 USD,
   różnica wynosi 0,60 USD (contango). To właśnie ta kwota zostanie
   rozliczona jako korekta na Twoim rachunku przy rolowaniu

**Wskazówka:** Na XTB możesz też po prostu sprawdzić korektę po fakcie —
po rolowaniu w historii rachunku pojawi się pozycja „Korekta rolowania"
z dokładną kwotą. Ale jeśli chcesz **wiedzieć z wyprzedzeniem**, ile wyniesie
korekta — porównaj ceny dwóch kolejnych kontraktów futures na giełdzie bazowej

---

## Przykład 1: CFD na ropę naftową (OIL)

### O instrumencie

Na XTB dostępne są dwa rodzaje ropy:

- **OIL** — ropa Brent (z Morza Północnego), benchmark dla rynków
  europejskich i światowych; tego instrumentu dotyczą wszystkie przykłady
  w tym przewodniku
- **OIL.WTI** — ropa WTI (West Texas Intermediate), benchmark dla rynku
  amerykańskiego

Cena OIL bazuje na notowaniach kontraktu futures na ropę Brent z giełdy
[ICE Futures Europe](https://www.ice.com/futures-europe) w Londynie. Obie ropy poruszają się zwykle razem, ale
Brent bywa o kilka dolarów droższa (koszt transportu i różnice w jakości).

### Krok po kroku — jak otworzyć pozycję

Załóżmy, że ropa kosztuje **70 USD za baryłkę** i uważasz, że cena wzrośnie.

1. **Wybierasz instrument:** wpisujesz „OIL" w wyszukiwarkę na xStation
2. **Decydujesz o wolumenie:** np. 0,1 lota = 100 baryłek
3. **Wartość pozycji:** 100 × 70 USD = **7 000 USD**
4. **Wymagany depozyt:** dźwignia 1:10, więc 7 000 / 10 = **700 USD**
5. **Ustawiasz SL/TP:** np. Stop Loss na 68 USD, Take Profit na 75 USD
6. **Klikasz BUY**

### Co się dzieje dalej?

| Scenariusz         | Cena ropy             | Twój wynik           | Przy depozycie 700 USD |
| ------------------ | --------------------- | -------------------- | ---------------------- |
| Cena rośnie do TP  | 75 USD (+5 USD)       | +500 USD (100 × 5)   | +71% zysku             |
| Cena spada do SL   | 68 USD (-2 USD)       | -200 USD (100 × 2)   | -29% straty            |
| Bez SL, cena spada | 66,50 USD (-3,50 USD) | -350 USD (100 × 3,5) | -50% - Margin Stop!    |

**Skąd 66,50 USD, a nie 63 USD?** Częsty błąd w rozumieniu dźwigni: nie musisz
stracić całego depozytu, żeby broker zamknął pozycję. Jeśli na koncie masz
tylko te 700 USD, Margin Stop (Margin Level 50%) uruchamia się, gdy equity
spadnie do 350 USD - czyli przy stracie 350 USD, co na 100 baryłkach daje
3,50 USD spadku ceny. Z większym saldem próg odsuwa się dalej: przy 1 400 USD
na koncie stop out wypada przy stracie 1 050 USD (cena 59,50 USD). Dlatego
Stop Loss z kroku 5 jest ważny - to Ty decydujesz, gdzie kończy się strata,
a nie mechanizm brokera.

![Margin Stop: poziomy ceny i equity na koncie](assets/margin-stop.svg)

### Specyfika ropy

- **Dźwignia:** 1:10 (depozyt 10%)
- **Spread:** zmienny, typowo ok. 0,03-0,04 USD
- **Swap:** naliczany codziennie (i potrójnie w środę)
- **Rolowanie:** co miesiąc — XTB robi to automatycznie
- **Godziny handlu:** prawie 24h w dni robocze (z przerwą na rozliczenie)
- **Waluta rozliczenia:** USD (kurs walutowy ma znaczenie!)
- **Zmienność:** duża — ceny ropy mogą się gwałtownie zmieniać pod wpływem
  geopolityki, decyzji [OPEC](https://www.opec.org/), zapasów surowca

### Na co uważać?

- Ropa jest **bardzo zmienna** — w kwietniu 2020 Brent spadła do ok. 16 USD
  za baryłkę (najniżej od 1999 roku), a amerykańska WTI na jeden dzień
  poniżej zera (-37 USD), bo kończące się kontrakty nie miały gdzie odebrać
  fizycznej dostawy
- Rolowanie jest automatyczne, ale przy dużych różnicach cen między seriami
  kontraktów może wpłynąć na Twój depozyt
- Swapy na ropie mogą być znaczące — to nie jest instrument do trzymania
  tygodniami

---

## Przykład 2: CFD na spółkę amerykańską (np. AAPL.US)

### O instrumencie

Na XTB akcje Apple są dostępne jako CFD pod tickerem **AAPL.US**. Zauważ, że
XTB oferuje też **prawdziwe akcje** Apple (bez dźwigni, 0% prowizji do
100 000 EUR/mies.) — to inna rzecz niż CFD!

### Kiedy wybrać CFD zamiast prawdziwych akcji?

- Chcesz zagrać **na spadki** (SHORT)
- Chcesz użyć **dźwigni** (masz mniej kapitału)
- Chcesz otworzyć pozycję **na krótki czas** (daytrading, kilka dni)

### Krok po kroku

Załóżmy, że akcja Apple kosztuje **200 USD** i spodziewasz się spadku po
słabych wynikach kwartalnych.

1. **Wybierasz:** AAPL.US (CFD)
2. **Wolumen:** 10 lotów = 10 akcji
3. **Wartość pozycji:** 10 × 200 = **2 000 USD**
4. **Depozyt:** dźwignia 1:5, więc 2 000 / 5 = **400 USD**
5. **Kierunek:** SELL (SHORT — stawiasz na spadek)
6. **SL:** 210 USD, **TP:** 180 USD

### Co się dzieje?

| Scenariusz          | Cena AAPL         | Twój wynik         |
| ------------------- | ----------------- | ------------------ |
| Cena spada (dobrze) | 180 USD (-20 USD) | +200 USD (10 × 20) |
| Cena rośnie (źle)   | 210 USD (+10 USD) | -100 USD (10 × 10) |

### Specyfika akcji amerykańskich CFD

- **Dźwignia:** 1:5 (depozyt 20%)
- **Spread:** zależy od płynności akcji — duże spółki (Apple, Tesla, Amazon)
  mają niski spread
- **Swap:** naliczany codziennie — trzymanie pozycji SHORT na Apple przez
  miesiąc będzie kosztowało
- **Dywidendy:** jeśli spółka wypłaca dywidendę i masz otwartą pozycję:
  - LONG → otrzymasz korektę dywidendową (dodatnią)
  - SHORT → zostanie Ci odjęta korekta dywidendowa (ujemna)
- **Godziny handlu:** godziny otwarcia giełdy NYSE/NASDAQ (15:30-22:00 czasu
  polskiego, z możliwym pre/after-market)
- **Waluta:** USD — kurs dolara wpływa na Twój wynik w PLN
- **Brak prawa głosu** — to CFD, nie jesteś akcjonariuszem

### Różnica vs. prawdziwe akcje Apple na XTB

| Cecha        | Akcje AAPL.US    | CFD AAPL.US  |
| ------------ | ---------------- | ------------ |
| Własność     | Tak              | Nie          |
| Dźwignia     | Brak             | 1:5          |
| SHORT        | Nie              | Tak          |
| Prowizja     | 0% (do 100k EUR) | Spread       |
| Swap         | Brak             | Codziennie   |
| Dywidenda    | Pełna            | Korekta      |
| Do trzymania | Miesiące/lata    | Dni/tygodnie |

---

## Przykład 3: CFD na spółkę polską (np. KGHM.PL)

### O instrumencie

Na XTB akcje KGHM są dostępne jako CFD pod tickerem **KGHM.PL**. Podobnie jak
przy akcjach US, XTB oferuje też prawdziwe akcje KGHM (0% prowizji do
100 000 EUR/mies.).

### Ważne: oferta CFD na polskie akcje jest ograniczona

Na XTB dostępnych jest ok. **39 polskich spółek jako CFD** (vs **709 polskich
spółek jako akcje rzeczywiste**). CFD są dostępne tylko na największe
i najpłynniejsze spółki z GPW — czyli głównie WIG20 i mWIG40.

### Krok po kroku

Załóżmy, że KGHM kosztuje **150 PLN** i uważasz, że cena wzrośnie po dobrych
danych o cenach miedzi.

1. **Wybierasz:** KGHM.PL (CFD)
2. **Wolumen:** 20 lotów = 20 akcji
3. **Wartość pozycji:** 20 × 150 = **3 000 PLN**
4. **Depozyt:** dźwignia 1:5, więc 3 000 / 5 = **600 PLN**
5. **Kierunek:** BUY (LONG)
6. **SL:** 140 PLN, **TP:** 170 PLN

### Specyfika akcji polskich CFD

- **Dźwignia:** 1:5 (depozyt 20%) — taka sama jak dla akcji US
- **Spread:** może być **wyższy** niż na akcjach US, bo polskie spółki mają
  mniejszą płynność
- **Swap:** naliczany codziennie
- **Godziny handlu:** godziny sesji GPW — notowania ciągłe 9:00-16:50 (faza przed otwarciem 8:30-9:00, fixing otwarcia 9:00, fixing zamknięcia 17:00, dogrywka 17:00-17:05)
- **Waluta:** PLN — brak ryzyka walutowego (w odróżnieniu od akcji US!)
- **Liczba dostępnych spółek:** ograniczona do ~39 najpłynniejszych
- **Dywidendy:** korekta dywidendowa, tak jak przy akcjach US CFD

### Różnica vs. prawdziwe akcje KGHM na XTB

| Cecha           | Akcje KGHM.PL    | CFD KGHM.PL |
| --------------- | ---------------- | ----------- |
| Własność        | Tak              | Nie         |
| Dźwignia        | Brak             | 1:5         |
| SHORT           | Nie              | Tak         |
| Prowizja        | 0% (do 100k EUR) | Spread      |
| Waluta          | PLN              | PLN         |
| Dostępne spółki | 709              | ~39         |

---

## Porównanie: ropa vs spółka US vs spółka PL

### Tabela porównawcza

| Cecha                               | Ropa Brent (OIL)     | Akcja US (AAPL.US)  | Akcja PL (KGHM.PL)    |
| ----------------------------------- | -------------------- | ------------------- | --------------------- |
| **Typ instrumentu**                 | Surowiec             | Akcja CFD           | Akcja CFD             |
| **Dźwignia**                        | 1:10                 | 1:5                 | 1:5                   |
| **Depozyt**                         | 10%                  | 20%                 | 20%                   |
| **Waluta**                          | USD                  | USD                 | PLN                   |
| **Ryzyko walutowe**                 | Tak (USD/PLN)        | Tak (USD/PLN)       | Nie                   |
| **Przewalutowanie (rachunek PLN)**  | 0,5% od wyniku       | 0,5% od wyniku      | Brak                  |
| **Spread**                          | Niski (płynny rynek) | Niski (duże spółki) | Wyższy (mniej płynny) |
| **Swap**                            | Tak                  | Tak                 | Tak                   |
| **Rolowanie**                       | Tak (co miesiąc)     | Nie                 | Nie                   |
| **Dywidendy**                       | Nie dotyczy          | Korekta             | Korekta               |
| **Godziny handlu**                  | ~24h (pon-pt)        | 15:30-22:00 CET     | 9:00-16:50 CET        |
| **Zmienność**                       | Bardzo wysoka        | Wysoka              | Średnia/wysoka        |
| **Dostępność SHORT**                | Tak                  | Tak                 | Tak                   |
| **Odpowiednik „prawdziwych" akcji** | Nie istnieje         | Tak (0% prowizji)   | Tak (0% prowizji)     |

### Kluczowe wnioski

1. **Dźwignia na surowcach jest większa (1:10) niż na akcjach (1:5)** — możesz
   kontrolować większą pozycję mniejszym depozytem, ale ryzyko też jest większe

2. **Ryzyko walutowe** — przy ropie i akcjach US Twój wynik w PLN zależy nie
   tylko od ceny instrumentu, ale też od kursu USD/PLN. Przy polskich akcjach
   CFD tego problemu nie ma

3. **Rolowanie dotyczy tylko surowców** — akcje CFD nie wygasają, nie musisz
   się martwić o rolowanie

4. **Płynność i spread** — ropa i duże spółki US mają niskie spready. Polskie
   spółki mogą mieć wyższe spready, szczególnie mniejsze

5. **Godziny handlu** — ropa handluje prawie 24h, co daje elastyczność.
   Polskie akcje tylko w godzinach GPW

6. **Jeśli chcesz trzymać długo — kup prawdziwe akcje, nie CFD.** CFD jest
   do krótkoterminowej spekulacji. Swapy zjedzą Twój zysk przy długim
   trzymaniu

---

## Najczęstsze błędy początkujących

### 1. Ignorowanie dźwigni

„Mam 1000 zł, otworzę pozycję za 5000 zł — w końcu mogę!"

Tak, **możesz**, ale spadek ceny o 20% to strata **100% Twojego kapitału** -
a w praktyce broker zamknie pozycję jeszcze wcześniej: przy Margin Level 50%
wystarczy spadek o 10%, żeby uruchomił się Margin Stop. Dźwignia to miecz
obosieczny.

**Zasada:** Na początek używaj małej dźwigni. Otwieraj pozycje za ułamek
dostępnego depozytu.

### 2. Brak Stop Loss

Przy akcjach możesz „przeczekać" spadki — w końcu spółka może odrobić straty.
Przy CFD z dźwignią **nie masz tego luksusu**. Bez SL możesz stracić cały
depozyt, zanim cena się odbije.

**Zasada:** Zawsze ustawiaj Stop Loss. Zawsze.

### 3. Trzymanie CFD jak akcji

„Kupię CFD na Apple i potrzymam rok."

Po roku swapy mogą zjeść znaczną część Twojego zysku. CFD to instrument
do spekulacji krótkoterminowej (minuty, godziny, dni — max tygodnie).

### 4. Ignorowanie kosztów (spread + swap)

Spread płacisz przy otwarciu. Swap co noc. Przy małych ruchach cenowych te
koszty mogą sprawić, że nawet „dobra" transakcja kończy się stratą.

### 5. Overtrading

**Co to jest overtrading?** Overtrading to nadmierne handlowanie — otwieranie
zbyt wielu pozycji, zbyt często, bez solidnych podstaw analitycznych. To jeden
z najczęstszych powodów strat wśród początkujących traderów.

**Przyczyny overtradingu:**

- **Chęć odrobienia strat** (revenge trading) — po stracie chcesz „szybko
  odzyskać" pieniądze i otwierasz kolejne pozycje bez analizy
- **FOMO** (Fear of Missing Out) — strach przed przegapieniem okazji. Każdy
  ruch cenowy wydaje się szansą
- **Nuda** — siedzisz przed ekranem i czujesz, że „musisz coś robić"
- **Adrenalina** — handel daje emocjonalny „kop", uzależniający jak hazard
- **Brak planu** — bez jasnych kryteriów wejścia/wyjścia każda sytuacja
  wygląda jak okazja
- **Zbyt łatwy dostęp** — aplikacja na telefonie, jeden klik = transakcja

**Konsekwencje overtradingu:**

- **Koszty transakcyjne** — każda transakcja to spread + ewentualny swap.
  20 transakcji dziennie przy spreadzie 0,03 USD na ropie to 0,60 USD
  na baryłkę „stracone" na samych kosztach
- **Gorsze decyzje** — zmęczenie decyzyjne prowadzi do coraz gorszej jakości
  analiz
- **Wypalenie emocjonalne** — ciągły stres i wahania emocji
- **Spirala strat** — straty prowadzą do revenge tradingu, który prowadzi do
  kolejnych strat

**Różnica między overtradingiem a regularnym handlem:**

| Cecha            | Regularny handel                               | Overtrading                             |
| ---------------- | ---------------------------------------------- | --------------------------------------- |
| Częstotliwość    | Kilka transakcji dziennie/tygodniowo           | Dziesiątki transakcji dziennie          |
| Podstawa decyzji | Analiza techniczna/fundamentalna               | Emocje, przeczucia, FOMO                |
| Plan             | Jasny SL, TP, uzasadnienie                     | Brak lub ignorowanie planu              |
| Emocje           | Kontrolowane                                   | Dominują (strach, chciwość, frustracja) |
| Wyniki           | Konsekwentne (nawet jeśli nie zawsze zyskowne) | Chaotyczne, narastające straty          |

**Jak unikać overtradingu:**

- **Ustal dzienny limit transakcji** — np. max 3-5 transakcji dziennie.
  Po osiągnięciu limitu zamknij platformę
- **Ustal dzienny limit straty** — np. max 2-3% kapitału dziennie. Po
  osiągnięciu limitu — stop na resztę dnia
- **Prowadź dziennik transakcji** — zapisuj każdą transakcję z uzasadnieniem.
  Jeśli nie potrafisz napisać powodu wejścia — nie wchodź
- **Handel tylko w określonych godzinach** — np. tylko podczas sesji
  europejskiej (09:00-17:00)
- **Odchodź od ekranu** — po zamknięciu pozycji zrób przerwę. Nie szukaj
  od razu kolejnej okazji
- **Trzymaj się planu** — jeśli Twoja strategia mówi „2 setup-y dziennie",
  nie szukaj trzeciego na siłę

### 6. Handel bez planu

Przed otwarciem pozycji powinieneś wiedzieć:

- **Dlaczego** wchodzisz? (analiza, nie „przeczucie")
- **Gdzie** ustawiasz SL? (ile jesteś gotów stracić)
- **Gdzie** ustawiasz TP? (kiedy realizujesz zysk)
- **Ile ryzykujesz?** (max 1-2% kapitału na jedną transakcję — to popularna
  zasada zarządzania ryzykiem)

### 7. Trzymanie lewarowanej pozycji przez weekend lub publikację wyników

Stop Loss chroni Cię tylko wtedy, gdy rynek "przechodzi" przez Twój poziom.
Gdy rynek jest zamknięty, a cena otwiera się z luką (gap), SL wykona się po
pierwszej dostępnej cenie za luką - nie po tej, którą ustawiłeś.

Typowe sytuacje:

- **Wyniki kwartalne** - spółki publikują je po sesji lub przed otwarciem.
  Akcja potrafi otworzyć się 10-20% niżej. Przy CFD z dźwignią 1:5 luka 20%
  to strata 100% depozytu pod pozycją, a SL ustawiony 5% niżej nic tu nie zmieni
- **Weekend** - ropa, indeksy i forex reagują w poniedziałek na wszystko, co
  wydarzyło się od piątku (OPEC, geopolityka, wybory). Luka po weekendzie to
  najczęstsza przyczyna gwałtownych Margin Stopów
- **Dane makro** (decyzje Fed, NFP, CPI) - rynek jest otwarty, ale przez kilka
  sekund płynność znika i spread rozszerza się wielokrotnie; SL wykonuje się
  z dużym poślizgiem

**Zasada:** przed wynikami spółki i przed weekendem zamknij lewarowaną pozycję
albo zmniejsz ją tak, żeby luka 20% nie zagrażała rachunkowi. Jeśli chcesz
mieć ekspozycję przez publikację, kup prawdziwe akcje (bez dźwigni) - albo
zaakceptuj, że SL jest w tym momencie tylko życzeniem. Sprawdzaj kalendarz
wyników i kalendarz makro **przed** otwarciem pozycji, nie po.

---

## Podatki od CFD i akcji (Polska)

Zysk z CFD, akcji i ETF-ów podlega **podatkowi od zysków kapitałowych 19%**
(tzw. podatek Belki). Kilka rzeczy, które trader musi wiedzieć:

### Kiedy powstaje podatek

- Podatek płacisz od **zrealizowanego** wyniku - czyli po zamknięciu pozycji.
  Otwarta pozycja z niezrealizowanym zyskiem nie jest opodatkowana
- Liczy się **łączny wynik roczny**: suma zysków i strat ze wszystkich
  transakcji zamkniętych od 1 stycznia do 31 grudnia. Zyskowne i stratne
  transakcje kompensują się
- Swapy i korekty (rolowania, dywidendowe) są częścią wyniku z instrumentu -
  trafiają do rozliczenia razem z transakcją, nie osobno

### Jak rozliczyć

| Krok | Co                                                                                                                         | Termin          |
| ---- | -------------------------------------------------------------------------------------------------------------------------- | --------------- |
| 1    | XTB (jak każdy polski dom maklerski) wysyła **PIT-8C** z sumą przychodów, kosztów i wynikiem                               | do końca lutego |
| 2    | Przepisujesz dane z PIT-8C do **PIT-38** (np. w e-Urzędzie Skarbowym, gdzie formularz jest zwykle już wstępnie wypełniony) | do 30 kwietnia  |
| 3    | Płacisz 19% od dochodu (albo wykazujesz stratę)                                                                            | do 30 kwietnia  |

Broker **nie pobiera** podatku od CFD i akcji automatycznie - rozliczenie jest
po Twojej stronie. Wyjątek: dywidendy z polskich spółek (19% potrącane u
źródła, nic nie rozliczasz).

### Strata podatkowa

- Stratę z danego roku odliczasz od zysków w **kolejnych 5 latach**, maksymalnie
  50% straty w jednym roku
- Strata z CFD kompensuje zyski z akcji, ETF-ów i futures (to samo źródło:
  kapitały pieniężne)
- Strata z **kryptowalut** to osobna kategoria - nie kompensuje się z CFD
  ani akcjami

### Waluty obce

- Wynik w USD/EUR przelicza się na PLN po **średnim kursie NBP z dnia
  poprzedzającego** zamknięcie transakcji. XTB robi to za Ciebie w PIT-8C
- U brokerów zagranicznych bez PIT-8C (np. Interactive Brokers) przeliczasz
  każdą transakcję samodzielnie - przy setkach transakcji rocznie to realny
  koszt czasu

### Dywidendy z akcji zagranicznych

- USA: podpisany **W-8BEN** (XTB prosi o niego przy rejestracji) obniża
  podatek u źródła z 30% do 15%; brakujące 4% dopłacasz w PIT-38
- **Korekta dywidendowa na CFD** to nie dywidenda - jest częścią wyniku
  z instrumentu pochodnego i nie podlega podatkowi u źródła

### Uwaga na IKE/IKZE

Na rachunkach IKE i IKZE (zwolnienie z podatku Belki) można kupować akcje
i ETF-y, ale **nie CFD**. Jeśli inwestujesz długoterminowo, to kolejny argument
za prawdziwymi akcjami zamiast kontraktów.

---

## Źródła i przydatne linki

### Oficjalne materiały XTB

- [Kontrakty CFD — podstawowe pojęcia (XTB)](https://www.xtb.com/pl/lp/kontrakty-cfd-podstawowe-pojecia)
- [Kontrakty CFD — co to jest? Na czym polega handel CFD? (XTB)](https://www.xtb.com/pl/edukacja/kontrakty-cfd)
- [CFD na akcje spółek giełdowych (XTB)](https://www.xtb.com/pl/edukacja/akcje-cfd)
- [Jak obliczyć wartość punktów swapowych (XTB)](https://www.xtb.com/pl/edukacja/jak-obliczyc-wartosc-punktow-swapowych)
- [Swapy i opłaty (XTB)](https://www.xtb.com/pl/edukacja/swapy-i-oplaty)
- [Rolowanie — wszystko co musisz wiedzieć (XTB)](https://www.xtb.com/pl/edukacja/rolowanie)
- [Rynki akcyjne i akcje CFD (XTB)](https://www.xtb.com/pl/edukacja/rynki-akcyjne)
- [Akcje CFD — GPW (XTB)](https://www.xtb.com/pl/akcje-cfd/gpw)
- [Ropa naftowa — notowania OIL (XTB)](https://www.xtb.com/int/commodities/oil)

### Inne przydatne źródła

- [Czym jest spread i jego znaczenie w handlu (Świat Inwestycji)](https://swiatinwestycji.pl/spread/)
- [CFD a akcje — co lepsze? (Poradnik Inwestora)](https://www.poradnik-inwestora.pl/cfd-vs-akcje/)
- [Punkty swapowe — jak obliczyć ich wartość (GiełdoMania)](https://gieldomania.pl/punkty-swapowe-jak-obliczyc-ich-wartosc/)
- [XTB — opinie i recenzja 2026 (Poradnik Inwestora)](https://www.poradnik-inwestora.pl/brokerzy-xtb/)

### Regulacje

- [ESMA — ograniczenia dźwigni dla klientów detalicznych](https://www.esma.europa.eu/policy-rules/mifid-ii-and-mifir/investor-protection/cfd)
- [KNF — ostrzeżenia dot. CFD](https://www.knf.gov.pl)

### Podatki

- [PIT-38 — formularz i objaśnienia (gov.pl)](https://www.gov.pl/web/finanse/pit-38)
- [e-Urząd Skarbowy (Twój e-PIT)](https://www.podatki.gov.pl/e-urzad-skarbowy/)
- [Tabela A średnich kursów NBP](https://nbp.pl/statystyka-i-sprawozdawczosc/kursy/tabela-a/)

---

> **Disclaimer:** Ten przewodnik ma charakter edukacyjny i nie stanowi porady
> inwestycyjnej. Handel kontraktami CFD wiąże się z wysokim ryzykiem straty
> kapitału. Przed rozpoczęciem handlu upewnij się, że rozumiesz wszystkie
> ryzyka i koszty. Dane i przykłady liczbowe mają charakter poglądowy
> i mogą nie odpowiadać aktualnym warunkom rynkowym.

## License

[The MIT License](https://piecioshka.mit-license.org) @ 2026
