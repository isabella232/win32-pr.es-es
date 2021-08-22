---
title: Atributo BlackLevel de VML
description: Atributo BlackLevel de VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057913"
---
# <a name="vml-blacklevel-attribute"></a>Atributo BlackLevel de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la intensidad del negro en una imagen. Lectura/escritura **NumberNumber**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *element* blacklevel=" *expression* ">

**Sintaxis de script**

*element* .blacklevel="*expression*"

*expresión* = *elemento*.blacklevel

**Comentarios:**

Permite modificar el nivel de color para que los negros aparezcan como verdaderos negros y todos los demás colores sean visibles como tonalidades por encima del negro. El valor predeterminado es 0. Aunque se permite cualquier número entre infinito positivo y negativo, los valores menores que -0,5 se mostrarán como todos los valores negros y los valores mayores que 0,5 se mostrarán como todos los valores en blanco.

*Atributo estándar de VML*

**Ejemplo**

La imagen se mostrará con colores muy oscuros.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 