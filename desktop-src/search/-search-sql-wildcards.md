---
description: El predicado CONTAINS admite el uso del asterisco ( ) como carácter \* comodín para representar palabras y frases. Solo puede agregar el asterisco al final de la palabra o frase. La presencia del asterisco habilita el modo de coincidencia de prefijos.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Usar caracteres comodín en el predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760a9b4b8dae1392bf5590639775ba1b4fe534c99120322c05cc16432c1fa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944565"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Usar caracteres comodín en el predicado CONTAINS

El predicado CONTAINS admite el uso del asterisco ( ) como carácter \* comodín para representar palabras y frases. Solo puede agregar el asterisco al final de la palabra o frase. La presencia del asterisco habilita el modo de coincidencia de prefijos. En este modo, se devuelven coincidencias si la columna contiene la palabra de búsqueda especificada seguida de cero o más caracteres. Si se proporciona una frase, se detectan coincidencias si la columna contiene todas las palabras especificadas con cero o más caracteres después de la palabra final.

## <a name="examples"></a>Ejemplos

El primer ejemplo coincide con documentos que tienen cualquier palabra en la columna FileName que comienza por "serv". Entre las palabras que coinciden de ejemplo se incluyen "servidor", "servidores" y "servicio".


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



El segundo ejemplo coincide con documentos con cualquier frase de la columna FileName que comienza por "comp" y en la que la palabra siguiente comienza por "serv". Entre las palabras que coinciden de ejemplo se incluyen "comp server", "comp servers" y "comp service".


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



El asterisco solo funciona para la coincidencia de prefijos y solo se puede colocar al final de la palabra o frase; no funciona para la coincidencia de sufijos. La sintaxis siguiente no es válida y no coincide con los documentos con ninguna palabra de la columna FileName que termine con "serve".


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



