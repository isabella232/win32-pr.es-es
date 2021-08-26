---
title: Error de tabla de presentación de ARIA
description: Error de tabla de presentación de ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896c7ec4061119535ed544cfc41598c1387d98011eb275f6a0345d9334a7dc9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122294"
---
# <a name="aria-presentation-table-error"></a>Error de tabla de presentación de ARIA

## <a name="text"></a>Texto

La tabla usada para el diseño no debe tener definidos el encabezado, el nombre accesible ni la información de resumen (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a las etiquetas de tabla HTML que tienen el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) establecido en "presentation" o con una tabla que tiene una sola celda (1×1 tabla).

Este error indica que una tabla está marcada solo como diseño (tiene ), pero también contiene información de accesibilidad como si fuera una tabla de datos, lo que puede resultar confuso para los usuarios del lector `role="presentation"` de pantalla.

Para solucionar este error, determine si la tabla es realmente solo una tabla de diseño y, si es así, quite el marcado accesible:

-   [**Elemento CAPTION,**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) [**aria-labelledby,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o atributos [**de**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) título.
-   [**atributos de resumen**](https://www.bing.com/search?q=**summary**) [**o aria-describedby.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)
-   [**Etiquetas THEAD.**](https://developer.mozilla.org/docs/Web/HTML/Element/thead)

## <a name="example"></a>Ejemplo

![html para un elemento de tabla, con atributos como el resumen que desencadenan el error de la tabla de presentación aria que se muestra como marcado HTML desenlazador ](images/aria-layout-table.png)

## <a name="remarks"></a>Comentarios

Si determina que una tabla necesita información de accesibilidad, quite el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) o establezca en un valor distinto de "presentation".

 

 




