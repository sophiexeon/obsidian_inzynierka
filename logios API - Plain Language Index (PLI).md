[[czytelność tekstu - polski]]

[![logios](https://logios.dev/wp-content/themes/logios/front/dist/static/img/logo-light.svg)](https://logios.dev)

 [API](https://logios.dev/api/)
 [O nas](https://logios.dev#o-nas)
[Kontakt](https://logios.dev/kontakt/)

# API

## **Dostęp do API**

Tworzysz narzędzia informatyczne? Prowadzisz badania języka? Teraz możesz bezpłatnie skorzystać z naszego API.

Do czego API daje Ci dostęp?

- Do indeksu prostoty języka (PLI)
- Do 10 składowych PLI
- Do ponad 40 innych cech języka

## **Dokumentacja dla programistów**

[Opis działania API (PDF](https://logios.dev/wp-content/uploads/2024/02/logios-api.pdf))

[Przykładowa realizacja](https://logios.dev/wp-content/uploads/2024/02/logios-calculate-measures-response.json)

## O indeksie prostoty języka (PLI)

### Przystępność tekstu

Przystępność (ang. _readability_) to obiektywna właściwość języka tekstu, która pozwala prognozować, w jakim stopniu czytelnik poradzi sobie z przetwarzaniem zawartych w tekście informacji. Przystępne teksty czyta się szybciej i lepiej rozumie.

Indeksy przystępności można opracowywać metodami psychologicznymi lub korpusowymi. W podejściu psychologicznym badacze opracowują formuły na podstawie badań eksperymentalnych, np. ankiet z grupą rzeczywistych czytelników. W podejściu korpusowym – badane teksty porównuje się pod względem różnych cech języka z tekstami referencyjnymi – reprezentującymi teksty łatwe oraz trudne.

### Jak powstał nasz indeks

Plain Language Index opracowaliśmy metodami korpusowymi. Zbiorem tekstów wzorcowych był korpus KINGNET2019, czyli przygotowany przez ING Bank Śląski zbiór 4000 tekstów z poczytnych serwisów internetowych. Korpus języka negatywnego (trudnego) zawierał tysiące tekstów urzędowych, prawnych, firmowych i naukowych.

PLI składa się z 10 cech stylu, które wybraliśmy z niemal 60 parametrów. Każda cecha tworząca PLI musiała spełniać 4 warunki.

Jakie?

- maksymalnie różnicować korpusy referencyjne (teksty proste vs. teksty trudne)
- nie zależeć od innych cech
- nie powtarzać informacji innych cech
- zmieniać się pod wpływem interwencji eksperta prostego języka

Analizę statystyczną wykonał dr inż. Robert Kapłon.

### Teoretyczna podstawa PLI

PLI wykorzystuje teorię mimikry w komunikacji, tzn. imituje cechy tekstów, które zwykli ludzie czytają na co dzień w czasie wolnym. Indeks ocenia w procentach podobieństwo badanego tekstu do atrakcyjnej polszczyzny. Mierzy bezwzględną prostotę tekstu, ale pozwala też oceniać postęp upraszczania.

Jest bardzo czuły na transformacje profesjonalnych upraszczaczy, jednak -w przeciwieństwie do innych indeksów – bardzo trudno nim manipulować (skracanie zdań i usuwanie trudnych słów na niewiele się zdaje :-)).

### Biznesowa podstawa PLI

PLI tworzyliśmy na zamówienie organizacji, które wprowadzają u siebie standard prostego języka.

Nasi klienci potrzebowali narzędzia, które:

- ocenia zgodność tekstu z wprowadzonym w organizacji standardem
- pozwala wyznaczać mierzalne cele dla całej organizacji i poszczególnych jednostek
- uwzględnia parametry, które wewnętrzni redaktorzy mogą kontrolować
- pokazuje wzorce polszczyzny atrakcyjnej dla ogółu społeczeństwa
- ma intuicyjną skalę: 0%-100%
- pozwala przewidywać zgodność tekstu z obydwoma standardami: prostego języka oraz języka łatwego

### 10 składowych PLI

PLI ocenia stopień, w jakim tekst realizuje normy prostego języka. Mierzy 10 cech stylu. Osiągnięcie normy przez każdą cechę oznacza przyznanie tekstowi 10 punktów procentowych. PLI ocenia teksty w języku polskim, ale algorytm można wykorzystać do zbudowania PLI dowolnego języka.

Jakie cechy stylu mierzy PLI?

#### **Dobór słów**

- **Urzędyzmy (ton formalny)** – parametr ten pokazuje, jak dużo jest w tekście wyrazów urzędowych. To one sprawiają, że styl staje się formalny i urzędowy. Urzędyzmy wskazują, czy firma ma urzędowe DNA.
- **Terminy o szyku N+A (terminy)** – parametr ten pokazuje, jak dużo jest w tekście 2-wyrazowych wyrażeń specjalistycznych o szyku: rzeczownik + przymiotnik. To one sprawiają, że tekst staje się niezrozumiały dla nieprofesjonalisty. Wysoki poziom terminów świadczy o merytorycznej trudności tekstu.
- **Wyrazy najczęstsze (TOP100)** – parametr ten oblicza, jak dużo jest w tekście słów najczęstszych (z listy frekwencyjnej 100 wyrazów). To one sprawiają, że tekst ma łatwą tematykę. To parametr ważny w tekstach adresowanych do małych dzieci i migrantów.
- **Wyrazy długie i rzadkie (trudne słowa)** – parametr ten pokazuje, jak dużo jest w tekście słów rzadkich i jednocześnie długich. Ich obecność świadczy o merytorycznej trudności tekstu.

#### **Spójność tekst**

- **Zaimkowość (zaimki)**– parametr ten mierzy w tekście odsetek zaimków. Słowa te zastępują powtarzane terminy i pojęcia, wzmacniając międzyzdaniową spójność tekstu.

#### **Budowa zdań**

- **Stosunek N/V (rzeczownikowość)**– parametr ten wskazuje, czy styl tekstu jest czasownikowy (cech pożądana) czy rzeczownikowy (cecha niepożądana). Czasowniki są informacyjnym sercem zdania, więc w tekście powinno być ich jak najwięcej. Wysoki stopień rzeczownikowości świadczy o tzw. chorobie rzeczownikowej.
- **Nienaturalna gramatyka (złe czasowniki)** – parametr ten zlicza, ile nazw czynności występuje w tekście w postaci imiesłowów, strony biernej, rzeczowników odczasownikowych i form bezosobowych. Zwykle cecha ta odpowiada za tzw. syndrom „nieśmiałego zięcia i synowej”.
- **Średnia długość zdania** **(długość zdania)**– parametr ten oblicza średnią długość zdania, czyli liczbę wyrazów w zdaniu. W atrakcyjnych tekstach nie spotykamy zbyt wielu zdań dłuższych niż 15 wyrazów. Pozwala zidentyfikować trzy typy kropek: kropkę miłosierdzia, kropkę miłości i kropkę grozy.

#### **Relacje nadawczo-odbiorcze**

- **Wykładniki nadawcy (nadawca)** – parametr ten pokazuje, jak często nadawca ujawnia w tekście swoją obecność. Mogą to być zaimki (ja, mnie, nasz) lub czasowniki (proszę, witam) pierwszej osoby. Im więcej nadawcy, tym więcej w tekście autoprezentacji..
- **Wykładniki odbiorcy** **(odbiorca)** – parametr ten pokazuje, jak często w tekście nadawca zwraca się bezpośrednio do odbiorcy. Mogą to być zaimki (Ty, Ciebie, Wasz, Pan, Pani, Państwo) lub czasowniki (prześlij, weź) drugiej osoby. Im więcej takich zwrotów, tym tekst jest bardziej perswazyjny.

Warto wiedzieć, ze interpersonalne cechy stylu pozwalają zidentyfikować typ relacyjności tekstu. Wystarczy wyliczyć stosunek nadawcy do odbiorcy, czyli bilans H2H.

---

## Bibliografia

Romanik, W., Piekot, T., & Tymiński, R. (2022). [Adaptation of informed consent for anaesthesia to plain language standard](https://journals.viamedica.pl/nowotwory_journal_of_oncology/article/download/NJO.a2022.0034/66974). _Nowotwory. Journal of Oncology_, _72_(4), 265-273.

Andrzejewska, D. (2022). [Wpływ typu relacyjności na recepcję tekstu: Wnioski z eksperymentu](https://wuwr.pl/okom/article/view/15100/13680). _Oblicza Komunikacji_, _14_(1), 9-26.

Jeśli masz pytania, napisz do nas: support@logios.dev