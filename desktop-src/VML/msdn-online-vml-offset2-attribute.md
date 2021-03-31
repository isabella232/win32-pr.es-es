---
title: Atributo Offset2 de VML
description: Atributo Offset2 de VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533436"
---
# <a name="vml-offset2-attribute"></a>Atributo Offset2 de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina un segundo desplazamiento. Lectura/escritura **VgVector2D**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *Element* offset2 = " *expresión* " >

**Sintaxis de script**

*Element* . offset2 = "*expresión*"

*expresión* = de *elemento*. offset2

**Comentarios:**

El valor predeterminado para un segundo desplazamiento para el valor x es 0 y el valor predeterminado para el valor y es 0. Los valores son una medida absoluta o un valor fraccionario de forma. Si es fraccionario, los valores van de 50% a-50%.

Use un segundo desplazamiento para crear efectos de sombra especiales. Vea el atributo [Type](type-attribute--shadow--vml.md) para obtener más información sobre los dos desplazamientos.

*Atributo estándar de VML*

**Ejemplo**

Se crea una sombra doble para la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 