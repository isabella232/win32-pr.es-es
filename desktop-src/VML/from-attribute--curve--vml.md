---
title: Atributo From (Curve)(VML)
description: Atributo From (Curve)(VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df431e9239f185ce83771f7822fe98e5bf491bd84a1deb7b869df7d3d2f235e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905505"
---
# <a name="from-attribute-curvevml"></a>Atributo From (Curve)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el punto inicial de una curva. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxis de etiquetas**

<v: *element* from=" *expression* ">

**Sintaxis de script**

*Element* .from="*expression*"

*expresión* = *elemento*.from

**Comentarios:**

Define el punto inicial de una curva bézier cúbica en el espacio de coordenadas del elemento primario. Si el elemento primario no es [](msdn-online-vml-units.md) un elemento VML, la unidad predeterminada es un píxel (pero también se puede especificar in, cm, mm, pt, pc). El valor predeterminado es 0,0.

*Atributo estándar de VML*

**Ejemplo**

La curva es sonriente. Comienza a la izquierda y termina a la derecha. Los dos puntos de control se encuentran a lo largo del camino para extraer la curva hacia abajo para dar la apariencia de una sonrisa.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 