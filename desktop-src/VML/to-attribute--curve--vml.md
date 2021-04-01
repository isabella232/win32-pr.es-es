---
title: En atributo (curva) (VML)
description: En atributo (curva) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904813"
---
# <a name="to-attribute-curvevml"></a>En atributo (curva) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el punto final de una curva. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Sensible](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *Element* a = " *expresión* " >

**Sintaxis de script**

*Element* . to = "*expresión*"

*expresión* = de *elemento*. para

**Comentarios:**

Define el punto final de una curva Bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC). El valor predeterminado es 30, 20.

**Atributo estándar de VML**

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se sitúan a lo largo del modo de extraer la curva para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 