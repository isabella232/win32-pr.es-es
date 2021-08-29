---
title: Atributo con trazo de VML
description: Atributo con trazo de VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9398452365ee6076309cafa40c0373dcaa12d52a868e71eb77e4b42780badb0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754450"
---
# <a name="vml-stroked-attribute"></a>Atributo con trazo de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define si la ruta de acceso se va a trazo. Lectura/escritura [DvTriState](msdn-online-vml-vgtristate.md) .

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* stroked=" *expression* ">

**Sintaxis de script**

*expresión* .stroked="*del elemento*"

*expresión* = *elemento*.stroked

**Comentarios:**

El valor se duplica del atributo **On** del [elemento Stroke.](msdn-online-vml-stroke-element.md)

*Atributo estándar de VML*

**Ejemplo**

El trazado de la forma se acaricia.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo trazo](/previous-versions/bb264094(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 