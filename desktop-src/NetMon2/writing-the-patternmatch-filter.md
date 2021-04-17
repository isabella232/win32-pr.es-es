---
description: El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tengan un patrón específico en un desplazamiento específico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Escribir el filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677666"
---
# <a name="writing-the-patternmatch-filter"></a>Escribir el filtro PATTERNMATCH

El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tengan un patrón específico en un desplazamiento específico. Puede especificar un máximo de cuatro coincidencias de patrones detalladas, que se pueden combinar en instrucciones AND o or lógicas para Monitor de red evaluación de controladores.

Para implementar coincidencias de patrones, utilice las siguientes estructuras de Monitor de red:

-   [**Expresiones**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

Para evaluar una instrucción **o** , combine dos a cuatro patrones que coincida con una estructura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Para evaluar una instrucción y, combine una a cuatro estructuras **ANDEXP** y una estructura [**EXPRESSION**](expression.md) (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Definiciones de coincidencia de patrones

La estructura [**PATTERNMATCH**](patternmatch.md) define una coincidencia de patrón única. Una coincidencia individual puede funcionar de una de estas dos maneras.

Normalmente, el controlador tomará la base de desplazamiento (que puede estar desplazada en relación con el \_ \_ \_ \_ marco, la base de desplazamiento \_ \_ \_ en relación con el \_ \_ Protocolo efectivo, la \_ base de desplazamiento \_ \_ en relación con \_ IPX o la \_ base de desplazamiento \_ con respecto \_ a la \_ dirección IP) e iniciar el recuento allí. El controlador contará los bytes de desplazamiento desde allí y, después, coincidirá con los datos que encuentre con los bytes de primera longitud de **PatternToMatch**. Si son iguales y \_ no se establecen las marcas de coincidencia de patrones \_ \_ no marcadas, se pasa este patrón. Si son diferentes y \_ no se han establecido las marcas de coincidencia de patrones, se \_ \_ pasa el patrón. En caso contrario, se produce un error en este patrón.

O:

Si \_ se establece la marca de marcas de coincidencia de patrones \_ \_ \_ especificada y la base se establece en desplazamiento de base con respecto a la base de \_ \_ \_ \_ IPX o de desplazamiento \_ \_ con respecto \_ a \_ la dirección IP, la comparación es más compleja. En primer lugar, el controlador garantiza que el protocolo de base de desplazamiento está ahí, el controlador comprueba que el puerto especificado coincida con el puerto del marco. Por último, el controlador garantiza que el miembro **PatternToMatch** coincide como antes, con la excepción de que el desplazamiento es del final de IP o IPX. Tenga en cuenta que si la base no es una de estas dos, se \_ omitirá el indicador de marcas de coincidencia de patrones \_ \_ \_ especificado y el patrón se evaluará como se ha indicado anteriormente.

Para evaluar una coincidencia de patrón única, una estructura de [**expresión**](expression.md) debe tener un miembro **AndExp** que contenga una coincidencia de patrón única.

La creación del filtro de coincidencia de patrones implica la creación de estructuras [**PATTERNMATCH**](patternmatch.md) y su combinación lógica con las estructuras [**Expression**](expression.md) y [**ANDEXP**](andexp.md) .

**Para escribir un filtro de PATTERNMATCH**

1.  En la estructura [**ANDEXP**](andexp.md) , rellene la matriz con coincidencias de patrones.
2.  Rellene la estructura de [**expresión**](expression.md) con una matriz de miembros de **AndExp** .
3.  No supere un total de cuatro coincidencias de patrón para el filtro de captura.
4.  En la estructura [**PATTERNMATCH**](patternmatch.md) , seleccione un tipo de marca.
5.  Seleccione una base de desplazamiento.
6.  Enumerar un valor de puerto.
7.  Defina el valor de desplazamiento.
8.  Defina la longitud del patrón.
9.  Enumera el valor del patrón.

## <a name="patternmatch-examples"></a>Ejemplos de PATTERNMATCH

Este marco representa un desplazamiento estándar.

![marco de desplazamiento estándar](images/offs-pat.png)

El fragmento de código se implementa como:

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

Este marco representa un desplazamiento especificado por el puerto (contra IPX).

![marco de desplazamiento especificado por el puerto](images/stan-pat.png)

El código de ejemplo se implementa como:

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



