---
title: Atributo AltHRef (Stroke)(VML)
description: Atributo AltHRef (Stroke)(VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cbdbe82330d154675b135f7e9f35869c8f47e25715680d97df05e5511a01e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867454"
---
# <a name="althref-attribute-strokevml"></a>Atributo AltHRef (Stroke)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica una referencia alternativa para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *elemento* o:althref=" *expresión* ">

**Sintaxis de script**

*Element* .althref="*expression*"

*expresión* = *elemento*.althref

**Comentarios:**

Admite la conservación de los datos DE LAN mediante el redondeo HTML. En la escritura HTML, se guarda la representación alternativa (es decir, los datos originales de LAV si el archivo se originó en Macintosh). En lectura HTML, **AltHRef** se favorece sobre **Src**.

*Microsoft Office Atributo Extensions*

**Ejemplo**

El trazo de la forma tiene un **AltHRef** que apunta a un archivo denominado myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 