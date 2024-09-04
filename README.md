Opis Projektu:

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
- 
