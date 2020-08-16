# Mapes de Catalunya amb shiny
#### _Ariadna Angulo-Brunet_

Per accedir a la app [https://angulobrunet.shinyapps.io/MapesCAT/](https://angulobrunet.shinyapps.io/MapesCAT/).

Aquesta aplicació s’ha creat per tal de poder crear mapes de Catalunya de forma relativament senzilla considerant diverses divisions territorials (municipis, comarques, províncies, àrees bàsiques de salut [ABS]  i regions sanitàries). 

Per tal de fer municipis, comarques i províncies s’ha utilitzat la cartografia de [CatSalut](https://catsalut.gencat.cat/ca/coneix-catsalut/transparencia/territori/informacio-cartografica/mapes/"). En canvi per a fer les ABS i les regions sanitàries s’ha fet servir la base municipal del [Institut Cartogràfic i Geològic de Catalunya]( https://ide.cat/geonetwork/srv/cat/catalog.search#/metadata/base-municipal-5k-v2r1)

Per a provincies s'ha fet servir dades de [arcgis](https://www.arcgis.com/home/item.html?id=83d81d9336c745fd839465beab885ab7)

Per dubtes o suggeriments pots posar-te en contacte amb mi a ariadna.angulo.brunet@gmail.com.

![imatge](https://github.com/AnguloB/mapesCatalunya/imatges/esquema.png)

##  El format

Per tal d'entrar les dades has de tenir en compte principalment dues coses:

1. Necessites una variable anomenada "valor" amb el valor numèric d’allò que vulguis representar (un recompte, una proporció, etc)
2. Necessites una variable en comú amb la base cartogràfica. 

- El codi de la ciutat, comarca, provincia, ABS o Regió sanitària. Aquesta variable és important que s'anomeni "codi".

- Pot ser el nom de la ciutat, comarca, provincia, ABS o Regió sanitària. Aquesta variable és important anomenar-la "nom".



| Mapa              | Relació de codis i exemples | 
| -------------     |-------------| 
| `Ciutats`         | [codis ciutats](https://github.com/AnguloB/mapesCatalunya/dades/01_relacio_Ciutats_201408.csv) i [exemple ciutats](https://github.com/AnguloB/mapesCatalunya/exemples/ciutats.txt)     | 
| `Comarques`       | [codis comarques](https://github.com/AnguloB/mapesCatalunya/dades/01_relacio_comarques_201408.csv) i [exemple comarques](https://github.com/AnguloB/mapesCatalunya/exemples/comarques.txt)  |
| `Provincies`      | [codis provincies](https://github.com/AnguloB/mapesCatalunya/dades/01_relacio_Provincia_201408.csv) i [exemple provincies](https://github.com/AnguloB/mapesCatalunya/exemples/provincia.txt)      | 
| `ABS`             | [codis ABS](https://github.com/AnguloB/mapesCatalunya/dades/01_relacio_ABS_201408.csv)  i [exemple ABS](https://github.com/AnguloB/mapesCatalunya/exemples/ABS.txt)   |
| `Regió sanitària` | [codis RS](https://github.com/AnguloB/mapesCatalunya/dades/01_relacio_RS_201408.csv) i [exemple RS](https://github.com/AnguloB/mapesCatalunya/exemples/RS.txt)    | 

## Abans de començar

Assegura’t de que els codis que hi ha al arxiu que puges siguin correctes. Posem per exemple que volem treballar amb províncies. El codi de Barcelona "08" comença amb un 0, i en moltes ocasions les fulles de text els ometen. Això pot donar problemes per exemple amb els "csv" si els obrim en un full de càlcul d'Excel. Una bona opció pot ser convertir-ho a txt, i assegurar-se de que el 08 figura entre cometes "08".

| codi| **codi incorrecte** | nom         | valor  |
| ----| ----|-------------| -----|
| 08  | **8**  | Barcelona   | 60 |
| 17  | **17**  | Girona      |   20 |
| 25  | **25**  | Lleida      |    10 |
| 43  | **43**  | Tarragona   |    5 |


