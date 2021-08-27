---
title: Advertencia de la tabla de datos ARIA
description: Advertencia de la tabla de datos ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fb9e8e97336199b5b133dc59ef7c5f0900f7bdeb0c7a8d8098a51707b107f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122395"
---
# <a name="aria-data-table-warning"></a>Advertencia de la tabla de datos ARIA

## <a name="text"></a>Texto

La tabla contiene datos, pero no tiene un resumen ni un **atributo aria-describedby** válido.

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

Esta advertencia se aplica a las tablas HTML con más de una celda. No se aplica a las tablas con, ya que se consideran `role="presentation"` tablas de diseño.

Esta advertencia indica que la tabla se identifica como una tabla de datos, pero no tiene definida una descripción accesible.

> [!Note]  
> No todas las tablas de datos deben tener una descripción accesible. Debe definir una descripción accesible si los usuarios necesitan más información para comprender la estructura y el contenido de la tabla de datos.

 

Para solucionar esta advertencia, defina una descripción accesible de tabla mediante el atributo summary o **el atributo aria-describedby.**

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



 

 




