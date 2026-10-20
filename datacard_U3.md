# Data Card: Proiect MEDE - CP1
**Autor:** Popa Cătălina-Florentina (U3)  
**Tema:** Impactul secetei agricole din anul 2022 asupra culturilor (Studiu de caz pe 41 de județe din România)  
**Perioada analizată:** 2018 – 2022 (5 ani)  
**Unitatea de analiză:** Județ × An (41 județe × 5 ani = 205 unități observaționale)

---

## 1. Sursa 1: INS Tempo (Randament Agricol)
* **Proveniență:** Institutul Național de Statistică (INS) – Baza de date TEMPO online.
* **Perioada acoperită:** 2018 – 2022.
* **Rezoluție spațială / temporală:** Nivel județean (41 județe) / Agregare anuală.
* **Variabilă extrasă:** Randamentul culturilor agricole (producția de porumb / hectar).
* **Unități de măsură:** kg/ha sau tone/ha.
* **Goluri & Calitate:** 194 valori valide din 205 (Aproximativ 94.6% acoperire).
* **Licență / Acces:** Open Data / Uz academic.

---

## 2. Sursa 2: GEE MODIS NDVI (Indicele de Vegetație)
* **Proveniență:** Google Earth Engine / Colecția MODIS (MOD13Q1).
* **Perioada acoperită:** 2018 – 2022 (sezonul estiv).
* **Rezoluție spațială / temporală:** 250 metri / Compozit la 16 zile, mediat la nivel de județ.
* **Variabilă extrasă:** `MODIS_NDVI_mean` (Media indicelui de vegetație).
* **Unități de măsură:** Adimensional (valori între 0.0 și 1.0).
* **Goluri & Calitate:** 204 valori valide din 205 (99.5% acoperire).
* **Licență / Access:** NASA LP DAAC – Open Data prin GEE.

---

## 3. Sursa 3: ERA5-Land (Parametri Climatici / SPEI)
* **Proveniență:** Copernicus Climate Change Service (C3S) / ERA5-Land prin GEE.
* **Perioada acoperită:** 2018 – 2022.
* **Rezoluție spațială / temporală:** ~9 km / Pas lunar și sezonier.
* **Variabilă extrasă:** `ERA5_Temp_Vara` / indici hidrologici de secetă.
* **Unități de măsură:** Grade Celsius (°C) / Adimensional.
* **Goluri & Calitate:** 197 valori valide din 205 (96.1% acoperire).
* **Licență / Access:** Copernicus / ECMWF – Open Data.

---

## 4. Sinteza Matricei de Aliniere (Matricea X)
* **Dimensiune totală:** 205 rânduri (41 județe × 5 ani) × 5 coloane principale.
* **Observații complete pentru model:** 185 rânduri complet curate.
* **Rată de acoperire globală:** 90.2%, validată prin scriptul Python din repository (`CP1_Matrice_X.ipynb`).
