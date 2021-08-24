---
title: Atributo To (Line)(VML)
description: Atributo To (Line)(VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d1e47261daf76103717476a84eea3bed99ddb0b514192df8a74cd0b69572a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654455"
---
# <a name="to-attribute-linevml"></a>Atributo To (Line)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el punto final de una línea. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Línea](msdn-online-vml-line-element.md)

**Sintaxis de etiquetas**

<v: *element* to=" *expression* ">

**Sintaxis de script**

*Element* .to="*expression*"

*expresión* = *elemento*.to

**Comentarios:**

Define el punto final de la línea en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 10,10.

**Atributo estándar de VML**

**Ejemplo**

La línea termina en una ubicación 100 puntos hacia abajo y 100 puntos a la derecha de la esquina superior izquierda del espacio primario.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 