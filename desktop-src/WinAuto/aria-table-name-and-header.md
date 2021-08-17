---
title: Error de tabla de datos de ARIA
description: Error de tabla de datos de ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025443ab452ff0103c8808c27dce834a03cb8c96e0d9106a7abb4409b64a0697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133978"
---
# <a name="aria-data-table-error"></a>Error de tabla de datos de ARIA

## <a name="text"></a>Texto

La tabla contiene datos, pero no tiene marcado accesible definido a través de los elementos **aria-label**, **aria-labelledby**, **title**, **caption** **o th.**

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a las tablas HTML con más de una celda. Este error no se aplica a las tablas con porque se `role="presentation"` consideran tablas de diseño.

Este error indica que una tabla de datos no tiene un nombre o información de encabezado accesibles.

Para corregir este error, defina un nombre accesible mediante la etiqueta [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) o los atributos [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title.**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Si falta información de encabezado en la tabla, use [**etiquetas THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar las celdas de encabezado.

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



 

 




