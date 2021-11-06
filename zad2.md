## Lekcja 1 – Markdown lekki język znaczników 

## Wstęp

Obecnie powszechnie wykorzystuje się języki ze znacznikami do opisania dodatkowych informacji umieszczanych w plikach tekstowych. Z pośród najbardziej popularnych można wspomnieć o: 

1. **html**  – służącym do opisu struktury informacji zawartych na stronach internetowych,
2. **Tex** (Latex) – poznany na zajęciach język do „profesjonalnego” składania tekstów,
3. **XML** (Extensible Markup Language) - uniwersalnym języku znaczników przeznaczonym do reprezentowania różnych danych w ustrukturalizowany sposób.



W tym przypadku mamy np. znacznik np.  opisujący parametry koła i który może być właściwie zinterpretowany przez dedykowaną aplikację (np. przeglądarki www). Jako ciekawostkę można podać fakt, że również pakiet MS Office wykorzystuje format XML do przechowywania informacji o dodatkowych parametrach formatowania danych. Na przykład pliki z rozszerzeniem docx, to nic innego jak spakowane algorytmem zip katalogi z plikami xml.



Wszystkie te języki znaczników cechują się rozbudowaną i złożoną składnią i dlatego do ich edycji wymagają najczęściej dedykowanych narzędzi w postaci specjalizowanych edytorów. By wyeliminować powyższą niedogodność powstał **Markdown**  - uproszczony język znaczników służący do formatowania dokumentów tekstowych (bez konieczności używania specjalizowanych narzędzi). Dokumenty w tym formacie można bardzo łatwo konwertować do wielu innych formatów: np. html, pdf, ps (postscript), epub, xml i wiele innych. Format ten jest powszechnie używany do tworzenia plików README.md (w projektach open source) i powszechnie obsługiwany przez serwery git’a. Język ten został stworzony w 2004 r. a jego twórcami byli John Gruber i Aaron Swartz. W kolejnych latach podjęto prace w celu stworzenia standardu rozwiązania i tak w 2016 r. opublikowano dokument RFC 7764 który zawiera opis kilku odmian tegoż języka:

* CommonMark,  

* GitHub Flavored Markdown (GFM),

* Markdown Extra. 

  

## Podstawy składni

Podany link: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet zawiera opis podstawowych elementów składni w języku angielskim. Poniżej zostanie przedstawiony ich krótki opis w języku polskim

### Definiowanie nagłówków

W tym celu używamy znaków kratki: #

Lewe okno zawiera kod źródłowy – prawe -podgląd przetworzonego tekstu

### Definiowanie list

Listy numerowane definiujemy wstawiając numery kolejnych pozycji zakończone kropką

Listy nienumerowane definiujemy znakami: *,+,-

### Wyróżnianie tekstu
### Tabele

Centrowanie zawartości kolumn realizowane jest poprzez odpowiednie użycie znaku dwukropka:

### Odnośniki do zasobów

[odnośnik do zasobów](www.gazeta.pl)

 [odnośnik do pliku](LICENSE.md) 
 [odnośnik do kolejnego zasobu][1] 
[1]: http://google,com

### Obrazki

![alt text](https://server.com/images/icon48.png "Logo 1") – obrazek z zasobów
internetowych
![](logo.png) – obraz z lokalnych zasobów

### Kod źródłowy dla różnych języków programowania
### Tworzenie spisu treści na podstawie nagłówków
## Edytory dedykowane
Pracę nad dokumentami w formacie Markdown( rozszerzenie md) można wykonywać w
dowolnym edytorze tekstowym. Aczkolwiek istnieje wiele dedykowanych narzędzi:
1. Edytor Typora - https://typora.io/
2. Visual Studio Code z wtyczką „markdown preview”
## Pandoc – system do konwersji dokumentów Markdown do innych formatów
Jest oprogramowanie typu open source służące do konwertowania dokumentów pomiędzy
różnymi formatami.
Pod poniższym linkiem można obejrzeć przykłady użycia:
https://pandoc.org/demos.html
Oprogramowanie to można pobrać z spod adresu: https://pandoc.org/installing.html
Jeżeli chcemy konwertować do formatu latex i pdf trzeba doinstalować oprogramowanie
składu Latex (np. Na MS Windows najlepiej sprawdzi się Miktex - https://miktex.org/)
Gdyby podczas konwersji do formatu pdf pojawił się komunikat o niemożliwości
znalezienia programu pdflatex rozwiązaniem jest wskazanie w zmiennej środowiskowej
**PATH** miejsca jego położenia

Pod adresem (https://gitlab.com/mniewins66/templatemn.git) znajduje się przykładowy plik
Markdown z którego można wygenerować prezentację w formacie pdf wykorzystując
klasę latexa beamer.
W tym celu należy wydać polecenie z poziomu terminala:
$pandoc templateMN.md -t beamer -o prezentacja.pdf