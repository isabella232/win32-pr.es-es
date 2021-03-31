---
title: Del atributo (línea) (VML)
description: Del atributo (línea) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793654"
---
# <a name="from-attribute-linevml"></a>Del atributo (línea) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el punto inicial de una línea. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Line](msdn-online-vml-line-element.md)

**Sintaxis de etiquetas**

<v: *Element* from = " *expresión* " >

**Sintaxis de script**

*Element* . from = "*expresión*"

*expresión* = de *elemento*. from

**Comentarios:**

Define el punto inicial de la línea en el espacio de coordenadas del elemento primario. Si el elemento primario no es un elemento VML, la [unidad](msdn-online-vml-units.md) predeterminada es un píxel (pero también se puede especificar in, cm, mm, PT, PC). El valor predeterminado es 0, 0.

*Atributo estándar de VML*

**Ejemplo**

La línea comienza en una ubicación de 10 puntos hacia abajo y 10 puntos a la derecha de la esquina superior izquierda del espacio primario.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 