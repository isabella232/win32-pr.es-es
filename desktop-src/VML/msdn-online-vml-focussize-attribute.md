---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322bea9f9d78ff76cd631cc36149939bb5b3db5f87dc9c80e9f2a5100f031c1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099265"
---
# <a name="vml-focussize-attribute"></a>Atributo FocusSize de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tamaño del foco para los rellenos radiales. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* focussize=" *expression* ">

**Sintaxis de script**

*element* .focussize="*expression*"

*expresión* = *elemento*.focussize

**Comentarios:**

Los valores son fracciones del ancho y alto de la forma. El primero es un porcentaje del relleno al borde derecho de la forma y el segundo es un porcentaje del relleno hasta la parte inferior de la forma. El valor predeterminado es 0,0. Un **valor focusSize** de 100%,100 % y una **focusPosition** de 0,0 harían que Color2 dominase por completo la mezcla. Se recomiendan valores pequeños de alrededor del 10 %,10 % para las mezclas equilibradas.

*Atributo estándar de VML*

**Ejemplo**

El relleno radial creará una mezcla que comienza en el centro como azul y se vuelve roja en los cuatro bordes. FocusPosition define el centro  de la mezcla y el tamaño del color inicial interno viene determinado por **FocusSize.**


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



 

 