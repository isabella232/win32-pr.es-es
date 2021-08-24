---
description: En este tema se describen las consideraciones de lematización para los idiomas aglúxtivos y los pares suplentes Unicode, y para el uso de pares suplentes para ampliar el juego de caracteres Unicode para dar cabida a distintos juegos de caracteres.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Consideraciones lingüísticas y Unicode diversas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24372194fb17498e1e0ce19be1bbbac3f1dccb27a63d840cedf95de38f735026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594485"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Consideraciones lingüísticas y Unicode diversas

En este tema se describen las consideraciones de lematización para los idiomas aglúxtivos y los pares suplentes Unicode, y para el uso de pares suplentes para ampliar el juego de caracteres Unicode para dar cabida a distintos juegos de caracteres. En este tema también se describe cómo los separadores de palabras identifican las frases en el texto y controlan los espacios sin romper, y cómo los separadores de palabras y lematizadores controlan números y fechas, palabras compuestas, frases compuestas, palabras y caracteres especiales, acrónimos y abreviaturas y mayúsculas.

Este tema se organiza de la siguiente manera:

-   [Identificación de frases](#phrase-identification)
-   [Idiomas aglutivos](#agglutinative-languages)
-   [Números, horas y fechas](#numbers-times-and-dates)
-   [Palabras compuestas](#compound-words)
-   [Frases compuestas](#compound-phrases)
-   [Caracteres y palabras especiales](#special-characters-and-words)
-   [Acrónimos y abreviaturas](#acronyms-and-abbreviations)
-   [Uso de mayúsculas](#capitalization)
-   [Espacios nobreaking](#nonbreaking-spaces)
-   [Pares suplentes](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificación de frases

Las frases son una palabra o un grupo de palabras que una o más personas modifican. Las frases son difíciles de identificar de forma coherente porque se puede usar el mismo modificador en más de una frase con el mismo nombre. Por ejemplo, "nueva casa", "Casa de la casa del hogar", "nueva casa de la casa de la casa".

Windows La búsqueda usa frases con más frecuencia en el momento de la consulta. Las frases del texto de consulta reciben mayor peso que las palabras individuales. En el ejemplo anterior, un documento que contiene "House of Alcoy" se clasifica por encima de uno que contiene "House" y "House" en distintos puntos del documento. Se recomienda que los separadores de palabras generen una frase en tiempo de consulta si es probable que la frase coincida con al menos un documento.

## <a name="agglutinative-languages"></a>Idiomas aglutivos

Los lenguajes aglutivos forman palabras a través de la combinación de formas más pequeñas para expresar ideas compuestas. Por lo general, cada una de estas funciones tiene un significado o función y conserva su forma y significado originales durante el proceso de combinación. En el caso de los idiomas que tienen una morfología aglomerativa, como el turco, el finés, el húngaro o el coreano, es posible generar miles de formas para una palabra raíz determinada.

En la tabla siguiente se muestra una lista de formularios desfasados para la palabra finés "talo" ("house").



| Word      | Traducción   |
|-----------|---------------|
| Talo      | Casa         |
| Taloni    | Mi casa      |
| Talossa   | En la casa  |
| Talossani | En mi casa   |
| Tal talía    | Casas        |
| Taloissa  | En las casa |



 

Los idiomas inflectados, como el inglés, el francés y el latín, tienen un número muy pequeño de formas de palabras posibles para una palabra raíz. En los lenguajes con inflected, los métodos de transformación se influyen entre sí al enlazar. La mayoría de los cambios en la inflexión están presentes en la raíz o en el final de la palabra. A diferencia de los lenguajes aglutivos, los idiomas con aflectos tienden a tener funciones diferentes para un único morpheme. Por ejemplo, un morpheme puede determinar tanto el número como el caso.

Los lematizadores para lenguajes aglutivos deben sopesar el equilibrio entre el rendimiento y la precisión para generar solo un subconjunto del número de formas de palabras posibles.

## <a name="numbers-times-and-dates"></a>Números, horas y fechas

Los separadores de palabras deben usar un formato común para representar números, horas y fechas para facilitar la consulta coherente.

Al crear un separador de palabras, se recomienda que el separador de palabras normalice los números en una representación canónica mediante el patrón "NN *dd* D *cc",* donde NN es la secuencia literal "NN", *dd* es la parte entera del número, D es el literal "D" y *cc* es la parte fraccionario del número. Los separadores de palabras no restringen el número de dígitos para el entero o la fracción del número. Se recomienda que los separadores de palabras reconozcan patrones numéricos delimitados por puntos (.) y comas (,). Por ejemplo, Windows Search representa "1000.2" y "1.000,2" como "NN1000D2".

Elija un formato para el separador de palabras y el lematizador. Los números árabes de un solo byte se normalizan de forma que una consulta que contiene cualquiera de estos formularios coincide con los documentos con los demás formularios.

Al crear un separador de palabras, se recomienda que el separador de palabras presente todas las veces como una representación de 24 horas con el patrón "TT *hhmmss",* donde TT es el prefijo literal "TT", *hh* son las horas, *mm* son los minutos y *ss* son los segundos. Windows La búsqueda no coincide con unidades de tiempo adicionales, como milisegundos. Análisis de A.M. cono p.m. patterns es opcional.

Al crear un separador de palabras, se recomienda que el separador de palabras genere fechas en el formato canónico "DD *yyyymmdd",* donde DD es el literal "DD", *yyyy* son los años, *mm* son los meses y *dd* son los días. También se recomienda que los separadores de palabras almacenen años de dos dígitos en formatos de siglo xx y XX. Por ejemplo, los separadores de palabras representan "2.2.99" como "DD19990202" y "DD20990202". En el momento de la consulta, Windows Search deriva la fecha mediante interfaces de programación de aplicaciones (API) de Windows para determinar la fecha de cruce para que el servidor muestre el formato correcto, 19 *XX* o 20 *XX.*

## <a name="compound-words"></a>Palabras compuestas

En algunos idiomas, como el alemán, los nombres se suman a partir de nombres más sencillos. Estos nombres compuestos son demasiado específicos en cuanto a la recuperación razonable de consultas. Por ejemplo, sin descomposición, una consulta para "Versseguro" ("seguro") no coincide con "Lebensverscomposiciónsgesellschaft" ("vendedor de seguros de vida"). En casos como este, se recomienda que los separadores de palabras rompan estas palabras compuestas en componentes base durante la creación del índice y el tiempo de consulta. El separador de palabras alemán divide "Lebensversmutsgesellschaft" en las palabras de componente "Leben", "Verscela" y "Gesellschaft". Aplica la misma descomposición en el momento de la consulta, junto con la lematización opcional para cada uno de los términos resultantes.

## <a name="compound-phrases"></a>Frases compuestas

Algunos idiomas, como el coreano, contienen frases complejas que se pueden dividir de varias maneras diferentes. Una frase en coreano consta de palabras de *contenido,* como sustantivos, pronombres, verbos y adjetivos, seguidos de *palabras funcionales*. Las palabras funcionales se encuentran en posiciones posteriores y finales. Las posiciones posteriores indican el rol funcional del sustantivo o pronombre en una oración; Los finales indican el rol funcional del verbo o adjetivo.

Una frase puede tener varios análisis y cada análisis puede constar de varias palabras de contenido. El separador de palabras debe emplear heurística específica del lenguaje para determinar, desde el contexto, cuánto peso se debe dar a los distintos análisis. El separador de palabras puede determinar qué descomposición se debe usar en función del número de palabras de componente resultantes. Algunos separadores de palabras pueden favorecer secuencias cortas de términos más largos, mientras que otros separadores de palabras pueden favorecer secuencias largas de palabras más pequeñas.

Otra consideración es que en coreano, los nombres y pronombres pueden ser almacenados en el índice sin sus palabras funcionales correspondientes. El coreano es un lenguaje aglúcido y combina numerosos finales de palabras con verbos y adjetivos para formar incontables formularios desenfasados. Los verbos y adjetivos identificados en frases se guardan con sus finales en el índice, pero el separador de palabras no genera nuevas formas.

## <a name="special-characters-and-words"></a>Caracteres y palabras especiales

Los caracteres especiales son caracteres como "," "©" y "™". Estos caracteres rara vez se usan en las consultas. Los separadores de palabras deben quitar caracteres especiales durante la creación del índice y en el momento de la consulta.

Se recomienda que los separadores de palabras reconozcan palabras especiales, como "C++", \# "C", ".NET", notas y notación musical. Los separadores de palabras pueden usar un lenguaje heurístico para identificar un patrón para palabras especiales. Los separadores de palabras también pueden usar un diccionario personalizado que contenga palabras especiales reconocidas.

## <a name="acronyms-and-abbreviations"></a>Acrónimos y abreviaturas

Las abreviaturas y acrónimos deben tenerse en cuenta al implementar un separador de palabras. En muchos idiomas, las letras individuales de los acrónimos se separan por puntos. En ocasiones, las palabras que no se reconocen acrónimos o abreviaturas se abrevian. Por ejemplo, "Estados Unidos de Estados Unidos" se puede abreviar como "EE. UU." o "EE. UU.". Los separadores de palabras incluidos con Windows search suelen identificar las palabras de una sola letra como palabras ruidosas y tratar esas palabras como marcadores de posición durante el tiempo de consulta. Durante el tiempo de consulta, un separador de palabras que no conoce acrónimos comunes o que no reconoce abreviaturas convierte la abreviatura "U.S.A". en "U", "S" y "A". Esta descomposición no proporciona suficiente información para coincidir con las palabras del índice de texto completo porque todos los términos de consulta son palabras ruido. Al crear un separador de palabras, se recomienda que el separador de palabras quite los puntos que separan las letras de los acrónimos. En el ejemplo, "U.S.A". se almacena como "EE. UU." y un término de consulta que contiene "EE. UU.". consultas realmente para "EE. UU.". Si un separador de palabras procesa una abreviatura, el período de esa abreviatura no se trata como una interrupción de EOS. Por este problema, es posible que un separador de palabras no identifique correctamente una interrupción de EOS si la abreviatura está al final de la oración.

## <a name="capitalization"></a>Uso de mayúsculas

Windows La búsqueda no conserva actualmente mayúsculas cuando guarda palabras en el índice de texto completo. Los separadores de palabras y lematizadores no deben modificar el caso de las palabras.

## <a name="nonbreaking-spaces"></a>Espacios nobreaking

Al crear un separador de palabras, se recomienda asegurarse de que el separador de palabras trata los espacios sin separación como separadores de palabras. También se recomienda que el separador de palabras genere formas alternativas de la palabra, con y sin espacios de inrroba. Algunos caracteres, como los caracteres de subrayado, son caracteres especiales que se tratan como caracteres nobreaking debido a los orígenes del texto en el que se encuentran. Por ejemplo, el código fuente o los nombres de archivo pueden incluir caracteres de subrayado como caracteres nobreaking.

## <a name="surrogate-pairs"></a>Pares suplentes

Los pares suplentes son representaciones de caracteres en el código fuente que representan un único carácter que consta de una secuencia de dos valores Unicode. En un par codificado, el primer valor es un suplente alto y el segundo es un suplente bajo. Un suplente alto es un carácter del intervalo entre U+D800 y U+DBFF. Un suplente bajo es un carácter del intervalo entre U+DC00 y U+DFFF. Los pares suplentes extienden el juego de caracteres más allá del carácter Unicode. Se recomienda que un separador de palabras use las siguientes reglas al controlar los pares suplentes:

-   Un suplente alto debe preceder a un suplente bajo.
-   Un suplente bajo debe seguir un suplente alto.
-   Un suplente alto o bajo sin un valor correspondiente para su otra mitad no tiene ningún significado.

Los separadores de palabras deben tener en cuenta los pares y generar los pares como tales en el índice. Para obtener más información, [vea Suplentes y caracteres adicionales.](/windows/desktop/Intl/surrogates-and-supplementary-characters)

 

 
