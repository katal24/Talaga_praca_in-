# Talaga_praca_inż
Repozytorium zawiera:
1. Plik w języku R - odpowiedzialny za obliczenia.
2. Bibliotekę .jar
3. Kod źródłowy biblioteki w języku Java
4. Prosty projekt w Javie, który obrazuje działanie biblioteki.

Aby użyć bibliotekę PairwiseComparisons w swoim projekcie należy:
1. Zainstalować pakiet R (http://cran.us.r-project.org/)
2. W folderze głównym projektu umieścić plik pairwiseComparisons.R
3. Załączyć bibliotekę PairwiseComparisons.jar
4. Importować klasę z biblioteki: import main.out.pl.edu.agh.talaga.PairwiseComparisons;
5. Utworzyć nowy obiekt klasy i zacząć wywoływać metody.

Pomocne informacje do współpracy z biblioteką.
1. Biblioteka (a raczej RCallerScriptEngine, który wywołuje metody z R) może pracować w trybie "ciągłym" (jedno trwałe połączenie z silnikiem R) lub "jednorazowym" (otwiera i zamyka połączenie z silnikiem R dla każdej fukncji). 
Tryb "ciągły" wywołuje kolejne metody szybciej, należy jednak pamiętać o obciążeniu procesora oraz o tym, żeby na końcu aplikacji samodzielnie zamnkąć silnik.

2. Konstruktor domyślny otwiera powoduje, że silnik pracuje w trybie jednorazowym. Aby to zmienić można wywołać konstruktor z parametrem false: new PairwiseComparisons(true).

3. Funkcja seetKeepOpenConnection(boolean) służy do określania trybu pracy sinika, przekazywana do niej wartość decyduje, czy pracujemy w trybie "ciągłym", czy "jednorazowym". Można ją wywoływać wielokrotnie w czasie działania aplikacji.

3. Można również ręcznie otwierać i zamykać połączenie poprzez metody open() i close().
