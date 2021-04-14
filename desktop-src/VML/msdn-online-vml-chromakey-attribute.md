---
title: Atributo Chromakey de VML
description: Atributo Chromakey de VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359140"
---
# <a name="vml-chromakey-attribute"></a>Atributo Chromakey de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el valor de color de la imagen que se tratará como transparente. Lectura/escritura **VgColor**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *Element* Chromakey = " *expresión* " >

**Sintaxis de script**

*Element* . Chromakey = "*expresión*"

*expresión* = de *elemento*. Chromakey

**Comentarios:**

Use este atributo para que las partes de una imagen sean transparentes mediante la creación de una incrustación de la transparencia en un color específico. Por ejemplo, si hace que el valor de **Chromakey** sea **negro**, cualquier parte de la imagen que sea negra será transparente y el color de relleno se "mostrará a través" de esa parte de la imagen.

*Atributo estándar de VML*

**Ejemplo**

En su lugar, las áreas de la imagen que son de negro sólido serán transparentes, lo que permite que el color de relleno verde se muestre a través de esas áreas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 