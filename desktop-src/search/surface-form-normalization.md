---
description: Aunque las reglas lingüísticas y de palabras se diferencian drásticamente, hay algunas consideraciones, como números, fechas y horas, que se tratan de forma coherente en todos los separadores de palabras.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalización del formulario de superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b058be00e046ffc17ebd6c13178313267a47079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153931"
---
# <a name="surface-form-normalization"></a>Normalización del formulario de superficie

Aunque las reglas lingüísticas y de palabras se diferencian drásticamente, hay algunas consideraciones, como números, fechas y horas, que se tratan de forma coherente en todos los separadores de palabras. En este tema se documentan las consideraciones de normalización que pueden afectar a la implementación del separador de palabras.

Este tema se organiza de la siguiente manera:

-   [División](#hyphenation)
-   [Posesivos](#possessives)
-   [Diacríticos](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>División

Los guiones (-) se usan entre las partes de una palabra compuesta o nombre. También se usan entre las sílabas de una palabra cuando la palabra se divide al final de una línea de texto. En inglés, las palabras se unen con guiones para indicar una relación especial en contexto, pero es posible que esas palabras no estén normalmente en otros contextos. por ejemplo, "paso a paso". Durante la creación del índice, el separador de palabras debe tratar el guión como separador de palabras. Por ejemplo, "Data-base" se almacenaría como "Data" más "base". En el momento de la consulta, una frase con guiones debe reemplazarse por dos alternativas: la variante de dos palabras y el compuesto verdadero. Por ejemplo, "Data-base" se reemplazaría por "Data" más "base" y "Database". Esta diferencia entre el tiempo de índice y de consulta aumenta las combinaciones de representaciones para las palabras con guiones y hace que las palabras sean más fáciles de buscar en una consulta.

En la tabla siguiente se muestra cómo tratar los guiones como separadores de palabras en el idioma inglés aumenta el número de términos de consulta coincidentes para cada término incluido en el índice.



| Términos incluidos en el índice | Coincidencia en tiempo de consulta   |
|-----------------------------|----------------------|
| Base de datos                   | base de datos, base de datos |
| Base de datos                   | base de datos, base de datos |
| Base de datos                    | base de datos, base de datos  |



 

## <a name="possessives"></a>Posesivos

Los Possessive son variaciones en un nombre que indica la posesión. Los español se representan mediante la anexión de un apóstrofo (') o un apóstrofo, y de una (s) a una palabra. Por ejemplo, para indicar la posesión, la palabra "Mary" se representa como "María". El separador de palabras genera el apóstrofo y los formularios de apóstrofos en el momento de la consulta. Las consultas de "Mary" deben coincidir con "María" y "María".

## <a name="diacritics"></a>Marcas diacríticas

Los signos diacríticos se agregan a una letra o a un fonema para indicar un valor fonético especial para la pronunciación. Los signos diacríticos pueden distinguir palabras que, en caso contrario, son idénticas de forma gráfica. por ejemplo, "resume" y "resumé" en inglés. Sin embargo, el almacenamiento de diacríticos en el índice aumenta el número de claves de palabra únicas en el índice, lo que ralentiza el rendimiento de las consultas. Si los diacríticos solo se usan de forma mínima en un lenguaje, el separador de palabras de ese idioma debe quitarlos durante la creación y la consulta de índices. Por ejemplo, el separador de palabras en inglés genera "resume" al procesar "resumé", con lo que solo se produce un impacto mínimo en la relevancia de los resultados de la consulta.

## <a name="clitics"></a>Clitics

Un clitic es una palabra desacentuada que no es capaz de estar en su propio y se adjunta a una palabra con estrés para formar una sola unidad. Clitics no se puede clasificar fácilmente como phonological, sintáctica o morfológico. Clitics se presentan en dos tipos: *proclitics* y *enclitics*. Proclitics adjuntarse al principio de una palabra. Enclitics adjuntarse al final de una palabra.

Clitics son más difíciles de analizar en lenguajes como el español. Un verbo Español puede generar muchas formas de superficie, dependiendo del pasado. Se deben tener en cuenta las consideraciones entre quitar el clitic durante la creación del índice y generar los formularios de la superficie mediante la lematización en el momento de la consulta. La eliminación de clitics en los casos en los que la morfología de la composición clitic es ambigua puede producir resultados imprevisibles. La generación de un gran número de formas de superficie para una palabra aumenta el tamaño del índice de texto completo y puede ralentizar el rendimiento de las consultas. Se recomienda que el analizador lingüístico genere solo un pequeño número de formularios de superficie.

 

 



