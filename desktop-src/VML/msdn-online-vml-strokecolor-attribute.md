---
title: Atributo StrokeColor de VML
description: Atributo StrokeColor de VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077912"
---
# <a name="vml-strokecolor-attribute"></a>Atributo StrokeColor de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el color del pincel que traza el trazado de una forma. Lectura/escritura [IVgColor](msdn-online-vml-ivgcolor.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* StrokeColor = " *expresión* " >

**Sintaxis de script**

*Element* . StrokeColor = "*expresión*"

*expresión* = de *elemento*. StrokeColor

**Comentarios:**

El valor se duplica desde el atributo **color** del elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Atributo estándar de VML*

**Ejemplo**

El color del trazo del rectángulo es rojo.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo del atributo StrokeColor](/previous-versions/bb264093(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 