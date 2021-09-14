---
description: El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tienen un patrón específico en un desplazamiento específico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Escribir el filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245091"
---
# <a name="writing-the-patternmatch-filter"></a>Escribir el filtro PATTERNMATCH

El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tienen un patrón específico en un desplazamiento específico. Puede especificar un máximo de cuatro coincidencias de patrón detalladas, que se pueden combinar en instrucciones AND u OR lógicas para la evaluación Monitor de red controlador.

Para implementar coincidencias de patrón, use las siguientes Monitor de red estructura:

-   [**EXPRESIÓN**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

Para evaluar una **instrucción OR,** combinar dos a cuatro patrones coincide con una [**estructura ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Para evaluar una instrucción AND, combine entre una y cuatro estructuras **ANDEXP** y una estructura [**EXPRESSION**](expression.md) (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Definiciones de coincidencia de patrones

La estructura [**PATTERNMATCH**](patternmatch.md) define una coincidencia de patrón única. Una coincidencia individual puede funcionar de una de estas dos maneras.

Normalmente, el controlador toma la base de desplazamiento (que puede ser OFFSET \_ BASIS \_ RELATIVE TO \_ \_ FRAME, OFFSET BASIS RELATIVE \_ TO EFFECTIVE \_ \_ \_ \_ PROTOCOL, OFFSET BASIS RELATIVE TO IPX o \_ OFFSET BASIS RELATIVE TO \_ \_ \_ \_ \_ \_ \_ IP) y empieza a contar allí. El controlador cuenta los bytes de desplazamiento desde allí y, a continuación, hace coincidir los datos que encuentra con los primeros bytes de longitud **en PatternToMatch**. Si son iguales y no se establece la marca PATTERN \_ MATCH \_ FLAGS \_ NOT, este patrón pasa. Si son diferentes y PATTERN \_ MATCH \_ FLAGS \_ NOT se ha establecido, el patrón pasa. De lo contrario, se produce un error en este patrón.

O:

Si se establece la marca PATTERN MATCH FLAGS PORT SPECIFIED y la base se establece en OFFSET BASIS RELATIVE TO IPX o OFFSET BASIS RELATIVE TO IP, la comparación \_ \_ es \_ más \_ \_ \_ \_ \_ \_ \_ \_ \_ compleja. En primer lugar, el controlador garantiza que el protocolo de base de desplazamiento está ahí y, a continuación, comprueba que el puerto especificado coincide con el puerto del marco. Por último, el controlador garantiza que el miembro **PatternToMatch** coincide como antes, con la excepción de que el desplazamiento es desde el final de IP o IPX. Tenga en cuenta que si la base no es una de estas dos, se omitirá la marca PATTERN MATCH FLAGS PORT SPECIFIED y el patrón se evaluará como se ha \_ \_ indicado \_ \_ anteriormente.

Para evaluar una coincidencia de patrón única, una [**estructura EXPRESSION**](expression.md) debe tener un **miembro AndExp** que contenga una coincidencia de patrón única.

La creación del filtro de coincidencia de patrones implica crear estructuras [**PATTERNMATCH**](patternmatch.md) y combinarlas lógicamente con [**estructuras EXPRESSION**](expression.md) [**y ANDEXP.**](andexp.md)

**Para escribir un filtro PATTERNMATCH**

1.  En la [**estructura ANDEXP,**](andexp.md) rellene la matriz con coincidencias de patrón.
2.  Rellene la [**estructura EXPRESSION**](expression.md) con una matriz de **miembros AndExp.**
3.  No supere un total de cuatro coincidencias de patrón para el filtro de captura.
4.  En la [**estructura PATTERNMATCH,**](patternmatch.md) seleccione un tipo de marca.
5.  Seleccione una base de desplazamiento.
6.  Enumerar un valor de puerto.
7.  Defina el valor de desplazamiento.
8.  Defina la longitud del patrón.
9.  Enumerar el valor del patrón.

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

Este marco muestra un desplazamiento especificado por puerto (en ipx).

![marco de desplazamiento especificado por puerto](images/stan-pat.png)

El código de ejemplo se implementa como:

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



