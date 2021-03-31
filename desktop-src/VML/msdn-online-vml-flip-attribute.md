---
title: Atributo Flip de VML
description: Atributo Flip de VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793761"
---
# <a name="vml-flip-attribute"></a>Atributo Flip de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Cambia la orientación de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Flip: *Expression* " >

**Sintaxis de script**

*Element* . Style. Flip = "*expresión*"

*expresión* = de *elemento*. Style. flip

**Comentarios:**

Estos valores incluyen:



| Value | Descripción                                           |
|-------|-------------------------------------------------------|
| x     | Se voltea a lo largo del eje y, invirtiendo las coordenadas *x*. |
| y     | Se voltea a lo largo del eje *x* y se invierten las coordenadas y. |
| xy    | Se voltea a lo largo del eje y y del eje *x*.                  |
| YX    | Se *voltea a lo* largo del eje *x* e y.                |



 

*Atributo estándar de VML*

**Vea también**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Ejemplo**

La forma se voltea a lo largo del eje *y* invirtiendo las coordenadas *x* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Ejemplo de atributo Flip](/previous-versions/bb229670(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 