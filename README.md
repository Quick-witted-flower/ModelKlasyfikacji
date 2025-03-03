# Model Klasyfikacji Gatunków Kwiatów z wykorzystaniem Sieci Neuronowych

## Wprowadzenie
Celem tego projektu jest klasyfikacja gatunków kwiatów z wykorzystaniem zbioru danych **Iris** oraz modelu opartego na **sztucznych sieciach neuronowych** (ANN - Artificial Neural Networks). Model wykorzystuje **TensorFlow/Keras** do budowy i treningu sieci neuronowej.

## Funkcjonalności

### 1. Wczytanie i eksploracja danych:
   - Pobranie zbioru danych **Iris** z pliku iris.csv.
   - Podział na cechy (`X`) i etykiety (`y`).
   - Zamiana etykiet na reprezentację **one-hot encoding**.

### 2. Podział danych:
   - Podział zbioru na **zbiór treningowy (80%) i testowy (20%)**.
   - Utrzymanie proporcji klas w obu zbiorach.

### 3. Budowa modelu sieci neuronowej:
   - **Warstwa wejściowa:** 4 neurony (odpowiadające cechom danych Iris).
   - **Warstwa ukryta:** 10 neuronów, funkcja aktywacji **ReLU**.
   - **Warstwa wyjściowa:** 3 neurony (dla trzech gatunków), funkcja aktywacji **Softmax**.
   - **Funkcja straty:** `categorical_crossentropy` (odpowiednia dla klasyfikacji wieloklasowej).
   - **Optymalizator:** `Adam`.

### 4. Trenowanie modelu:
   - Model jest trenowany przez **100 epok**, z **batch_size=5**.
   - Śledzona jest strata i dokładność na zbiorze walidacyjnym.

### 5. Ocena modelu:
   - Wyliczona dokładność modelu na zbiorze testowym.
   - Wykres przedstawiający zmianę straty i dokładności w trakcie treningu.

## Technologie
Projekt został stworzony z użyciem:
- **Python**: Język programowania do analizy danych i trenowania modelu.
- **TensorFlow/Keras**: Tworzenie i trenowanie sieci neuronowych.
- **Scikit-learn**: Pobranie zbioru danych, podział na treningowy/testowy, kodowanie etykiet.
- **Matplotlib/Seaborn**: Wizualizacja wyników.
- **NumPy/Pandas**: Manipulacja danymi.

## Pliki projektu:
- `model_iris.ipynb`: Skrypt implementujący proces trenowania i oceny modelu.
- `README.md`: Dokumentacja projektu.
- `iris.csv`; zbiór danych 

## Uruchomienie projektu
1. **Zainstaluj wymagane biblioteki**:
   ```bash
   pip install numpy pandas tensorflow scikit-learn matplotlib seaborn
   ```
2. **Uruchom główny skrypt**:
   ```bash
   python model_iris.ipynb
   ```
3. **Otrzymasz wyniki dokładności modelu oraz wykresy przedstawiające proces uczenia.**

