# OrchidAI - lista funkcji

    
## Moduł: Magazyn

### [M] US-01: Rejestracja strat (zwiędłe kwiaty)
- **Opis:** Jako magazynier chcę usunąć z magazynu zwiędłe kwiaty lub uszkodzone dekoracje wraz z podaniem powodu, żeby stany magazynowe były poprawne.
- **Kryteria:**
  - Wybór produktu z listy stanów magazynowych
  - Wpisanie liczby sztuk do usunięcia
  - Wybranie powodu usunięcia
  - Automatyczne pomniejszenie ilości sztuk w bazie
 
### [M] US-02: Rejestracja dostaw
- **Opis:** Jako magazynier chcę zarejestrować wszystkie sztuki w bazie, podając nazwę dostawcy, czas dostawy oraz całkowity wolumin
- **Kryteria:**
  - Wybór pozycji z listy produktów lub utworzenie nowej
  - Wpisanie liczby sztuk do dodania na stan magazynowy
  - Wprowadzenie danych dostawy, np. czasu dostawy, nazwy firmy itp.
 
### [S] US-03: Inwentaryzacja
- **Opis:** Jako magazynier chcę sprawdzić czy meteriał na stanie w systemie zgadza się z rzeczywistością
- **Kryteria:**
  - Pod koniec miesiąca magazynier przeprowadza audyt
  - Może dowolnie dodawać i usuwać materiał (wzrost ilości lub strat) na stanie magazynowym
  - Odbywa się to bez konieczności raportowania dostawy czy tworzenia spisów strat (uzgodnienie stanu magazynowego z      fizycznym)
 
### [S] US-00: Przyjęcie na stan z brakiem, uszkodzeniem lub zamiennikiem
- **Opis:** Jako magazynier chcę przyjąć dostawę z rozbieżnościami
- **Kryteria:**
  - Jeden dostawca miał przywieźć 1000 szt. róży Red Naomi. 50 szt. przyjechało uszkodzone, 20 brakowało, a 100 szt.      okazało się tańszym zamiennikiem Madame Red
  - Magazwynier przyjmuje dostawę, ale w systemie oznacza odpowiednią ilość mateiriału odpowiednimi etykietami BRAK,
    USZKODZONE, ZAMIENNIK
  - 830 szt. zostaje dodane do stanu MAG, a pozostałe 170 
  - Takie rozwiązanie pozwala na udokumentowanie dostawy i szybszy/łatwiejszy proces reklamacji
  - Takie rozwiązanie pozwala na nieprzerzucanie odpowiedzialności na pracowników i wiarygodną analitykę biznesową
 
### [C] US-00: Generowanie protokołu rozbieżności
- **Opis:** Jako magazynier chcę wygenerować w systemie protokół rozbieżności dostawy
- **Kryteria:**
  - Przyjmuję dostawę z rozbieżnościami
  - System generuje raport rozbieżności

## Moduł: Pracownia
 
### [M] US-03: Kontrola stanu wykonywanych prac
- **Opis:** Jako florysta przy realizacji zamówienia zapomniałem numeru zlecenia i nie wiem co zamówiłem na dziś       do pracowni
- **Kryteria:**
  - Oglądam historię zamówień z MAG do WIP
  - Klikam na interesujący mnie materiał i wyświetla mi się numer zlecenia, z którego pochodzi
  - Filtry umożliwiają mi grupowanie mateirałów w liście w poszczególne BOMy 


### [M] US-04: Rezerwacja materiału na MAG do danego NZ
- **Opis:** Jako florysta rezerwuję materiał na MAG do wykorzystania w zamówieniu długoterminowym
- **Kryteria:**
  - Klient złożył zamówienie, które trzeba zrealizować najbliżej za tydzień (zakładam istnienie poziomów priorytetów      w zleceniach)
  - Wybieram w systemie rodzaj i ilość materiału na magazynie i rezerwuję go pod konkretne zlecenie
  - System nie pozwoli mi pobrać zarezerwowanego materiału do innego zlecenia o niższym priorytecie
 
### [M] US-05: Zwrot materiału z WIP do MAG
- **Opis:** Jako florysta chce oddać część materiału z WIP do MAG
- **Kryteria:**
  - Klient zamówił bukiet ślubny na dziś
  - Po godzinie dzwoni poinformować, że zrezygnował z usługi
  - W systemie zaznaczam każdy materiał z osobna lub cały BOM i przesuwam stan z WIP do MAG
 
### [S] US-00: Wykorzystanie materiałów pomocniczych
- **Opis:** Jako florysta chcę ściągnąć na WIP materiały pomocnicze, np. wstążki, toppery, lakiery, itp.
- **Kryteria:**
  - Na WIP skończył się lakier ozdobny
  - W systemie zamawiam go z MAG bez generowania BOMów ani numerów zleceń NZ 
