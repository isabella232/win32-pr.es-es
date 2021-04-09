---
description: En este tema se describen las consideraciones sobre la lematización para los lenguajes agglutinative y los pares suplentes de Unicode, y para usar pares suplentes para extender el juego de caracteres Unicode para alojar distintos juegos de caracteres.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Consideraciones lingüísticas y Unicode misceláneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433fb212917f29acbc2347c3324668a77533dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082012"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Consideraciones lingüísticas y Unicode misceláneas

En este tema se describen las consideraciones sobre la lematización para los lenguajes agglutinative y los pares suplentes de Unicode, y para usar pares suplentes para extender el juego de caracteres Unicode para alojar distintos juegos de caracteres. En este tema también se describe el modo en que los separadores de palabras identifican frases en el texto y controlan los espacios de no separación y la forma en que los separadores de palabras y lematizadores controlan los números y las fechas, palabras compuestas, frases compuestas, palabras y caracteres especiales, acrónimos y abreviaturas, y uso

Este tema se organiza de la siguiente manera:

-   [Identificación de la frase](#phrase-identification)
-   [Lenguajes Agglutinative](#agglutinative-languages)
-   [Números, horas y fechas](#numbers-times-and-dates)
-   [Palabras compuestas](#compound-words)
-   [Frases compuestas](#compound-phrases)
-   [Caracteres especiales y palabras](#special-characters-and-words)
-   [Acrónimos y abreviaturas](#acronyms-and-abbreviations)
-   [Uso de mayúsculas](#capitalization)
-   [Espacios de no separación](#nonbreaking-spaces)
-   [Pares suplentes](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificación de la frase

Las frases son una palabra o un grupo de palabras modificadas por uno o más usuarios. Las frases son difíciles de identificar de forma coherente, ya que se puede usar el mismo modificador en más de una frase con el mismo nombre. Por ejemplo, "New House", "House of Parlamento", "New House of Parlamento".

Windows Search usa frases con mayor frecuencia en el momento de la consulta. Las frases del texto de consulta reciben un peso mayor que las palabras individuales. En el ejemplo anterior, un documento que contenga "House of Parlamento" tiene una clasificación superior a la que contiene "House" y "Parlamento" en distintos puntos del documento. Se recomienda que los separadores de palabras generen una frase en el momento de la consulta si es probable que la frase coincida con al menos un documento.

## <a name="agglutinative-languages"></a>Lenguajes Agglutinative

Los lenguajes Agglutinative forman palabras a través de la combinación de morfemas más pequeños para expresar ideas compuestas. Cada uno de estos morfemas generalmente tiene un significado o una función y conserva su forma original y su significado durante el proceso de combinación. En el caso de los idiomas que tienen morfología agglutinative, como turco, finés, Húngaro o coreano, es posible generar miles de formularios para una palabra raíz determinada.

En la tabla siguiente se muestra una lista de formas derivadas de la palabra "Talo" ("House") de finés.



| Word      | Traducción   |
|-----------|---------------|
| Talo      | Casa         |
| Taloni    | Mi casa      |
| Talossa   | En la casa  |
| Talossani | En mi casa   |
| Taloja    | Empresas        |
| Taloissa  | En las casas |



 

Los idiomas que se derivan, como inglés, francés y latín, tienen un número muy pequeño de formas de Word posibles para una palabra raíz. En los lenguajes transpuestos, morfemas influye en otro al enlazar. La mayoría de los cambios en la inflexión están presentes en el extremo o en el final de la palabra. A diferencia de los lenguajes agglutinative, los lenguajes declinados tienden a tener distintas funciones para un solo morpheme. Por ejemplo, un morpheme puede determinar tanto el número como el uso de mayúsculas y minúsculas.

Lematizadores para los lenguajes agglutinative debe sopesar el equilibrio entre el rendimiento y la precisión para generar solo un subconjunto del número de formas posibles de Word.

## <a name="numbers-times-and-dates"></a>Números, horas y fechas

Los separadores de palabras deben utilizar un formato común para representar números, horas y fechas para facilitar una consulta coherente.

Cuando se crea un separador de palabras, se recomienda que el separador de palabras normalice los números en una representación canónica mediante el patrón "NN *DD* D *CC*", donde NN es la secuencia literal "NN", *DD* es la parte entera del número, D es el literal "D" y *CC* es la parte fraccionaria del número. Los separadores de palabras no restringen el número de dígitos para el entero o la parte de fracción del número. Se recomienda que los separadores de palabras reconozcan patrones numéricos delimitados por puntos (.) y comas (,). Por ejemplo, la búsqueda de Windows representa "1.000,2" y "1.000", "NN1000D2".

Elija un formato para el separador de palabras y el analizador lingüístico. Los números arábigos de un solo byte se normalizan de modo que una consulta que contenga cualquiera de estos formularios coincida con los documentos con los demás formularios.

Al crear un separador de palabras, se recomienda que el separador de palabras presente todo el tiempo como una representación de 24 horas con el patrón "TT *HHMMSS*", donde TT es el prefijo literal "TT", *HH* es las horas, *mm* es el minuto y *SS* es el segundo. Windows Search no coincide con otras unidades de tiempo, como milisegundos. Analizar A.M. cono p.m. Patterns es opcional.

Cuando se crea un separador de palabras, se recomienda que el separador de palabras genere fechas en el formato canónico de "DD *AAAAMMDD*", donde DD es el literal "DD", *AAAA* es el año, *mm* es el mes y *DD* es el día. También se recomienda que los separadores de palabras almacenen años de dos dígitos en los formatos del siglo veinte y del vigésimo primero. Por ejemplo, los separadores de palabras representan "2.2.99" como "DD19990202" y "DD20990202". En el momento de la consulta, Windows Search deriva la fecha mediante interfaces de programación de aplicaciones (API) de Windows para determinar la fecha de convergencia del servidor con el fin de mostrar el formato correcto, 19 *XX* ó 20 *XX*.

## <a name="compound-words"></a>Palabras compuestas

En algunos idiomas, como el alemán, los nombres se comparten de nombres más sencillos. Estos nombres compuestos son demasiado específicos en lo que se refiere a una recuperación de consultas razonable. Por ejemplo, sin la descomposición, una consulta de "Versicherung" ("Insurance") no coincide con "Lebensversicherungsgesellschaft" ("Life-Insurance sales"). En casos como este, se recomienda que los separadores de palabras interrumpan estas palabras compuestas en componentes base durante la creación del índice y el tiempo de la consulta. El separador de palabras en alemán divide "Lebensversicherungsgesellschaft" en las palabras del componente "Leben", "Versicherung" y "Gesellschaft". Aplica la misma descomposición en el momento de la consulta, junto con una lematización opcional para cada uno de los términos resultantes.

## <a name="compound-phrases"></a>Frases compuestas

Algunos idiomas, como el coreano, contienen frases complejas que pueden dividirse de varias maneras. Una frase en Coreano consta de *palabras de contenido*, como sustantivos, pronombres, verbos y adjetivos, seguidas de *palabras funcionales*. Las palabras funcionales se encuentran en las posiciones posteriores y los finales. Las posiciones posteriores indican el rol funcional del nombre o pronombres en una oración; los fines de finalización indican el rol funcional del verbo o adjetivo.

Una frase puede tener los distintos análisis y cada análisis puede constar de varias palabras de contenido. El separador de palabras debe emplear la heurística específica del lenguaje para determinar, desde el contexto, la cantidad de peso que se va a dar a distintos análisis. El separador de palabras puede determinar la descomposición que se va a usar en función del número de palabras del componente resultante. Algunos separadores de palabras pueden favorecer secuencias cortas de términos más largos, mientras que otros separadores de palabras pueden favorecer grandes secuencias de palabras más pequeñas.

Otra consideración es que, en Coreano, los nombres y los pronombres pueden estar almacenados en el índice sin sus palabras funcionales correspondientes. El coreano es un lenguaje agglutinative y combina numerosos finales de palabras con verbos y adjetivos para formar innumerables formas derivadas. Los verbos y adjetivos identificados en frases se guardan con sus finales en el índice, pero el separador de palabras no genera nuevos formularios.

## <a name="special-characters-and-words"></a>Caracteres especiales y palabras

Los caracteres especiales son caracteres como "," "©" y "™". Estos caracteres rara vez se utilizan en las consultas. Los separadores de palabras deben quitar los caracteres especiales durante la creación del índice y en el momento de la consulta.

Se recomienda que los separadores de palabras reconozcan palabras especiales, como "C++", "C", ".net", \# calificaciones y notación musical. Los separadores de palabras pueden utilizar una heurística de idioma para identificar un patrón para palabras especiales. Los separadores de palabras también pueden usar un diccionario personalizado que contenga palabras especiales reconocidas.

## <a name="acronyms-and-abbreviations"></a>Acrónimos y abreviaturas

Los acrónimos y las abreviaturas se deben tener en cuenta al implementar un separador de palabras. En muchos idiomas, las letras individuales de los acrónimos están separadas por puntos. En ocasiones, se abrevian las palabras que no se reconocen como acrónimos o abreviaturas. Por ejemplo, "Estados Unidos de America" se puede abreviar como "EE. UU." o "Estados Unidos" Los separadores de palabras incluidos en Windows Search normalmente identifican las palabras de una letra como palabras irrelevantes y las tratan como marcadores de posición durante el tiempo de consulta. Durante el tiempo de consulta, un separador de palabras que no es consciente de los acrónimos comunes o que no reconoce las abreviaturas convierte la abreviatura en "U.S.A." en "U", "S" y "A". Esta descomposición no proporciona suficiente información para buscar palabras en el índice de texto completo porque todos los términos de la consulta son palabras irrelevantes. Al crear un separador de palabras, se recomienda que el separador de palabras Quite los puntos que separan las letras de los acrónimos. En el ejemplo, "U.S.A." se almacena como "EE. UU." y un término de consulta que contiene "U.S.A." en realidad, consulta "EE. UU.". Si un separador de palabras procesa una abreviatura, el punto de esa abreviatura no se trata como una interrupción de EOS. Por este motivo, es posible que un separador de palabras no identifique correctamente una interrupción de EOS si la abreviatura está al final de la frase.

## <a name="capitalization"></a>Uso de mayúsculas

Windows Search no conserva actualmente las mayúsculas y minúsculas cuando guarda palabras en el índice de texto completo. Los separadores de palabras y lematizadores no deben modificar las mayúsculas y minúsculas de las palabras.

## <a name="nonbreaking-spaces"></a>Espacios de no separación

Al crear un separador de palabras, se recomienda asegurarse de que el separador de palabras trata los espacios de no separación como separadores de palabras. También se recomienda que el separador de palabras genere formas alternativas de la palabra, con y sin espacios de no separación. Algunos caracteres, como los caracteres de subrayado, son caracteres especiales que se tratan como caracteres sin interrupción debido a los orígenes del texto en el que se encuentran. Por ejemplo, el código fuente o los nombres de archivo pueden incluir caracteres de subrayado como caracteres sin interrupción.

## <a name="surrogate-pairs"></a>Pares suplentes

Los pares suplentes son representaciones de caracteres en el código fuente que representan un único carácter que consta de una secuencia de dos valores Unicode. En un par codificado, el primer valor es un suplente alto y el segundo es un suplente bajo. Un suplente alto es un carácter en el intervalo de U + D800 a U + DBFF. Un suplente bajo es un carácter en el intervalo de U + DC00 a U + DFFF. Los pares suplentes amplían el juego de caracteres más allá del carácter Unicode. Se recomienda que un separador de palabras use las siguientes reglas al controlar los pares suplentes:

-   Un suplente alto debe preceder a un suplente bajo.
-   Un suplente bajo debe seguir a un suplente alto.
-   Un suplente alto o bajo sin un valor correspondiente para la otra mitad no tiene ningún significado.

Los separadores de palabras deben tener en cuenta cualquier par y generar los pares como tal en el índice. Para obtener más información, vea [suplentes y caracteres adicionales](/windows/desktop/Intl/surrogates-and-supplementary-characters).

 

 
