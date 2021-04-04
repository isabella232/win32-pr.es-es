---
title: ADVERTENCIA de la tabla de datos ARIA
description: ADVERTENCIA de la tabla de datos ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076244"
---
# <a name="aria-data-table-warning"></a>ADVERTENCIA de la tabla de datos ARIA

## <a name="text"></a>Texto

La tabla contiene datos, pero no tiene ningún Resumen ni un atributo **Aria-describedby** válido.

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

Esta advertencia se aplica a las tablas HTML con más de una celda. No se aplica a las tablas con `role="presentation"` , ya que se consideran tablas de diseño.

Esta advertencia indica que la tabla se identifica como una tabla de datos, pero no tiene definida una descripción accesible.

> [!Note]  
> No es necesario que todas las tablas de datos tengan una descripción accesible. Debe definir una descripción accesible si los usuarios necesitan más información para entender la estructura y el contenido de la tabla de datos.

 

Para solucionar esta advertencia, defina una descripción accesible de tabla mediante el atributo Summary o el atributo **Aria-describedby** .

## <a name="example"></a>Ejemplo


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




