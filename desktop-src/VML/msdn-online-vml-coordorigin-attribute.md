---
title: Atributo CoordOrigin de VML
description: Atributo CoordOrigin de VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf568f2c305108a651d56a891a96890154f9493cbadd80a9c5610414c88f4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601948"
---
# <a name="vml-coordorigin-attribute"></a>Atributo CoordOrigin de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el origen de la unidad de coordenadas del rectángulo que delimita una forma. Lectura/escritura [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* coordorigin=" *expression* ">

**Sintaxis de script**

*Element* .coordorigin="*expression*"

*expresión* = *elemento*.coordorigin

**Comentarios:**

Si no se especifica, las coordenadas de origen están (0,0) en la esquina superior izquierda del cuadro de límite de forma.

El valor x de **CoordSize** se agrega al valor x de **CoordOrigin** para determinar el intervalo de los valores horizontales. Por ejemplo, si el valor x de **CoordOrigin** es -100 y el valor x de **CoordSize** es 200, las unidades horizontales oscilarán entre -100 y +100. Si el valor x de **CoordOrigin** es 100 y el valor x de **CoordSize** es 200, las unidades horizontales oscilarán entre 100 y 300, todo dentro del cuadro de límite. Lo mismo se aplica a los valores y.

Tenga en cuenta que este atributo es un vector y que las unidades son el mismo tipo de unidad que [CoordSize](msdn-online-vml-coordsize-attribute.md) .

En el scripting, dado que se trata de un vector 2D, puede acceder a los valores x e y por separado, y también puede determinar el tipo de unidades esperadas.

*Atributo estándar de VML*

**Ejemplo**

El centro del cuadro de límite será el origen (0,0) de la ruta de acceso de la forma. Dado que **CoordOrigin** es "-500 -500" y **CoordSize** es "1000 1000", las unidades horizontal y vertical oscilarán entre -500 y +500. La esquina izquierda y superior de la ruta de acceso estarán en el centro del cuadro de límite definido por los puntos izquierdo y superior, tal como se define en **Estilo**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 