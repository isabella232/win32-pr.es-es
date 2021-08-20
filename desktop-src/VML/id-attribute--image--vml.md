---
title: Atributo ID (Image)(VML)
description: Atributo ID (Image)(VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d09c2f3ec4a58e303c54ca9fd191b6872f7e3b12b30f9a8707be54108f46c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939492"
---
# <a name="id-attribute-imagevml"></a>Atributo ID (Image)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un nombre que proporciona un identificador único para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* id=" *expression* ">

**Sintaxis de script**

*element* .id="*expression*"

*expresión* = *elemento*.id

**Comentarios:**

Use **id.** para hacer referencia a una imagen específica. Una vez que haya creado una imagen y le haya dado un identificador, puede usar el nombre del identificador cuando desee manipular la imagen.

**Atributo estándar de VML**

**Ejemplo**

La forma tiene un **id. de ImageData** denominado "myimage".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 