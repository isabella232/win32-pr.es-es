---
description: El predicado CONTAINS admite el uso del asterisco ( \* ) como carácter comodín para representar palabras y frases. Solo puede Agregar el asterisco al final de la palabra o frase. La presencia del asterisco habilita el modo de coincidencia de prefijo.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Usar caracteres comodín en el predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153950"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Usar caracteres comodín en el predicado CONTAINS

El predicado CONTAINS admite el uso del asterisco ( \* ) como carácter comodín para representar palabras y frases. Solo puede Agregar el asterisco al final de la palabra o frase. La presencia del asterisco habilita el modo de coincidencia de prefijo. En este modo, se devuelven coincidencias si la columna contiene la palabra de búsqueda especificada seguida de cero o más caracteres. Si se proporciona una frase, se detectan coincidencias si la columna contiene todas las palabras especificadas con cero o más caracteres que siguen a la palabra final.

## <a name="examples"></a>Ejemplos

En el primer ejemplo se buscan los documentos que tienen cualquier palabra en la columna FileName que empiece por "serv". Entre las palabras coincidentes de ejemplo se incluyen "servidor", "servidores" y "servicio".


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



En el segundo ejemplo se buscan los documentos con cualquier frase en la columna FileName que empiece por "Comp" y en las que la palabra siguiente comience por "serv". Entre las palabras coincidentes de ejemplo se incluyen "servidor de COMP", "servidores de COMP" y "servicio comp".


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



El asterisco solo funciona para la coincidencia de prefijos y solo se puede colocar al final de la palabra o frase; no funciona para la coincidencia de sufijos. La sintaxis siguiente no es válida y no coincide con los documentos que tengan cualquier palabra en la columna FileName que termine en "Serve".


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

 

 



