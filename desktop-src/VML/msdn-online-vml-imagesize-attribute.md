---
title: Atributo ImageSize de VML
description: Atributo ImageSize de VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be63fb0adf39e2494ae2fa4d1037b96c7873a7c12524215de0d1ecfd016e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600251"
---
# <a name="vml-imagesize-attribute"></a>Atributo ImageSize de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la imagen para el trazo. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* imagesize=" *expression* ">

**Sintaxis de script**

*element* .imagesize="*expression*"

*expresión* = *elemento*.imagesize

**Comentarios:**

El valor predeterminado es el tamaño de la imagen.

*Atributo estándar de VML*

**Ejemplo**

La imagen de trazo tendrá un tamaño de 10 a 10 puntos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 