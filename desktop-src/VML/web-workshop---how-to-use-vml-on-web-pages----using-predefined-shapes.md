---
title: Usar formas predefinidas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, formas predefinidas
- diseñar páginas web, formas predefinidas
- Lenguaje de marcado de vectores (VML), formas predefinidas
- VML (Lenguaje de marcado de vectores), formas predefinidas
- gráficos vectoriales, formas predefinidas
- Formas VML, predefinidas
- formas predefinidas
- Lenguaje de marcado de vectores (VML), elemento Rect
- VML (Lenguaje de marcado de vectores), elemento Rect
- gráficos vectoriales, elemento Rect
- elemento Rect
- Elementos VML, Rect
- Lenguaje de marcado de vectores (VML), elemento roundrect
- VML (Lenguaje de marcado de vectores), elemento roundrect
- graphics Vector, elemento roundrect
- elemento roundrect
- Elementos VML, roundrect
- Lenguaje de marcado de vectores (VML), elemento de línea
- VML (Lenguaje de marcado de vectores), elemento de línea
- Vector Graphics, line (elemento)
- elemento line
- Elementos VML, línea
- Lenguaje de marcado de vectores (VML), elemento Polyline
- VML (Lenguaje de marcado de vectores), elemento Polyline
- Vector Graphics, Polyline (elemento)
- Polyline (elemento)
- Elementos VML, Polyline
- Elemento Curve de Lenguaje de marcado de vectores (VML)
- VML (Lenguaje de marcado de vectores), elemento Curve
- gráficos vectoriales, elemento Curve
- elemento Curve
- Elementos VML, curva
- Lenguaje de marcado de vectores (VML), elemento Arc
- VML (Lenguaje de marcado de vectores), elemento Arc
- gráficos vectoriales, elemento Arc
- elemento Arc
- Elementos VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533268"
---
# <a name="using-predefined-shapes"></a>Usar formas predefinidas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede usar el `<oval>` elemento de VML para crear un óvalo sencillo. VML proporciona varios elementos predefinidos. En este tema, se muestra cómo dibujar gráficos mediante estos elementos.

En este tema:

-   [Rect](#roundrect)
-   [roundrect](#roundrect)
-   [Ondula](#polyline)
-   [Polyline](#polyline)
-   [curva](#curve)
-   [vería](#arc)
-   [Resumen](#summary)

## <a name="rect"></a>rect

Puede usar el `<rect>` elemento para dibujar un rectángulo. Después, puede personalizar el rectángulo especificando distintos atributos de propiedad.

Por ejemplo, puede dibujar un rectángulo relleno con azul especificando **fillColor**= "Blue" y póngale un contorno rojo de 3,5 puntos especificando **StrokeColor**= "red" **strokeweight**= "3.5 PT", como se muestra en la siguiente representación de VML:

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . (Nota: la especificación de VML no tiene un marcador para el `<rect>` elemento).

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="roundrect"></a>roundrect

Puede usar el `<roundrect>` elemento para dibujar un rectángulo con esquinas redondeadas. Después, puede personalizar el rectángulo redondeado especificando distintos atributos de propiedad.

Por ejemplo, puede dibujar un rectángulo con esquinas redondeadas del 30% de la mitad de la dimensión más pequeña del rectángulo mediante la especificación de la función de 0,3 "StrokeColor", para rellenarlo con amarillo; para ello, especifique **fillColor**= "Yellow" y asígnele un contorno rojo de 2 puntos especificando = "red" **strokeweight**= "2PT", como se muestra en la siguiente representación

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="line"></a>line

Puede usar el `<line>` elemento para crear una línea recta. Después, puede personalizar la línea especificando distintos atributos de propiedad.

Por ejemplo, puede dibujar una línea horizontal especificando **from**= "20 PT, 20 PT" **en**= "100pt, 20 PT" y conviértalo en 2 puntos y en rojo especificando **StrokeColor**= "red" **strokeweight**= "2PT", tal y como se muestra en la siguiente representación en VML:

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Puede dibujar una línea vertical o diagonal simplemente especificando valores diferentes para los atributos **de propiedad From** y **to** , tal y como se muestra en la siguiente representación VML:

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="polyline"></a>Polyline

Puede usar el `<polyline>` elemento para definir formas que se crean a partir de segmentos de línea conectados. Después, puede personalizar la forma especificando distintos atributos de propiedad.

Por ejemplo, para dibujar la forma que se muestra en la siguiente imagen, puede escribir la siguiente representación en VML:

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="curve"></a>curva

Puede usar el `<curve>` elemento para dibujar una curva Bézier cúbica. Después, puede personalizar la curva especificando distintos atributos de propiedad.

Por ejemplo, para dibujar una curva como se muestra en la siguiente imagen, puede escribir la siguiente representación en VML:

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="arc"></a>arc

Puede usar el `<arc>` elemento para dibujar un arco que se define como un segmento de una elipse. El arco se define mediante la intersección de la elipse con los vectores de radio inicial y final dados por los ángulos. Los ángulos se calculan mediante las propiedades de un círculo (ancho igual a alto) y, a continuación, se escalan de forma anisotrópico al ancho y el alto deseados.

Por ejemplo, puede dibujar un arco que empiece en 0 grados y termine en 90 grados especificando **startAngle**= "0" imponed = " **90",** como se muestra en la siguiente representación de VML:

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Puede cambiar el arco especificando distintos valores de **startAngle** y  impuestos, tal y como se muestra en la siguiente representación de VML:

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="summary"></a>Resumen

Puede usar elementos predefinidos de VML como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` y `<arc>` para dibujar fácilmente gráficos en una página web y, a continuación, personalizar esos gráficos cambiando sus atributos de propiedad.

 

 