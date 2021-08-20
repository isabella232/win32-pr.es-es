---
title: Atributo CoordSize de VML
description: Atributo CoordSize de VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9ce79507e789c38512e775100aa27eda25dc61d5f2af56f9a677daf04d238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999195"
---
# <a name="vml-coordsize-attribute"></a>Atributo CoordSize de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica las unidades horizontales y verticales del rectángulo que delimita una forma. Lectura/escritura [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* coordsize=" *expression* ">

**Sintaxis de script**

*Element* .coordsize="*expression*"

*expresión* = *elemento*.coordsize

**Comentarios:**

Si no se especifica, el tamaño de la coordenada es el mismo que el cuadro de límite de la forma.

Tenga en cuenta que este atributo es un vector y que las unidades son relativas a la longitud y el ancho del rectángulo delimitador.

Tenga en cuenta también que la **asignación entre coordsize** y el cuadro de límite se puede convertir en anisotropía. Asegúrese de que el ancho **de coordsize** y el  alto  **de coordsize** son los mismos que el ancho y el alto del estilo si no desea distorsionar la forma.

En el scripting, dado que se trata de un vector 2D, puede acceder a los valores x e y por separado, y también puede determinar el tipo de unidades esperadas.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene 100 puntos de alto y 100 puntos de ancho, pero cada unidad horizontal y vertical del espacio de coordenadas es de 1/10 de un punto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo CoordSize](/previous-versions/bb229665(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 