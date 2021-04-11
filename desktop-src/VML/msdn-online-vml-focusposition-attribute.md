---
title: Atributo FocusPosition de VML
description: Atributo FocusPosition de VML
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149612"
---
# <a name="vml-focusposition-attribute"></a>Atributo FocusPosition de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el centro de un degradado radial. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* focusposition = " *expresión* " >

**Sintaxis de script**

*Element* . focusposition = "*expresión*"

*expresión* = de *elemento*. focusposition

**Comentarios:**

Especifica los degradados radiales del centro positionfor. El vector es una fracción del ancho y el alto de la forma. El primero es un porcentaje del relleno en el borde izquierdo; el segundo es un porcentaje del relleno en la parte superior. El valor predeterminado es 0,0. Para colocar un relleno radial en el centro de una forma, use el valor del 50%, 50%.

*Atributo estándar de VML*

**Ejemplo**

El relleno radial se centrará de modo que el azul se inicie en el centro y Radiate hacia afuera, cambiando gradualmente a rojo en el momento en que alcance los bordes y las esquinas exteriores.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 