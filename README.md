# ESMFold__AlphaFold2
Рассматриваем две структуры:
### 1. Лизоцим (Hen Egg White Lysozyme) — контрольный белок
**PDB:** 1LYZ (рентгеновская кристаллография, 2.00 Å)
**Длина:** 129 а.о.
Хорошо изученный, стабильный белок. Оба метода должны показать высокий pLDDT (>90).

```text
>1LYZ_HenEggWhiteLysozyme
KVFGRCELAAAMKRHGLDNYRGYSLGNWVCAAKFESNFNTQATNRNTDGSTDYGILQINSRWWCNDGRTPGSRNLCNIPCSALLSSDITASVNCAKKIVSDGNGMNAWVAWRNRCKGTDVQAWIRGCRL
```

### 2. Gaussia Luciferase (GLuc) — белок с известной ЯМР-структурой
**PDB:** 7D2O (ЯМР, 2020) / 9FLA (ЯМР, 2024)
**Длина:** 168 а.о.

```text
>GLuc_GaussiaPrinceps
KPTENNEDFNIVAVASNFATTDLDADRGKLPGKKLPLEVLKEMEANARKAGCTRGCLICLSHIKCTPKMKKFIPGRCHTYEGDKESAQGGIGEAIVDIPEIPGFKDLEPMEQFIAQVDLCVDCTTGCLKGLANVQCSDLLKKWLPQRCATFASKIQGQVDKIKGAGGD
```
Используя [ESMFold](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/ESMFold.ipynb#scrollTo=CcyNpAvhTX6q) и [AlphaFold2](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/AlphaFold2.ipynb#scrollTo=G4yBrceuFbf3) получаем ZIP-архивы c необходимыми файлами.

