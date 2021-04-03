---
title: Src (atributo, Stroke) (VML)
description: Src (atributo, Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791806"
---
# <a name="src-attribute-strokevml"></a>Src (atributo, Stroke) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la imagen de origen que se va a cargar para un relleno de trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *elemento* src = " *expresión* " >

**Sintaxis de script**

*Element* . src = "*expresión*"

*expresión* = de *elemento*. src

**Comentarios:**

Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen. Si este atributo aparece solo, es decir, sin **href** ni **title**, la imagen se vincula.

*Atributo estándar de VML*

**Ejemplo**

El trazo se crea con la imagen especificada por el archivo de cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 