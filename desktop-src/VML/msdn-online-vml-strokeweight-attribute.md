---
title: Atributo StrokeWeight de VML
description: Atributo StrokeWeight de VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792202"
---
# <a name="vml-strokeweight-attribute"></a>Atributo StrokeWeight de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el grosor del pincel que traza el trazado de una forma. Lectura/escritura **VGLength**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* strokeweight = " *expresión* " >

**Sintaxis de script**

*Element* . strokeweight = "*expresión*"

*expresión* = de *elemento*. strokeweight

**Comentarios:**

El valor se duplica desde el atributo **Weight** del elemento **Stroke** . Si se especifica un número, pero no se agregan unidades, la unidad de medida predeterminada es la UME. Si no se especifica ningún valor, el valor predeterminado es 1 píxel (1px).

En el caso de las secuencias de comandos, sin embargo, la unidad de medida predeterminada está en puntos.

*Atributo estándar de VML*

**Vea también**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Ejemplo**

El grosor del trazo de la forma es de 1 punto.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo del atributo StrokeWeight](/previous-versions/bb264095(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 