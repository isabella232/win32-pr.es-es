---
title: Atributo From (Line)(VML)
description: Atributo From (Line)(VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a8bf41462f698397b193835d08655f8d6acefb2df77b17e035ec170c3c4781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099315"
---
# <a name="from-attribute-linevml"></a>Atributo From (Line)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el punto inicial de una línea. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Línea](msdn-online-vml-line-element.md)

**Sintaxis de etiquetas**

<v: *element* from=" *expression* ">

**Sintaxis de script**

*Element* .from="*expression*"

*expresión* = *elemento*.from

**Comentarios:**

Define el punto inicial de la línea en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 0,0.

*Atributo estándar de VML*

**Ejemplo**

La línea comienza en una ubicación 10 puntos hacia abajo y 10 puntos a la derecha de la esquina superior izquierda del espacio primario.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 