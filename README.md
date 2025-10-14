# Pfam-domain-search-EVs-Entamoeba-histolytica-Sharma
Pipeline en Google Colab diseñado para la búsqueda, filtrado y visualización de dominios proteicos mediante modelos ocultos de Markov (HMMs) utilizando la herramienta HMMER3.
Este flujo de trabajo automatiza la identificación de dominios conservados de Pfam en proteomas o subconjuntos de proteínas de interés.

Los modelos ocultos de Markov (HMMs) son algoritmos estadísticos que representan patrones probabilísticos dentro de secuencias biológicas (como proteínas o ácidos nucleicos).
En el contexto de HMMER3, estos modelos permiten detectar dominios y motivos conservados en una proteína comparándola contra los perfiles probabilísticos depositados en la base Pfam-A, lo que ofrece mayor sensibilidad y precisión que las búsquedas por similitud directa (como BLAST).

El análisis se basó en el proteoma descrito por Sharma et al. (2020) —Characterization of Extracellular Vesicles from Entamoeba histolytica Identifies Roles in Intercellular Communication That Regulates Parasite Growth and Development, mBio, 11:e03138-19— tomando como referencia las 40 proteínas más abundantes encontradas en las vesículas extracelulares (EVs) de Entamoeba histolytica, seleccionadas según sus cuentas espectrales reportadas en dicho estudio.

El pipeline se ejecuta de forma interactiva en Google Colab mediante el notebook PFAM.ipynb, el cual solicita al usuario subir su archivo proteoma.faa (con las secuencias proteicas en formato FASTA).
El flujo incluye los siguientes pasos principales:

Ejecución de HMMER3 (hmmscan) contra la base Pfam-A.hmm.

Filtrado de hits por cobertura mínima (≥0.5) y valor i-Evalue ≤ 1e−5 para garantizar relevancia estadística.

Generación automática de archivos de salida:

pfam_filtered.tsv: resultados tabulares filtrados

pfam_filtered.gff3: anotaciones en formato GFF3

pfam_counts.png: gráfico con los dominios más frecuentes

pfam_heatmap_all.png: heatmap Proteína × Dominio Pfam

Visualización y exportación de los resultados finales.

💡 Resumen técnico

Lenguaje: Python 3

Entorno: Google Colab

Herramientas: HMMER3, Pfam-A, pandas, matplotlib, seaborn

Entradas: proteoma.faa

Notebook principal: PFAM.ipynb

Salidas: .tsv, .gff3, .png

📚 Referencia

Sharma, M., Morgado, P., Zhang, H., Ehrenkaufer, G., Manna, D., & Singh, U. (2020).
Characterization of Extracellular Vesicles from Entamoeba histolytica Identifies Roles in Intercellular Communication That Regulates Parasite Growth and Development.
mBio, 11(5):e03138–19. https://doi.org/10.1128/iai.00349-20
