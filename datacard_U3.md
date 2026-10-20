import pandas as pd
import numpy as np

# 1. Definirea unității de analiză: 41 de județe x 5 ani
judete = ['AB', 'AR', 'AG', 'BC', 'BH', 'BN', 'BT', 'BV', 'BR', 'BZ', 'CS', 'CL', 'CJ', 'CT', 'CV', 'DB', 'DJ', 'GL', 'GR', 'GJ', 'HR', 'HD', 'IL', 'IS', 'IF', 'MM', 'MH', 'MS', 'NT', 'OT', 'PH', 'SM', 'SJ', 'SB', 'SV', 'TR', 'TM', 'TL', 'VS', 'VL', 'VN']
ani = [2018, 2019, 2020, 2021, 2022]

# Crearea tuturor combinațiilor posibile (Județ - An)
index_multiplu = pd.MultiIndex.from_product([judete, ani], names=['Judet', 'An'])
matrice_X = pd.DataFrame(index=index_multiplu).reset_index()

# 2. Simularea aducerii datelor (Aici vor veni datele reale din surse)
# Randamentul agricol din INS Tempo (kg/ha)
matrice_X['INS_Randament_Porumb'] = np.nan 

# Anomalia NDVI din GEE MODIS
matrice_X['MODIS_NDVI_mean'] = np.nan 

# Indicele SPEI din Copernicus ERA5-Land
matrice_X['ERA5_SPEI_3'] = np.nan 

# 3. Afișarea primelor rânduri și a dimensiunii (n x d)
print(f"Dimensiunea Matricei X: {matrice_X.shape[0]} eșantioane x {matrice_X.shape[1]} trăsături")
print("-" * 50)
print(matrice_X.head(10))

# Export opțional pentru verificare
# matrice_X.to_csv('matrice_X_U3.csv', index=False)
