# BibliotekaDomowaAPI
Interfejs API oparty o REST obsługujący domową bibliotekę napisany za pomocą języka Python.
# Uruchomienie
Do uruchomienia aplikacji oprócz Python w wersji 3.8 lub wyższej będziemy potrzebować microframeworku Flask w wersji 1.1.2.
Po pobraniu i zainstalowaniu wymaganych modułów uruchamiamy aplikację app.py.
# Obsługa
Najprostrzym sposobem komunikacji z interfejsem jest odwiedzenie adresu http://127.0.0.1:5000/api/v1/books/,
który wyświetli aktualną listę książek dostępnych w bibliotece w formacie JSON.  
  
Aby przejść do konkretnej dostępnej książki na koniec adresu wystarczy dopisać numer id np. http://127.0.0.1:5000/api/v1/books/2.  
  
Interfejs umożliwia również dodanie nowej książki dzięki metodzie POST wysłanej na adres http://127.0.0.1:5000/api/v1/books/.  
Jedynym wymaganym parametrem jest tytuł ('title') ale możliwe jest również podanie autora ('author'), roku wydania ('year'), krótkiego opisu ('description') oraz informacji czy ksążka została już przeczytana czy nie.  
  
Konkretna książka może być usuwana metodą DELETE na adres danej książki np. http://127.0.0.1:5000/api/v1/books/1.  
  
Update wybranej książki odbywa się według zasad REST poprzez metodę PUT na adres książki np. /api/v1/books/3  
Wystarczy tylko podać parametr, którego wartość chcemy zmienić oraz nową zawartość.
