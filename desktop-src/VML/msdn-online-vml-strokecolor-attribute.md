---
title: Atributo StrokeColor de VML
description: Atributo StrokeColor de VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124238"
---
# <a name="vml-strokecolor-attribute"></a>Atributo StrokeColor de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el color de pincel que marca el trazado de una forma. Lectura/escritura [IVgColor](msdn-online-vml-ivgcolor.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* strokecolor=" *expression* ">

**Sintaxis de script**

*element* .strokecolor="*expression*"

*expresión* = *elemento*.strokecolor

**Comentarios:**

El valor se duplica del atributo **Color** del [elemento Stroke.](msdn-online-vml-stroke-element.md)

*Atributo estándar de VML*

**Ejemplo**

El color del trazo del rectángulo es rojo.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo StrokeColor](/previous-versions/bb264093(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 