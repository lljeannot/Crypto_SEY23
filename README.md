
# **Seabird-derived nutrients influence feeding pathways and body size in cryptobenthic reef fishes**

**This repository contains code and data presented in the article**:
  
  Authors (anonymised). Seabird-derived nutrients influence feeding pathways and body size in cryptobenthic reef fishes.


## 1. How to download this project?

On the project main page on Anonymous GitHub, click on the button `Download Repository` and then extract the ZIP folder.



## 2. Description of the project

### 2.1 Project organization

This project is organized in 3 folders:
  
* :file_folder:	`data` folder contains 10 datasets and 3 KML files (see **2.2 Datasets description**).
* :file_folder:	`output_data` folder contains 4 datasets generated for mixing models.
* :file_folder:	`figures` folder contains 1 subfolder `silhouettes` containing 11 PNG files.


### 2.2 Datasets description

* SEY23 datasets

All SEY23 datasets correspond to data collected in Fregate Island, Seychelles, between the 27/03/2023 and the 10/04/2023, and results from associated analyses (stable isotope data).

The dataset _SEY23_Crypto_data.csv_ corresponds to all fish data sampled using anaesthetic stations, and contains the following variables:
- `ID` Sample ID
- `GENSPE` Genus and species
- `FAM` Family
- `TL` Total length (mm)
- `W` Weight (g)
- `TUBE` Sampling tube

The dataset _SEY23_Site_info.csv_ corresponds to site-specific information, and contains the following variables:
- `Site` Site ID
- `Location` Seabird-rich (High) or seabird-poor (Low)
- `Lat` Latitude
- `Lon` Longitude
- `Depth` Sampling depth (m)
- `CSL` Curved surface length
- `Complexity` Complexity index
- `Community` Inclusion of site for community-level analyses


The datasets _SEY23_Crypto_SIA_data.csv_ and _SEY23_Source_SIA_data.csv_ both contain C and N isotope values for cryptobenthic fishes and benthic and pelagic end-members respectively:
 - `ID` Sample ID
- `GENSPE` / `Source` Genus and species or end-member category
- `d15N` Measure of the ratio of the two stable isotopes of nitrogen, 15N:14N (‰)
- `d13C` Measure of the ratio of the two stable isotopes of carbon, 13C:12C (‰)

The datasets _SEY23_UVC.csv_ and _SEY23_Benthic_cover.csv_ correspond to underwater surveys of visually conspicuous fishes and benthic cover transects respectively.

* UVC datasets

The datasets _UVC_info.csv_ and _UVC_lw.csv_ correspond to feeding group and Bayesian length-weight estimates extracted from the literature of all visually conspicuous species recorded in the underwater surveys.

* Trophic discrimination factors

The table _crypto_discr_SIA_mix.csv_ corresponds to TDFs for C and N isotopes (Post, 2002).

* KML files

The files _Fregate_Lesser_noddy_territories.kml_ and _Fregate_Fairy_tern-points.kml_ contain information regarding annual seabird censuses on Fregate island.
The file _contours.kml_ represents 10-m isopleths.

### 2.3 Code description

The _SEY23.Rmd_ code is formatted in Rmarkdown and contains all R-based analyses and code to reproduce data and figures from the paper. It is divided into six sections:

* I. Stable isotope analysis - d15N
* II. Stable isotope analysis - d13C
* III. Mixing models
* IV. Community effects
* V. Species-specific effects
* VI. UVC


## 3. Reproducibility parameters


```R
R version 4.3.2 (2023-10-31 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 10 x64 (build 19045)

Matrix products: default


locale:
  [1] LC_COLLATE=English_United Kingdom.utf8  LC_CTYPE=English_United Kingdom.utf8    LC_MONETARY=English_United Kingdom.utf8 LC_NUMERIC=C                           
[5] LC_TIME=English_United Kingdom.utf8    

time zone: Europe/London
tzcode source: internal

attached base packages:
  [1] grid      stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
  [1] rgdal_1.6-7              lubridate_1.9.3          stringr_1.5.1            dplyr_1.1.3              purrr_1.0.2              readr_2.1.5              tidyr_1.3.0             
[8] tibble_3.2.1             tidyverse_2.0.0          plyr_1.8.9               fishflux_0.0.1.6         forcats_1.0.0            modelr_0.1.11            emmeans_1.10.1          
[15] ggcheck_0.0.5            MixSIAR_3.1.12           rfishbase_4.1.2          tidybayes_3.0.6          brms_2.21.0              Rcpp_1.0.12              ggformula_0.12.0        
[22] ggridges_0.5.6           scales_1.3.0             vcd_1.4-12               ggpubr_0.6.0             lwgeom_0.2-14            performance_0.11.0       RColorBrewer_1.1-3      
[29] corrplot_0.92            reshape2_1.4.4           mapdata_2.3.1            labdsv_2.1-0             mgcv_1.9-1               nlme_3.1-164             ade4_1.7-22             
[36] ggord_1.1.8              ggvegan_0.1.999          vegan_2.6-4              lattice_0.22-6           permute_0.9-7            raster_3.6-26            sp_2.1-4                
[43] mapproj_1.2.11           sf_1.0-16                viridis_0.6.5            viridisLite_0.4.2        maps_3.4.2               magick_2.8.3             XML_3.99-0.16.1         
[50] tmap_3.3-4               rnaturalearthdata_1.0.0  rnaturalearthhires_0.2.1 rnaturalearth_1.0.1      ggimage_0.3.3            ggnewscale_0.4.10        gtable_0.3.5            
[57] cowplot_1.1.3            ggrepel_0.9.5            ggmap_4.0.0              ggplot2_3.5.1            NCmisc_1.2.0    
```
