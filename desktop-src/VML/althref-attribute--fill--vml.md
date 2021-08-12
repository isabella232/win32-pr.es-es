---
title: Atributo AltHRef (Fill)(VML)
description: Atributo AltHRef (Fill)(VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181f98ace80403668f8f67c6f8412091271fdfcf2abcb5a1320d0685853d92bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603008"
---
# <a name="althref-attribute-fillvml"></a>Atributo AltHRef (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una referencia alternativa para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* o:althref=" *expression* ">

**Sintaxis de script**

*Element* .althref="*expression*"

*expresión* = *elemento*.althref

**Comentarios:**

Admite la conservación de los datos DE LAN mediante el redondeo HTML. En la escritura HTML, se guarda la representación alternativa (los datos ORIGINAL DE SI el archivo se originó en Apple Macintosh). En lectura HTML, **AltHRef** se favorece sobre **Src**.

*Microsoft Office Atributo Extensions*

**Ejemplo**

El relleno de la forma tiene un **AltHRef** que apunta a un archivo denominado myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 