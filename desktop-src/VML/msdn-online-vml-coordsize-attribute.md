---
title: Atributo CoordSize de VML
description: Atributo CoordSize de VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695618"
---
# <a name="vml-coordsize-attribute"></a>Atributo CoordSize de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica las unidades horizontales y verticales del rectángulo que delimita una forma. Lectura/escritura [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* coordsize = " *expresión* " >

**Sintaxis de script**

*Element* . coordsize = "*expresión*"

*expresión* = de *elemento*. coordsize

**Comentarios:**

Si no se especifica, el tamaño de la coordenada es el mismo que el del rectángulo de selección de la forma.

Tenga en cuenta que este atributo es un vector y que las unidades son relativas a la longitud y el ancho del rectángulo delimitador.

Tenga en cuenta también que la asignación entre **coordsize** y el cuadro de límite se puede convertir en anisotrópico. Asegúrese de que el **ancho de coordsize** y el **alto de coordsize** coinciden con el ancho y el **alto** de **estilo** si no desea distorsionar la forma.

En scripting, dado que se trata de un vector 2D, puede tener acceso a los valores x e y por separado, y también puede determinar el tipo de unidades que se espera.

*Atributo estándar de VML*

**Ejemplo**

La forma es 100 puntos alto y 100 puntos de ancho, pero cada unidad horizontal y vertical del espacio de coordenadas es 1/10 de un punto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo del atributo CoordSize](/previous-versions/bb229665(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 