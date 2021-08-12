---
title: Atributo Opacity (Stroke)(VML)
description: Atributo Opacity (Stroke)(VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f457ee73ffdccd589f5ab3b4d89c5ce4c05f871a71572c1f04b2ddef5de4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596776"
---
# <a name="opacity-attribute-strokevml"></a>Atributo Opacity (Stroke)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la cantidad de transparencia de un trazo. Lectura/escritura **Accionario**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* opacity=" *expression* ">

**Sintaxis de script**

*element* .opacity="*expression*"

*expresión* = *element*.opacity

**Comentarios:**

El valor predeterminado es 1,0.

*Atributo estándar de VML*

**Ejemplo**

El trazo es 50 % transparente.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 