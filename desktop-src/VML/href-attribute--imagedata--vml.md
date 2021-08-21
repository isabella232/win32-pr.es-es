---
title: Atributo HRef (ImageData)(VML)
description: Atributo HRef (ImageData)(VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3c8640992ba5c71334cd4ac7170d7cebdea1997de228e29f6e50a9c7234ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118846137"
---
# <a name="href-attribute-imagedatavml"></a>Atributo HRef (ImageData)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una dirección URL para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* o:href=" *expression* ">

**Sintaxis de script**

*Element* .href="*expression*"

*expresión* = *elemento*.href

**Comentarios:**

Cuando se hace clic en la forma, el explorador cargará la dirección URL. El **atributo HRef** es similar al atributo **HRef** HTML estándar de delimitadores.

El uso de este atributo facilita la creación de botones con imágenes en una página web.

Este atributo se usa en Microsoft Office solo si se ha vinculado e insertado una imagen. Microsoft Word tiene una interfaz de usuario para insertar imágenes de esta manera.

*Microsoft Office Atributo Extensions*

**Ejemplo**

Cuando se hace clic en la imagen, el explorador cargará el Microsoft Corporation página principal.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 