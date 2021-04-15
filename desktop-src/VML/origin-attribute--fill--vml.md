---
title: Origin (atributo, Fill) (VML)
description: Origin (atributo, Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421366"
---
# <a name="origin-attribute-fillvml"></a>Origin (atributo, Fill) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el centro de una imagen de relleno. Lectura/escritura [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Origin = " *expresión* " >

**Sintaxis de script**

*Element* . Origin = "*expresión*"

*expresión* = de *elemento*. Origin

**Comentarios:**

Especifica un punto relativo a la esquina superior izquierda de la imagen; este punto se trata como el origen de la imagen. El valor predeterminado es el centro de la imagen. El vector es una fracción del ancho y el alto de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen del relleno se desplaza hacia la izquierda hasta un punto 50% del ancho de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 