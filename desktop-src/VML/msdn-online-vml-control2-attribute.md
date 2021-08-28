---
title: Atributo VML Control2
description: Atributo VML Control2
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c0eee9ba861a73ec6d9f0fd07cca22a551c92c5add5498cd0e33522419fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999255"
---
# <a name="vml-control2-attribute"></a>Atributo VML Control2

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el segundo punto de control de una curva bézier. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *element* control2=" *expression* ">

**Sintaxis de script**

*Element* .control2="*expression*"

*expresión* = *elemento*.control2

**Comentarios:**

Define el segundo punto de control de una curva bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 20.0.

*Atributo estándar de VML*

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se sitúan a lo largo del camino para extraer la curva hacia abajo para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 