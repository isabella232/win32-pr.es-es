---
title: Atributo VML Control1
description: Atributo VML Control1
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b4c57a936a2820e5189be78cab119b4455d20af22735a47a66c444f721723f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601947"
---
# <a name="vml-control1-attribute"></a>Atributo VML Control1

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el primer punto de control de una curva bézier. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *element* control1=" *expression* ">

**Sintaxis de script**

*element* .control1="*expression*"

*expresión* = *elemento*.control1

**Comentarios:**

Define el primer punto de control de una curva bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 10,10.

*Atributo estándar de VML*

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se encuentran a lo largo del camino para extraer la curva hacia abajo para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 