---
title: Atributo de desplazamiento (sombra) (VML)
description: Atributo de desplazamiento (sombra) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995319"
---
# <a name="offset-attribute-shadowvml"></a>Atributo de desplazamiento (sombra) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define hasta qué punto se extiende la sombra más allá de la forma. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *elemento* offset = " *expresión* " >

**Sintaxis de script**

*Element* . offset = "*expresión*"

*expresión* = de *Element*. offset

**Comentarios:**

El desplazamiento predeterminado para el valor x es 2PT y el valor predeterminado para el valor y es 2PT. Los valores son una medida absoluta o un valor fraccionario de forma. Si es fraccionario, van del 50% a-50%.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene una sombra con un desplazamiento de 5 puntos hacia abajo y 10 puntos a la derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 