# 🧬 Pipeline per a l'anàlisi de dades de citometria espectral

Aquest repositori conté un pipeline en R per a l’anàlisi de dades de citometria de flux espectral, enfocat a la identificació i caracterització de subpoblacions cel·lulars. Està creat en base a un panell específic però es pot modificar segons les necessitats de cada experiment. 

El flux de treball inclou:

- Control de qualitat automatitzat
- Clustering no supervisat
- Visualització de poblacions
- Anotació biològica assistida


## ⚙️ Requisits

El pipeline requereix els paquets següents: 
```{r}
library(flowCore)
library(PeacoQC)
library(FlowSOM)
library(cytoMEM)
library(dplyr)
```


## 🧠 Notes importants

El pipeline assumeix que la transformació de dades i el gating inicial (singlets, live, lymphocytes, etc) ja està fet.

Els canals utilitzats (channelsqc, channels_fsom) s’han d’adaptar segons el panell experimental.

L’anotació final és semi-manual i depèn del coneixement biològic.


## 📂 Estructura del projecte

```{r}
.
├── data/            # (opcional) Fitxers .FCS d'entrada
├── plots/           # Resultats gràfics
├── Pipeline.qmd         # Codi del pipeline
└── README.md
```

## 🐍 Entorn Conda
