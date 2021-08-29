---
title: Atributo de puntos DE VML
description: Atributo de puntos DE VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8324bc22459b2991ff6360d661d85a2fcc52a4954d65307d2a5522033b7c0063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057743"
---
# <a name="vml-points-attribute"></a>Atributo de puntos DE VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un conjunto de puntos que forma una polilínea. Lectura/escritura [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .

**Se aplica a**

[Polilínea](msdn-online-vml-polyline-element.md)

**Sintaxis de etiquetas**

<v: *element* points=" *expression* ">

**Sintaxis de script**

*elemento* .points="*expression"".**

*expresión* = *elemento*.points

**Comentarios:**

Define un conjunto de segmentos de línea recta que se componen de una serie de puntos. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es "0,0 10,10". Tenga en cuenta que las comas no son necesarias, pero facilitan la legibilidad.

*Atributo estándar de VML*

**Ejemplo**

La polilínea comienza en el punto 10,10 y termina en 100 100, con los valores de los puntos.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 