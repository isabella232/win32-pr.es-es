---
title: Atributo HRef (ImageData) (VML)
description: Atributo HRef (ImageData) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791722"
---
# <a name="href-attribute-imagedatavml"></a>Atributo HRef (ImageData) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una dirección URL para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *Element* o:href = " *expresión* " >

**Sintaxis de script**

*Element* . href = "*expresión*"

*expresión* = de *elemento*. href

**Comentarios:**

Al hacer clic en la forma, el explorador cargará la dirección URL. El atributo **href** es similar al atributo **href** de HTML estándar de los delimitadores.

El uso de este atributo facilita la creación de imágenes de buttonswith en una página web.

Este atributo lo usa Microsoft Office solo si una imagen se ha vinculado e incrustado. Microsoft Word tiene una interfaz de usuario para insertar imágenes de esta manera.

*Microsoft Office atributo Extensions*

**Ejemplo**

Cuando se hace clic en la imagen, el explorador carga la Página principal de Microsoft Corporation.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 