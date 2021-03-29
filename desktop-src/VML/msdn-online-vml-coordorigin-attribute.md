---
title: Atributo CoordOrigin de VML
description: Atributo CoordOrigin de VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904630"
---
# <a name="vml-coordorigin-attribute"></a>Atributo CoordOrigin de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica el origen de la unidad de coordenadas del rectángulo que delimita una forma. Lectura/escritura [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* coordorigin = " *expresión* " >

**Sintaxis de script**

*Element* . coordorigin = "*expresión*"

*expresión* = de *elemento*. coordorigin

**Comentarios:**

Si no se especifica, las coordenadas de origen son (0,0) en la esquina superior izquierda del cuadro de límite de la forma.

El valor x de **CoordSize** se agrega al valor x de **CoordOrigin** para determinar el intervalo de los valores horizontales. Por ejemplo, si el valor x de **CoordOrigin** es-100 y el valor x de **CoordSize** es 200, las unidades horizontales van de-100 a + 100. Si el valor x de **CoordOrigin** es 100 y el valor x de **CoordSize** es 200, las unidades horizontales van de 100 a 300, todo dentro del cuadro de límite. Lo mismo se aplica a los valores y.

Tenga en cuenta que este atributo es un vector y que las unidades son el mismo tipo de unidad que [CoordSize](msdn-online-vml-coordsize-attribute.md) .

En scripting, dado que se trata de un vector 2D, puede tener acceso a los valores x e y por separado, y también puede determinar el tipo de unidades que se espera.

*Atributo estándar de VML*

**Ejemplo**

El centro del cuadro de límite será el origen (0,0) de la ruta de acceso de la forma. Dado que **CoordOrigin** es "-500-500" y **CoordSize** es "1000 1000", las unidades horizontales y verticales oscilarán entre-500 y + 500. La esquina izquierda y superior de la ruta de acceso estará en el centro del cuadro de límite definido por los puntos izquierdo y superior, tal como se define en el **estilo**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo del atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 