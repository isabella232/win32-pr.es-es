---
title: Atributo To (Curve)(VML)
description: Atributo To (Curve)(VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1d2a4c7fd91652ca59707ff00b67a8215d754134bc150402d72e833f249f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596246"
---
# <a name="to-attribute-curvevml"></a>Atributo To (Curve)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el punto final de una curva. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *element* to=" *expression* ">

**Sintaxis de script**

*Element* .to="*expression*"

*expresión* = *elemento*.to

**Comentarios:**

Define el punto final de una curva bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 30,20.

**Atributo estándar de VML**

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se sitúan a lo largo del camino para extraer la curva hacia abajo para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 