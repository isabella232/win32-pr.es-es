---
title: Size (atributo, Fill) (VML)
description: Size (atributo, Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995318"
---
# <a name="size-attribute-fillvml"></a>Size (atributo, Fill) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la imagen para el relleno. Lectura/escritura [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* size = " *expresión* " >

**Sintaxis de script**

*Element* . size = "*expresión * *"**

*expresión* = de *elemento*. Size

**Comentarios:**

El valor predeterminado es el tamaño de la imagen original. Los tamaños mayores que el shapewill muestran una versión ampliada pero recortada de la imagen.

*Atributo estándar de VML*

**Ejemplo**

Aunque el tamaño original de la imagen es de 50 a 50 puntos, se mostrará la imagen como una imagen de 10 por 10 en el centro del relleno.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 