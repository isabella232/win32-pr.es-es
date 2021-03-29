---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078345"
---
# <a name="vml-focussize-attribute"></a>Atributo FocusSize de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el tamaño del foco para los rellenos radiales. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* focussize = " *expresión* " >

**Sintaxis de script**

*Element* . focussize = "*expresión*"

*expresión* = de *elemento*. focussize

**Comentarios:**

Los valores son fracciones del ancho y el alto de la forma. El primero es un porcentaje del relleno en el borde derecho de la forma y el segundo es un porcentaje del relleno en la parte inferior de la forma. El valor predeterminado es 0,0. Un valor **FocusSize** de 100%, 100% y un **FocusPosition** de 0, 0 haría que el color2 dominara por completo la combinación. Se recomiendan valores pequeños de aproximadamente el 10%, 10% para las combinaciones equilibradas.

*Atributo estándar de VML*

**Ejemplo**

El relleno radial creará una mezcla empezando en el centro como azul y se convertirá en rojo en los cuatro bordes. El centro de la mezcla está definido por **FocusPosition** y el tamaño del color inicial interior viene determinado por **FocusSize**.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 