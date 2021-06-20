---
title: Usar formas predefinidas
description: En este artículo se describe el uso de formas predefinidas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Taller web, formas predefinidas
- diseñar páginas web, formas predefinidas
- Lenguaje de marcado de vectores (VML), formas predefinidas
- VML (Lenguaje de marcado de vectores), formas predefinidas
- gráficos vectoriales, formas predefinidas
- Formas de VML predefinidas
- formas predefinidas
- Lenguaje de marcado de vectores (VML), elemento rect
- VML (Lenguaje de marcado de vectores), elemento rect
- vector graphics,rect element
- elemento rect
- Elementos VML, rect
- Lenguaje de marcado de vectores (VML), elemento roundrect
- VML (Lenguaje de marcado de vectores), elemento roundrect
- vector graphics,roundrect element
- roundrect, elemento
- Elementos VML,roundrect
- Lenguaje de marcado de vectores (VML),elemento line
- VML (Lenguaje de marcado de vectores),elemento line
- gráficos vectoriales, elemento de línea
- elemento line
- Elementos de VML, línea
- Lenguaje de marcado de vectores (VML), elemento de polilínea
- VML (Lenguaje de marcado de vectores),elemento de polilínea
- gráficos vectoriales, elemento de polilínea
- elemento de polilínea
- Elementos vml, polilínea
- Lenguaje de marcado de vectores (VML),elemento curve
- VML (Lenguaje de marcado de vectores),elemento curve
- gráficos vectoriales, elemento de curva
- elemento curve
- Elementos de VML, curva
- Lenguaje de marcado de vectores (VML),elemento arc
- VML (Lenguaje de marcado de vectores),arc element
- vector graphics,arc element
- arc, elemento
- Elementos de VML, arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407688"
---
# <a name="using-predefined-shapes"></a>Usar formas predefinidas

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede usar el elemento `<oval>` de VML para crear un óvalo simple. VML proporciona otros elementos predefinidos. En este tema, se ilustrará cómo dibujar gráficos mediante estos elementos.

En este tema:

-   [Rect](#roundrect)
-   [roundrect](#roundrect)
-   [line](#polyline)
-   [Polilínea](#polyline)
-   [curva](#curve)
-   [Arco](#arc)
-   [Resumen](#summary)

## <a name="rect"></a>rect

Puede usar el elemento `<rect>` para dibujar un rectángulo. A continuación, puede personalizar el rectángulo especificando atributos de propiedad diferentes.

Por ejemplo, puede dibujar un rectángulo que se rellena con azul especificando **fillcolor**="blue" y darle un contorno rojo de 3,5 puntos especificando **strokecolor**="red" **strokeweight**="3.5pt", como se muestra en la siguiente representación de VML:

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . (Nota: La especificación de VML no tiene un marcador para el `<rect>` elemento).

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="roundrect"></a>roundrect

Puede usar el elemento `<roundrect>` para dibujar un rectángulo con esquinas redondeadas. A continuación, puede personalizar el rectángulo redondeado especificando atributos de propiedad diferentes.

Por ejemplo, puede dibujar un rectángulo que tenga esquinas redondeadas al 30 % de la mitad de la dimensión más pequeña del rectángulo especificando **arcsize**="0.3", rellenarlo con amarillo especificando **fillcolor**="yellow" y darle un contorno rojo de 2 puntos especificando **strokecolor**="red" **strokeweight**="2pt", como se muestra en la siguiente representación de VML:

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="line"></a>line

Puede usar el elemento `<line>` para crear una línea recta. A continuación, puede personalizar la línea especificando atributos de propiedad diferentes.

Por ejemplo, puede dibujar una línea horizontal especificando de ="20pt,20pt" a ="100pt,20pt", y hacerlo de 2 puntos y rojo especificando **strokecolor**="red" **strokeweight**="2pt", como se muestra en la siguiente representación de VML:

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Puede dibujar una línea vertical o diagonal simplemente  especificando valores diferentes para los atributos de propiedad from y **to,** como se muestra en la siguiente representación de VML:

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="polyline"></a>Polilínea

Puede usar el elemento para definir formas que se crean a partir `<polyline>` de segmentos de línea conectados. A continuación, puede personalizar la forma especificando atributos de propiedad diferentes.

Por ejemplo, para dibujar la forma que se muestra en la siguiente imagen, puede escribir la siguiente representación de VML:

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="curve"></a>curva

Puede usar el elemento `<curve>` para dibujar una curva bézier cúbica. A continuación, puede personalizar la curva especificando atributos de propiedad diferentes.

Por ejemplo, para dibujar una curva como se muestra en la siguiente imagen, puede escribir la siguiente representación de VML:

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="arc"></a>arc

Puede usar el elemento `<arc>` para dibujar un arco que se define como un segmento de un óvalo. El arco se define mediante la intersección del óvalo con los vectores de radio inicial y final especificados por los ángulos. Los ángulos se calculan mediante las propiedades de un círculo (ancho igual a alto) y, a continuación, se escalan anisotropíamente hasta el ancho y alto deseados.

Por ejemplo, puede dibujar un arco que comience a 0 grados y termine en 90 grados especificando **startangle**="0" **endangle**="90", como se muestra en la siguiente representación de VML:

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Puede cambiar el arco especificando diferentes valores **startangle** y **endangle,** como se muestra en la siguiente representación de VML:

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

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="summary"></a>Resumen

Puede usar elementos predefinidos de VML como , , , , , , y para dibujar gráficos fácilmente en una página web y, a continuación, personalizar esos gráficos simplemente cambiando sus atributos `<oval>` `<line>` de `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` propiedad.

 

 