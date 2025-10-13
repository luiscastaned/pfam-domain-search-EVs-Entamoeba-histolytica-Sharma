# Pfam-domain-search-EVs-Entamoeba-histolytica-Sharma
Pipeline en Google Colab diseñado para la búsqueda, filtrado y visualización de dominios proteicos mediante modelos ocultos de Markov (HMMs) con la herramienta HMMER3.
Este flujo de trabajo permite identificar y caracterizar dominios conservados de Pfam en proteomas o subconjuntos proteicos de interés.

El análisis se basó en el proteoma descrito por Sharma et al. (2020), Characterization of Extracellular Vesicles from Entamoeba histolytica (mBio, 11:e03138-19), tomando como referencia las 40 proteínas más abundantes detectadas en las vesículas extracelulares (EVs) de E. histolytica, seleccionadas según sus cuentas espectrales reportadas en dicho estudio.

El pipeline implementa los siguientes pasos:

Ejecución automatizada de HMMER3 (hmmscan) contra la base Pfam-A.hmm.

Filtrado por cobertura mínima (≥0.5) y valor i-Evalue (≤1e−5) para garantizar la calidad estadística de los hits.

Generación de archivos TSV y GFF3 con las anotaciones filtradas.

Construcción de un heatmap Proteína × Dominio Pfam en formato visual, útil para análisis funcionales comparativos.

El notebook está completamente reproducible y optimizado para correr en Google Colab, sin necesidad de instalación local.
