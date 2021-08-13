---
title: Atributo Src (ImageData)(VML)
description: Atributo Src (ImageData)(VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688bc1e82afbaf0747a03465c93feb1d760cc60eb441792654ef11ec59cee749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596687"
---
# <a name="src-attribute-imagedatavml"></a>Atributo Src (ImageData)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un origen para la imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *elemento* src=" *expresión* ">

**Sintaxis de script**

*element* .src="*expression*"

*expresión* = *elemento*.src

**Comentarios:**

Este atributo siempre debe usarse con el [elemento ImageData](msdn-online-vml-imagedata-element.md) y apuntar a datos de imagen válidos para que se muestre una imagen. Si este atributo aparece sin [HRef](https://www.bing.com/search?q=HRef) o [Title](title-attribute--imagedata--vml.md), la imagen está vinculada.

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



 

 