---
title: Src (atributo, Fill) (VML)
description: Src (atributo, Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487762"
---
# <a name="src-attribute-fillvml"></a>Src (atributo, Fill) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la imagen que se va a cargar para un relleno. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *elemento* src = " *expresión* " >

**Sintaxis de script**

*Element* . src = "*expresión * *"**

*expresión* = de *elemento*. src

**Comentarios:**

Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen. Si este atributo aparece solo (es decir, ningún atributo **href** o **title** ), la imagen está vinculada.

*Atributo estándar de VML*

**Ejemplo**

Se muestra una imagen en mosaico que usa el archivo myimage.gif como origen.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 