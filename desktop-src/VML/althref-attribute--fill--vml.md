---
title: Atributo AltHRef (relleno) (VML)
description: Atributo AltHRef (relleno) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487886"
---
# <a name="althref-attribute-fillvml"></a>Atributo AltHRef (relleno) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una referencia alternativa para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* o:althref = " *expresión* " >

**Sintaxis de script**

*Element* . althref = "*expresión*"

*expresión* = de *elemento*. althref

**Comentarios:**

Admite la conservación de datos PICT a través de Roundtripping HTML. En la escritura HTML, se guarda la representación alternativa (los datos PICT originales si el archivo se originó en Apple Macintosh). En la lectura de HTML, **AltHRef** se favorece en **src**.

*Microsoft Office atributo Extensions*

**Ejemplo**

El relleno de la forma tiene un **AltHRef** que señala a un archivo denominado myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 