---
title: Atributo Control1 de VML
description: Atributo Control1 de VML
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676381"
---
# <a name="vml-control1-attribute"></a>Atributo Control1 de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el primer punto de control de una curva Bézier. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Sensible](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *Element* Control1 = " *expresión* " >

**Sintaxis de script**

*Element* . Control1 = "*expresión*"

*expresión* = de *elemento*. Control1

**Comentarios:**

Define el primer punto de control de una curva Bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC). El valor predeterminado es 10, 10.

*Atributo estándar de VML*

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se sitúan a lo largo del modo de extraer la curva para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 