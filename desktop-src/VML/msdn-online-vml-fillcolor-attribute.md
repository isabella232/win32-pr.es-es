---
title: Atributo FillColor de VML
description: Atributo FillColor de VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601365"
---
# <a name="vml-fillcolor-attribute"></a>Atributo FillColor de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el color de pincel que rellena el trazado cerrado de una forma. Lectura/escritura [IVgColor](msdn-online-vml-ivgcolor.md) .

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* fillcolor=" *expression* ">

**Sintaxis de script**

*element* .fillcolor="*expression*"

*expresión* = *elemento*.fillcolor

**Comentarios:**

El **valor FillColor** se duplica del atributo **Color** del **elemento Fill.**

*Atributo estándar de VML*

**Vea también**

[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Ejemplo**

El color de relleno del rectángulo es rojo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo FillColor](/previous-versions/bb229668(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 