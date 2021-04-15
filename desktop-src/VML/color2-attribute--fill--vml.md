---
title: Color2 (atributo, Fill) (VML)
description: Color2 (atributo, Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676449"
---
# <a name="color2-attribute-fillvml"></a>Color2 (atributo, Fill) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un segundo color para los rellenos. Lectura/escritura [VgColor](msdn-online-vml-ivgcolor.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* color2 = " *expresión* " >

**Sintaxis de script**

*Element* . color2 = "*expresión*"

*expresión* = de *elemento*. color2

**Comentarios:**

Se utiliza un segundo color cuando un tipo de relleno es un patrón o un degradado. El valor predeterminado es **blanco**.

*Atributo estándar de VML*

**Ejemplo**

El tipo de relleno de la forma es un patrón en el que la imagen de origen define el relleno de primer plano, pero el segundo color define el fondo transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 