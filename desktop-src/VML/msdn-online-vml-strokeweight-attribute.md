---
title: Atributo StrokeWeight de VML
description: Atributo StrokeWeight de VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac5efa964607fdd942c8dff31a4a124d424aa5fbfeede27abc6164fddef087
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680685"
---
# <a name="vml-strokeweight-attribute"></a>Atributo StrokeWeight de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el grosor del pincel que acaricia el trazado de una forma. Lectura/escritura **SILENGTH**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* strokeweight=" *expression* ">

**Sintaxis de script**

*element* .strokeweight="*expression*"

*expresión* = *elemento*.strokeweight

**Comentarios:**

El valor se duplica del atributo **Weight** del **elemento Stroke.** Si se especifica un número, pero no se agregan unidades, la unidad de medida predeterminada es la Emu. Si no se especifica ningún valor, el valor predeterminado es 1 píxel (1 píxel).

Sin embargo, para el scripting, la unidad de medida predeterminada está en puntos.

*Atributo estándar de VML*

**Vea también**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Ejemplo**

El grosor del trazo de la forma es de 1 punto.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo StrokeWeight](/previous-versions/bb264095(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 