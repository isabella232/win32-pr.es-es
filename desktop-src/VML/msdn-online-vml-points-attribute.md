---
title: Atributo de puntos VML
description: Atributo de puntos VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077847"
---
# <a name="vml-points-attribute"></a>Atributo de puntos VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un conjunto de puntos que forman una polilínea. Lectura/escritura [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .

**Se aplica a**

[Polilínea](msdn-online-vml-polyline-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Points = " *expresión* " >

**Sintaxis de script**

*Element* . Points = "*expresión * *"**

*expresión* = de *elemento*. Points

**Comentarios:**

Define un conjunto de segmentos de línea recta que se componen de una serie de puntos. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC). El valor predeterminado es "0, 0 10, 10". Tenga en cuenta que no se requieren comas, pero facilitan la lectura.

*Atributo estándar de VML*

**Ejemplo**

La polilínea comienza en el punto 10, 10 y termina en 100.100, con los valores en puntos.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 