# Analiza podatkov s programom R, 2016/17

Repozitorij z gradivi pri predmetu APPR v študijskem letu 2016/17

Avtor: Luka Lodrant

## Tematika

Za temo svojega projekta sem si izbral analizo podatkov o globalnem segrevanju. Primerjal bom podatke o povprečnih mesečnih temperaturah v zadnjih 300 letih po celem svetu in v njih poskusil najti razne vzorce. Poleg tega bom za zadnje 50 let zajel tudi podatke o CO2 izpustih, poseku gozdov, porabi sveže vode in pa številu prebivalstva in poskusil najti povezave med temi podatki in povrečnimi temperaturami.

Podatki bodo zajeti iz sledečih spletnih strani:
* http://data.worldbank.org/topic/climate-change
* https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data

Prek pridobljenih podatkov bom poskusil tudi napovedati temparature površja v prihodnosti, in na modelu ugotoviti, izboljšanje katerega izmed primarnih onesnaževalnih dejavnikov bi najbolj umirilo rast temperatur.

## Program

Glavni program in poročilo se nahajata v datoteki `projekt.Rmd`. Ko ga prevedemo,
se izvedejo programi, ki ustrezajo drugi, tretji in četrti fazi projekta:

* obdelava, uvoz in čiščenje podatkov: `uvoz/uvoz.r`
* analiza in vizualizacija podatkov: `vizualizacija/vizualizacija.r`
* napredna analiza podatkov: `analiza/analiza.r`

Vnaprej pripravljene funkcije se nahajajo v datotekah v mapi `lib/`. Podatkovni
viri so v mapi `podatki/`. Zemljevidi v obliki SHP, ki jih program pobere, se
shranijo v mapo `../zemljevidi/` (torej izven mape projekta).

## Potrebni paketi za R

Za zagon tega vzorca je potrebno namestiti sledeče pakete za R:

* `knitr` - za izdelovanje poročila
* `rmarkdown` - za prevajanje poročila v obliki RMarkdown
* `shiny` - za prikaz spletnega vmesnika
* `DT` - za prikaz interaktivne tabele
* `maptools` - za uvoz zemljevidov
* `sp` - za delo z zemljevidi
* `digest` - za zgoščevalne funkcije (uporabljajo se za shranjevanje zemljevidov)
* `readr` - za branje podatkov
* `rvest` - za pobiranje spletnih strani
* `reshape2` - za preoblikovanje podatkov v obliko *tidy data*
* `dplyr` - za delo s podatki
* `gsubfn` - za delo z nizi (čiščenje podatkov)
* `ggplot2` - za izrisovanje grafov
* `extrafont` - za pravilen prikaz šumnikov (neobvezno)
