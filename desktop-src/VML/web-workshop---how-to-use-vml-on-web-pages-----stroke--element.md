---
title: Usar el elemento stroke
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, Stroke (elemento)
- diseñar páginas web, elemento stroke
- Lenguaje de marcado de vectores (VML), elemento stroke
- VML (Lenguaje de marcado de vectores), elemento stroke
- Vector Graphics, Stroke (elemento)
- elemento stroke
- Elementos VML, trazo
- Formas VML, elemento stroke
- Lenguaje de marcado de vectores (VML), atributo de propiedad DashStyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad DashStyle
- gráficos vectoriales, atributo de propiedad DashStyle
- DashStyle (atributo de propiedad)
- Lenguaje de marcado de vectores (VML), atributo de propiedad Opacity
- VML (Lenguaje de marcado de vectores), atributo de propiedad Opacity
- gráficos vectoriales, atributo de propiedad Opacity
- atributo de propiedad Opacity
- Lenguaje de marcado de vectores (VML), atributo de propiedad lineStyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad lineStyle
- gráficos vectoriales, atributo de propiedad lineStyle
- atributo de propiedad lineStyle
- Lenguaje de marcado de vectores (VML), atributo de propiedad joinstyle
- VML (Lenguaje de marcado de vectores), atributo de propiedad joinstyle
- gráficos vectoriales, atributo de propiedad joinstyle
- atributo de propiedad joinstyle
- Lenguaje de marcado de vectores (VML), atributo de propiedad filltype
- VML (Lenguaje de marcado de vectores), atributo de propiedad filltype
- gráficos vectoriales, atributo de propiedad filltype
- atributo de propiedad filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359380"
---
# <a name="using-the-stroke-element"></a>Usar el elemento stroke

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Usar `<stroke>`

Como ha aprendido, puede usar los atributos de la propiedad **StrokeColor** y **strokeweight** de una forma predefinida, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --para especificar el color y el grosor del contorno de una forma. En este tema, se muestra cómo dibujar una forma que tiene un esquema más avanzado.

Puede colocar el `<stroke>` subelemento dentro de `<shape>` , o `<shapetype>` , o cualquier elemento de forma predefinido para describir cómo dibujar el contorno de la forma. Después, puede usar los atributos de propiedad (por ejemplo, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) ) del `<stroke>` subelemento para personalizar el esquema.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="dashstyle"></a>DashStyle

Puede usar el atributo de propiedad **DashStyle** del `<stroke>` subelemento para dibujar un contorno con varios estilos de guión.

**Ejemplos:**

Si especifica `<v:stroke dashstyle="solid" />` dentro del `<line>` elemento, puede crear una línea sólida, tal como se muestra en la siguiente representación de VML:

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Si cambia el atributo de la propiedad **DashStyle** a "dot", puede crear una línea de puntos, como se muestra en la siguiente representación de VML:

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Si cambia el atributo de la propiedad **DashStyle** a "Dash", puede crear una línea de guiones, tal y como se muestra en la siguiente representación de VML:

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Si cambia el atributo de la propiedad **DashStyle** a "dashDot", puede crear una línea con un estilo de puntos y guiones, tal y como se muestra en la siguiente representación de VML:

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Si cambia el atributo de la propiedad **DashStyle** a "longdash", puede crear una línea con un estilo largo discontinuo, tal como se muestra en la siguiente representación de VML:

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Si cambia el atributo de la propiedad **DashStyle** a "longdashdot", puede crear una línea con un estilo de puntos y guiones largos, tal y como se muestra en la siguiente representación de VML:

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Si coloca `<v:stroke dashstyle="dashdot" />` dentro del `<rect>` elemento, puede crear un rectángulo con un contorno discontinuo y punteado, tal y como se muestra en la siguiente representación de VML:

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="opacity"></a>opacidad

Puede usar el atributo de propiedad **Opacity** del `<stroke>` subelemento para dibujar un contorno con varios estilos de opacidad. El valor del atributo de la propiedad **Opacity** puede ser cualquier número entre 0 y 1. De forma predeterminada, es 1, lo que indica una opacidad completa.

**Ejemplos:**

La siguiente representación de VML crea una línea con una opacidad completa:

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Si agrega `<v:stroke opacity="0.5" />` dentro del `<line>` elemento, puede crear una línea con una opacidad del 50%, tal como se muestra en la siguiente representación de VML:

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="linestyle"></a>lineStyle

Puede usar el atributo de propiedad **LineStyle** del `<stroke>` subelemento para dibujar un contorno con varios estilos de línea.

**Ejemplos:**

Si especifica `<v:stroke linestyle="single" />` dentro del `<rect>` elemento, puede crear un rectángulo con un solo esquema, tal y como se muestra en la siguiente representación de VML:

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Si cambia el atributo de la propiedad **LineStyle** a "thinthin", puede crear un rectángulo con el contorno (1:1:1), tal y como se muestra en la siguiente representación de VML:

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Si cambia el atributo de la propiedad **LineStyle** a "thinthick", puede crear un rectángulo con el contorno (1:1:2), tal y como se muestra en la siguiente representación de VML:

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Si cambia el atributo de la propiedad **LineStyle** a "thickthin", puede crear un rectángulo con el contorno (2:1:1), tal y como se muestra en la siguiente representación de VML:

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Si cambia el atributo de la propiedad **LineStyle** a "thickbetweenthin", puede crear un rectángulo con el contorno (1:1:2:1:1), tal y como se muestra en la siguiente representación de VML:

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="joinstyle"></a>joinstyle

Puede usar el atributo **joinstyle** del `<stroke>` subelemento para definir cómo se unen las líneas.

Por ejemplo, para crear una forma que tenga el esquema de combinación redonda, tal y como se muestra en la siguiente ilustración, puede especificar `<v:stroke joinstyle="round" />` dentro del `<polyline>` elemento, como se muestra en la siguiente representación de VML:

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Si cambia el atributo de la propiedad **joinstyle** a "Bevel", puede crear una forma que tenga el contorno de la unión biselada, tal como se muestra en la siguiente representación VML:

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Si cambia el atributo de la propiedad **joinstyle** a "inglete", puede crear una forma que tenga el contorno de unión angular, tal como se muestra en la siguiente representación de VML:

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="filltype"></a>filltype

Puede usar el atributo de la propiedad **filltype** del `<stroke>` subelemento para dibujar un contorno con varios efectos de relleno.

**Ejemplos:**

Si especifica `<v:stroke filltype="solid" />` dentro del `<roundrect>` elemento, puede crear un rectángulo redondeado con el contorno sólido relleno, tal como se muestra en la siguiente representación de VML:

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Si cambia el atributo de la propiedad **filltype** a "pattern", apunte el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón y establezca el atributo de propiedad **color2** en el segundo color de patrón, puede crear un rectángulo redondeado con un contorno de patrón, tal como se muestra en la siguiente representación VML:

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Si cambia el atributo de la propiedad **filltype** a "Tile" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un esquema en mosaico, tal como se muestra en la siguiente representación VML:

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Si cambia el atributo de la propiedad **filltype** a "Frame" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno de imagen, como se muestra en la siguiente representación VML:

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 