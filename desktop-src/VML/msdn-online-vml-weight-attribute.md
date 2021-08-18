---
title: Atributo de peso de VML
description: Atributo de peso de VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1a4dc7e33a4a1bf8421350bed9df374f7edd31a1c1a48a2b3e1549dc63084d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999095"
---
# <a name="vml-weight-attribute"></a>Atributo de peso de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el grosor de un trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* weight=" *expression* ">

**Sintaxis de script**

*element* .weight="*expression*"

*expresión* = *elemento*.weight

**Comentarios:**

Este atributo es el mismo que el atributo **StrokeWeight** de **Shape** y lo invalida. El valor predeterminado es 1 punto.

*Atributo estándar de VML*

**Ejemplo**

El trazo tiene un grosor de 5 puntos, no 2 puntos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 