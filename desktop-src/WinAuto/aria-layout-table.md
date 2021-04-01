---
title: Error de tabla de presentación de ARIA
description: Error de tabla de presentación de ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797091"
---
# <a name="aria-presentation-table-error"></a>Error de tabla de presentación de ARIA

## <a name="text"></a>Texto

La tabla usada para el diseño no debe tener el encabezado, el nombre accesible o la información de Resumen definida (**TH**, **Summary**, **Aria-describedby**, **Aria-labelledby**, **Aria-Label**, **title**, **Caption** ).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a las etiquetas de la tabla HTML que tienen el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) establecido en "Presentation" o con una tabla que tiene una sola celda (1 x 1 tabla).

Este error indica que una tabla está marcada únicamente como diseño (tiene `role="presentation"` ), pero también contiene información de accesibilidad como si fuera una tabla de datos, lo que puede resultar confuso para los usuarios del lector de pantalla.

Para solucionar este error, determine si la tabla es realmente simplemente una tabla de diseño y, si es así, quite el marcado accesible:

-   Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Attributes.
-   los atributos [**Summary**](https://www.bing.com/search?q=**summary**) o [**Aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .
-   Etiquetas [**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .

## <a name="example"></a>Ejemplo

![HTML para un elemento de tabla, con atributos como Summary que desencadenan el error de tabla de presentación de Aria mostrado como marcado HTML de tachado ](images/aria-layout-table.png)

## <a name="remarks"></a>Observaciones

Si determina que una tabla necesita información de accesibilidad, quite el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) o establézcalo en un valor distinto de "Presentation".

 

 




