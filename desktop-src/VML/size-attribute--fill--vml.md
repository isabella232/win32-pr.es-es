---
title: Atributo Size (Fill)(VML)
description: Atributo Size (Fill)(VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754150"
---
# <a name="size-attribute-fillvml"></a>Atributo Size (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la imagen para el relleno. Lectura/escritura [Dvvector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* size=" *expression* ">

**Sintaxis de script**

*elemento* .size="*expression"".**

*expresión* = *element*.size

**Comentarios:**

El valor predeterminado es el tamaño de la imagen original. Los tamaños mayores que la forma mostrarán una versión ampliada pero recortada de la imagen.

*Atributo estándar de VML*

**Ejemplo**

Aunque el tamaño original de la imagen es de 50 por 50 puntos, la imagen se mostrará como una imagen de 10 por 10 en el centro del relleno.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 