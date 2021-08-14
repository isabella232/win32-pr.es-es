---
description: Aunque las palabras y las reglas lingüísticas difieren drásticamente, hay algunas consideraciones, como números, fechas y horas, que se controlan de forma coherente en todos los separadores de palabras.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalización de formularios surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862439"
---
# <a name="surface-form-normalization"></a>Normalización de formularios surface

Aunque las palabras y las reglas lingüísticas difieren drásticamente, hay algunas consideraciones, como números, fechas y horas, que se controlan de forma coherente en todos los separadores de palabras. En este tema se documenta las consideraciones de normalización que pueden afectar a la implementación del separador de palabras.

Este tema se organiza de la siguiente manera:

-   [Etimología](#hyphenation)
-   [Posesivos](#possessives)
-   [Diacríticos](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>Etimología

Los guiones (-) se usan entre las partes de una palabra o un nombre compuestos. También se usan entre las sílabas de una palabra cuando la palabra se divide al final de una línea de texto. En inglés, las palabras se unen con guiones para indicar una relación especial en el contexto, pero es posible que esas palabras no se guionen normalmente en otros contextos; por ejemplo, "paso a paso". Durante la creación del índice, el separador de palabras debe tratar el guion como separador de palabras. Por ejemplo, "base de datos" se almacenaría como "datos" más "base". En el momento de la consulta, una frase con guion debe reemplazarse por dos alternativas: la variante de dos palabras y el compuesto verdadero. Por ejemplo, "base de datos" se reemplazaría por "datos" más "base" y "base de datos". Esta diferencia entre el índice y el tiempo de consulta aumenta las combinaciones de representaciones para palabras con guiones y facilita la coincidencia de las palabras en una consulta.

En la tabla siguiente se muestra cómo el tratamiento de guiones como separadores de palabras en el idioma inglés aumenta el número de términos de consulta coincidentes para cada término incluido en el índice.



| Términos incluidos en el índice | Coincidencias en tiempo de consulta   |
|-----------------------------|----------------------|
| Base de datos                   | base de datos, base de datos |
| Base de datos                   | base de datos, base de datos |
| Base de datos                    | base de datos, base de datos  |



 

## <a name="possessives"></a>Posesivos

Los posesivos son variaciones en un sustantivo que indican la posesión. Los posesivos de inglés se representan anexando un apóstrofo (') o un apóstrofo y un (s) a una palabra. Por ejemplo, para indicar la posesión, la palabra "Mary" se representa como "Mary". El separador de palabras genera los formularios apóstrofo y apóstrofo en el momento de la consulta. Las consultas de "Mary" deben coincidir con "Mary" y "Mary's".

## <a name="diacritics"></a>Marcas diacríticas

Los signos diacríticos son marcas que se agregan a una letra o phonema para indicar un valor fonético especial para la pronunciación. Los signos diacríticos pueden distinguir palabras que, de lo contrario, son gráficamente idénticas; por ejemplo, "resume" y "resumé" en inglés. Sin embargo, guardar signos diacríticos en el índice aumenta el número de claves de palabras únicas en el índice, lo que ralentiza el rendimiento de las consultas. Si los signos diacríticos solo se usan mínimamente en un idioma, el separador de palabras de ese idioma debe quitarlos durante la creación de índices y las consultas. Por ejemplo, el separador de palabras en inglés genera "resume" al procesar "resumé", lo que solo tiene un impacto mínimo en la relevancia de los resultados de la consulta.

## <a name="clitics"></a>Clitics

Un clítico es una palabra sinstres que no es capaz de posiciones por sí misma y se asocia a una palabra estresada para formar una sola unidad. Los clíticos no se pueden clasificar fácilmente como fonológicos, sintácticos o morphológicos. Las clitics se incluyen en dos tipos: *proclitics* y *enclitics.* Los prolíticos se asocian al principio de una palabra. Los clíticos se asocian al final de una palabra.

Los clíticos son más difíciles de analizar en idiomas como el español. Un verbo español puede generar muchas formas de superficie, dependiendo del tiempo. Se deben tener en cuenta las consideraciones entre quitar el clitic durante la creación del índice y generar los formularios de superficie a través de la lematización en el momento de la consulta. La eliminación de clitics en casos en los que la morfología de la composición clitética es ambigua puede dar lugar a resultados impredecibles. La generación de un gran número de formas de superficie para una palabra aumenta el tamaño del índice de texto completo y puede ralentizar el rendimiento de las consultas. Se recomienda que el lematizador genere solo un pequeño número de formas de superficie.

 

 



