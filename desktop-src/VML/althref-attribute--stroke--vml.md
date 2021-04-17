---
title: Atributo AltHRef (Stroke) (VML)
description: Atributo AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695716"
---
# <a name="althref-attribute-strokevml"></a>Atributo AltHRef (Stroke) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica una referencia alternativa para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* o:althref = " *expresión* " >

**Sintaxis de script**

*Element* . althref = "*expresión*"

*expresión* = de *elemento*. althref

**Comentarios:**

Admite la conservación de datos PICT a través de Roundtripping HTML. En la escritura HTML, se guarda la representación alternativa (es decir, los datos PICT originales si el archivo se originó en el equipo Macintosh). En la lectura de HTML, **AltHRef** se favorece en **src**.

*Microsoft Office atributo Extensions*

**Ejemplo**

El trazo de la forma tiene un **AltHRef** que señala a un archivo denominado myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 