---
title: Error de la tabla de datos ARIA
description: Error de la tabla de datos ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421533"
---
# <a name="aria-data-table-error"></a>Error de la tabla de datos ARIA

## <a name="text"></a>Texto

La tabla contiene datos, pero no tiene marcado accesible definido a través de los elementos **Aria-Label**, **Aria-labelledby**, **title**, **Caption** o **TH** .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a las tablas HTML con más de una celda. Este error no se aplica a las tablas con `role="presentation"` porque se consideran tablas de diseño.

Este error indica que una tabla de datos no tiene un nombre accesible o información de encabezado.

Para corregir este error, defina un nombre accesible mediante la etiqueta de [**título**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) o los atributos [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) . Si falta información de encabezado en la tabla, use etiquetas [**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar las celdas de encabezado.

## <a name="example"></a>Ejemplo


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




