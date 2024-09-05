# Opis Projektu:

Projekt polega na analizie efektywności kampanii marketingowej banku, przeprowadzonej za pomocą telefonicznych kontaktów z klientami. Celem jest zrozumienie, które aspekty kampanii (np. liczba kontaktów, dni od ostatego kontaktu) mają największy wpływ na otwarcie depozytów przez klientów. W projekcie użyto narzędzi Power BI oraz funkcji DAX do wizualizacji danych i obliczenia kluczowych wskaźników skuteczności kampanii.

Użyte dane surowe obejmują następujące kolumny:

- Deposit (czy klient otworzył depozyt – tak/nie)
- Pdays (liczba dni od ostatniego kontaktu klienta z bankiem)
- Campaign (liczba kontaktów z klientem podczas bieżącej kampanii)

Dodatkowo utworzona została kolumna pomocnicza:
- Kolumna pomocnicza „Kategoria dni od ostatniego kontaktu” – stworzona w celu grupowania klientów według zakresów liczby dni od ostatniego kontaktu (Pdays), aby lepiej zrozumieć wpływ długości przerwy na otwieranie depozytów.

Na podstawie tych kolumn surowych oraz kolumny pomocniczej utworzyłem następujące miary w DAX:
- Liczba depozytów – całkowita liczba klientów, którzy otworzyli depozyt po kampanii
- Średnia liczba dni od ostatniego kontaktu dla depozytów – średnia liczba dni od ostatniego kontaktu dla klientów, którzy otworzyli depozyt
- Różnica dni od ostatniego kontaktu – różnica w liczbie dni od ostatniego kontaktu pomiędzy klientami, którzy otworzyli depozyt, a tymi, którzy tego nie zrobili
- Skuteczność kampanii (%) – procent klientów, którzy otworzyli depozyt w ramach kampanii
- Udział pozytywnych wyników (%) – procent pozytywnych odpowiedzi na kampanię

# Krok po kroku: Realizacja projektu:

### 1. Przygotowanie danych

Import danych: Dane kampanii marketingowej zostały zaimportowane do Power BI z pliku CSV, który zawierał informacje o liczbie kontaktów z klientami, czasie od ostatniego kontaktu oraz wynikach kampanii (depozytach).

Czyszczenie danych: W edytorze Power Query upewniłem się, że dane są poprawnie sformatowane i nie zawierają błędnych lub brakujących wartości. Przefiltrowałem dane, aby usunąć wiersze z brakującymi danymi w kolumnach Deposit, Pdays i Campaign.

Tworzenie kolumny pomocniczej: Utworzyłem nową kolumnę „Kategoria dni od ostatniego kontaktu” w Power BI, używając następującej formuły DAX, aby pogrupować klientów według liczby dni od ostatniego kontaktu

### 2. Tworzenie miar w DAX

Stworzyłem miary w DAX, aby dokładnie przeanalizować wyniki kampanii:

Obliczenie liczby depozytów, średniej liczby dni od ostatniego kontaktu, różnicy dni od ostatniego kontaktu, skuteczności kampanii i udziału pozytywnych wyników (szczegóły powyżej).

### 3. Tworzenie wizualizacji

Karty z kluczowymi wskaźnikami (KPI):

Utworzyłem trzy karty KPI, które pokazują:
Liczbę depozytów (Liczba depozytów)
Średnią liczbę dni od ostatniego kontaktu dla depozytów (Średnia liczba dni dla depozytów)
Skuteczność kampanii w procentach (Skuteczność kampanii %)

Wykres słupkowy: 

Utworzyłem wykres słupkowy pokazujący „Liczbę kontaktów z pojedynczym klientem” w zakresie od 1 do 8. Wykres ten przedstawia liczbę klientów, którzy mieli określoną liczbę kontaktów, oraz skuteczność tych kontaktów.
Wykres liniowy:

Wizualizacja macierzowa:

Zastosowałem macierz do wizualizacji wpływu „Kategorii dni od ostatniego kontaktu” na skuteczność kampanii, aby lepiej zrozumieć, które grupy czasowe miały najwyższy wskaźnik pozytywnych odpowiedzi.

### 4. Optymalizacja i formatowanie raportu

Formatowanie wizualizacji: Użyłem spójnych kolorów, czcionek i stylów, aby raport był estetyczny i czytelny.
Dodanie filtrów i slicerów: Zastosowałem slicery do dynamicznego filtrowania wyników według liczby kontaktów i kategorii dni od ostatniego kontaktu.
Przekształcenie wykresów: Zastosowałem różne typy wykresów, aby lepiej zobrazować wyniki i zależności między zmiennymi.

## Podsumowanie

Ten projekt analizuje skuteczność kampanii marketingowej banku, koncentrując się na liczbie kontaktów, czasie od ostatniego kontaktu oraz wynikach w postaci otwartych depozytów. Analiza pomaga lepiej zrozumieć, jakie czynniki mają największy wpływ na decyzje klientów, co może być przydatne do optymalizacji przyszłych kampanii. W projekcie wykorzystano zaawansowane funkcje DAX oraz narzędzia wizualizacyjne Power BI, aby przedstawić wyniki w sposób przystępny i interaktywny.
