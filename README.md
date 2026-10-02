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
Затем сравниваем средние значения pLDDT(predicted Local Distance Difference Test) - оценка того, насколько программа уверена в предсказанной структуре. 
В результате сравнения средних значений pLDDT получаем:

Белок                     | ESMFold (0-100)    | ColabFold (0-100)  | Разница
-------------------------------------------------------------------------------------
1LYZ_HenEggWhiteLysozyme  | 95.14              | 98.10              | -2.97
GLuc_GaussiaPrinceps      | 54.66              | 74.27              | -19.61

ESMFold и AlphaFold2 одинаково хорошо справляются с предсказанием структуры на простом, хорошо изученном белке, но AlphaFold2 значительно лучше на сложном.

Наконец, визуализируем структуры с помощью py3Dmol. 
- 1LYZ(обе): вся структура синяя, а значит уверенность высокая
- GLuc(ESMFold): много красного и жёлтого, нет уверенности
- GLuc (ColabFold): больше синего и зелёного, значительно лучше
  
<img width="895" height="641" alt="image" src="https://github.com/user-attachments/assets/921cbd3d-2f41-4324-93d1-b7a02d570e37" />
<img width="962" height="613" alt="image" src="https://github.com/user-attachments/assets/262ff64d-3e1c-4b8f-8664-cab7a304f6f9" />
<img width="887" height="610" alt="image" src="https://github.com/user-attachments/assets/7c54f859-a833-4e04-a60b-46525dcf9505" />
<img width="958" height="640" alt="image" src="https://github.com/user-attachments/assets/9ff3f16b-d7d2-4510-9c29-3329bca5c09f" />
