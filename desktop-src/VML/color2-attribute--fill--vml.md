---
title: Atributo Color2 (Fill)(VML)
description: Atributo Color2 (Fill)(VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007895"
---
# <a name="color2-attribute-fillvml"></a>Atributo Color2 (Fill)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un segundo color para los rellenos. Lectura/escritura [DvColor](msdn-online-vml-ivgcolor.md) .

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *element* color2=" *expression* ">

**Sintaxis de script**

*element* .color2="*expression*"

*expresión* = *elemento*.color2

**Comentarios:**

Se usa un segundo color cuando un tipo de relleno es un patrón o un degradado. El valor predeterminado es **Blanco.**

*Atributo estándar de VML*

**Ejemplo**

El tipo de relleno de la forma es un patrón en el que la imagen de origen define el relleno de primer plano, pero el segundo color define el fondo transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 