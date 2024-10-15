# Algorytmy geometryczne

To repozytorium zawiera implementację wybranych algorytmów geometrycznych.

## Klonowanie repozytorium

Aby skolonować to repozytorium wraz z modułem narzędzia wizualizującego musimy skorzystać z komendy:

```bash
git clone --recurse-submodules https://github.com/WSm-77/geometric_algorithms.git
```

## Narzędzie bit-algo-vis-tool

Podczas ćwiczeń korzystaliśmy z narzędzia dostarczonego przez koło naukowe **_Bit_**.

### Konfiguracja narzędzia bit-algo-vis-tool

Aby skorzystać z narzędzia wizualizującego należy skonfigurować środowisko (condę) zgodznie z instrukcją zawartą w **README.md** repozytorium narzędzia z uwzględnieniem, że  wszystkie komendy należy wykonać w folderze bit-algo-vis-tool.

#### 1. Stworzenie środowiska

```bash
conda create --name bit-algo-vis-tool python=3.9
conda activate bit-algo-vis-tool
```
#### 2. Pobranie niezbędnych pakietów

```bash
python3 setup.py sdist
python3 -m pip install -e .
```

#### 3. Użytkowanie

Teraz jeżeli jesteśmy w nowo stworzonym środowisku (w terminalu przed nazwą użytkownika powinno wyświetlać się __(bit-algo-vis-tool)__) tworzymy Jupyter notebook, w którym jako kernel wybieramy interpreter pythonwy z nowo stworzonego środowiska.

W przypadku zwykłych skryptów pythonowych (plików _.py_) w VSCode możemy ustawić interpreter na ten z środowiska __bit-algo-vis-tool__:

```
ctrl+shift+p > Python: Select Interpreter
```

Miejsce, w którym stworzymy nowy plik nie ma znaczenia - konfiguracja środowiska sprawia, że folder _bit-algo-vis-tool_ postrzegany jest jako folder główny projektu, więc jeżeli przykładowo chcemy skorzystać z klasy **_Visualizer_** wystarczy ją zaimportować:

```python
from bitalg.visualizer.main import Visualizer
```

W przypadku problemów pierwszym krokiem powinno być zrestartowanie środowiska:

```bash
conda deactivate
conda activate bit-algo-vis-tool
```
