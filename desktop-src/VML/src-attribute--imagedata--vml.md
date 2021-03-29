---
title: Atributo src (ImageData) (VML)
description: Atributo src (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077815"
---
# <a name="src-attribute-imagedatavml"></a>Atributo src (ImageData) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un origen para la imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* src = " *expresión* " >

**Sintaxis de script**

*Element* . src = "*expresión*"

*expresión* = de *elemento*. src

**Comentarios:**

Este atributo siempre debe usarse con el elemento [ImageData](msdn-online-vml-imagedata-element.md) y apuntar a datos de imagen válidos para que se muestre una imagen. Si este atributo aparece sin [href](https://www.bing.com/search?q=HRef) o [title](title-attribute--imagedata--vml.md), la imagen está vinculada.

*Atributo estándar de VML*

**Ejemplo**

El origen de la imagen es un archivo denominado "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 