# Lenguaje Claro - UPE
Lucas Pecina

09/01/21

---
### Objetivo
Comparar distintos textos (legales, judiciales, etc) para ver la complejidad que tiene ese texto en cuanto a palabras dificiles (poco frecuentes en el lenguaje cotidiano).

### Resumen
El lenguaje legal/judicial suele ser complicado de entender para la gente que no se dedica a temas relacionados debido a la complejidad de las palabras utilizadas y de su gramatica. El analisis de complejidad gramatical de los textos requiere la utilizacion de tecnicas muy sofisticadas y que no dan buenos resultados, por lo tanto, descartamos este tipo de estudio por el momento.

Comenzamos solo analizando las **palabras** de los textos y creamos un **indice de complejidad** que mide la cantidad y frecuencia de palabras "complejas", que son de poca frecuencia en el lenguaje cotidiano. 

No contaran para el calculo aquellas palabras que por su naturaleza tecnica juridica requiera de su uso obligatorio. Para dicha tarea, se elaborara a mano una lista de las palabras en cuestion.

### Fuentes de datos
- Textos a analizar: seran cargados como archivos de texto
 - Codigo Procesal Civil y Comercial actual http://biblioteca.asesoria.gba.gov.ar/redirect.php?id=2121 esta en un archivo CPCC
 - Codigo Procesal Penal actual http://servicios.infoleg.gob.ar/infolegInternet/anexos/0-4999/383/texact.htm 
- Bolsa de palabras de frecuencia del lenguaje español http://corpus.rae.es/lfrecuencias.html. Usando las 300mil palabras mas frecuentes del español: en datos/

### Pasos
1. Corpus de palabras frecuentes
 - Armar dataframe con frecuencias
 - Calcular complejidad de palabras
2. Cargar textos y preprocesarlo
 - Tokenizar las palabras
 - Limpiar errores
 - Remover stopwords


---
### Indice de complejidad del lenguaje
$$Complejidad_t = \frac{1}{P}\sum_p^P{Complejidad_p}$$

- t = texto a analizar
- p = lista de palabras en el texto t (pueden estar repetidas)
- P = cantidad de palabras en el texto t (todas)

$$Complejidad_p = f(FrecuenciaBolsa_p)$$

$$Complejidad_p = \frac{1}{FrecuenciaBolsa_p}$$
