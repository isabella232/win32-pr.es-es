---
title: Usar el elemento Stroke
description: En este artículo se describe el uso del elemento Stroke de VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Taller web, elemento de trazo
- diseñar páginas web, elemento de trazo
- Lenguaje de marcado de vectores (VML), elemento stroke
- VML (Lenguaje de marcado de vectores),elemento stroke
- gráficos vectoriales, elemento de trazo
- elemento stroke
- Elementos vml, trazo
- Formas de VML, elemento de trazo
- Lenguaje de marcado de vectores (VML),atributo de propiedad dashstyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad dashstyle
- vector graphics,dashstyle property attribute
- atributo de propiedad dashstyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad opacity
- VML (Lenguaje de marcado de vectores),atributo de propiedad opacity
- vector graphics,opacity property attribute
- Atributo de propiedad opacity
- Lenguaje de marcado de vectores (VML),atributo de propiedad linestyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad linestyle
- vector graphics,linestyle property attribute
- Atributo de propiedad linestyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad joinstyle
- VML (Lenguaje de marcado de vectores),atributo de propiedad joinstyle
- vector graphics,joinstyle property attribute
- atributo de propiedad joinstyle
- Lenguaje de marcado de vectores (VML),atributo de propiedad filltype
- VML (Lenguaje de marcado de vectores),atributo de propiedad filltype
- vector graphics,filltype property attribute
- atributo de propiedad filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407848"
---
# <a name="using-the-stroke-element"></a>Usar el elemento Stroke

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Usar `<stroke>`

Como ha aprendido, puede usar los atributos de propiedad **strokecolor** y **strokeweight** de una forma predefinida( como , , , , , , , ) para especificar el color y el peso del contorno de una `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. En este tema, se muestra cómo dibujar una forma que tiene un esquema más avanzado.

Puede colocar el sub element dentro de , o , o cualquier elemento de forma predefinido para describir cómo dibujar el `<stroke>` `<shape>` contorno de la `<shapetype>` forma. A continuación, puede usar los atributos de propiedad ( por ejemplo, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype)](#filltype) del `<stroke>` sub-elemento para personalizar el esquema.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="dashstyle"></a>dashstyle

Puede usar el atributo **de propiedad dashstyle** del `<stroke>` sub elemento para dibujar un esquema con varios estilos de guion.

**Ejemplos:**

Si especifica dentro `<v:stroke dashstyle="solid" />` del elemento , puede crear una línea `<line>` sólida, como se muestra en la siguiente representación de VML:

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Si cambia el atributo de **propiedad dashstyle** a "punto", puede crear una línea de puntos, como se muestra en la siguiente representación de VML:

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Si cambia el atributo de **propiedad dashstyle** a "dash", puede crear una línea de guiones, como se muestra en la siguiente representación de VML:

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Si cambia el atributo de propiedad **dashstyle** a "dashdot", puede crear una línea con un estilo discontinuo y de puntos, como se muestra en la siguiente representación de VML:

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Si cambia el atributo de propiedad **dashstyle** a "longdash", puede crear una línea con un estilo discontinuo largo, como se muestra en la siguiente representación de VML:

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Si cambia el atributo de propiedad **dashstyle** a "longdashdot", puede crear una línea con un estilo largo discontinuo y de puntos, como se muestra en la siguiente representación de VML:

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Si coloca dentro del elemento , puede crear un rectángulo que tenga un contorno discontinuo y de puntos, como se muestra `<v:stroke dashstyle="dashdot" />` en la siguiente representación de `<rect>` VML:

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="opacity"></a>opacidad

Puede usar el atributo **de propiedad de** opacidad del sub elemento para dibujar un esquema con varios estilos de `<stroke>` opacidad. El valor del atributo **de propiedad de** opacidad puede ser cualquier número entre 0 y 1. De forma predeterminada, es 1, lo que indica una opacidad completa.

**Ejemplos:**

La siguiente representación de VML crea una línea con opacidad completa:

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Si agrega dentro del elemento , puede crear una línea con una opacidad del 50 %, como se muestra `<v:stroke opacity="0.5" />` en la siguiente representación de `<line>` VML:

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="linestyle"></a>linestyle

Puede usar el atributo **de propiedad linestyle** del `<stroke>` sub elemento para dibujar un contorno con varios estilos de línea.

**Ejemplos:**

Si especifica dentro del elemento , puede crear un rectángulo con un único contorno, como se `<v:stroke linestyle="single" />` muestra en la siguiente representación de `<rect>` VML:

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Si cambia el atributo de propiedad **linestyle** a "thinthin", puede crear un rectángulo con el contorno (1:1:1), como se muestra en la siguiente representación de VML:

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Si cambia el atributo de propiedad **linestyle** a "thinthick", puede crear un rectángulo con el contorno (1:1:2), como se muestra en la siguiente representación de VML:

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Si cambia el atributo de propiedad **linestyle** a "thickthin", puede crear un rectángulo con el contorno (2:1:1), como se muestra en la siguiente representación de VML:

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Si cambia el atributo de propiedad **linestyle** a "thickbetweenthin", puede crear un rectángulo con el contorno (1:1:2:1:1), como se muestra en la siguiente representación de VML:

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="joinstyle"></a>joinstyle

Puede usar el atributo **joinstyle** del `<stroke>` sub-elemento para definir cómo se unen las líneas.

Por ejemplo, para crear una forma que tenga el contorno de combinación redondeada, como se muestra en la ilustración siguiente, puede especificar dentro del elemento , como se muestra en la siguiente representación `<v:stroke joinstyle="round" />` `<polyline>` de VML:

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Si cambia el atributo de propiedad **joinstyle** a "bevel", puede crear una forma que tenga el contorno bevel-join, como se muestra en la siguiente representación de VML:

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Si cambia el atributo de propiedad **joinstyle** a "miter", puede crear una forma que tenga el contorno de combinación de miter, como se muestra en la siguiente representación de VML:

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="filltype"></a>filltype

Puede usar el atributo **de propiedad filltype** del `<stroke>` sub elemento para dibujar un esquema con varios efectos de relleno.

**Ejemplos:**

Si especifica dentro del elemento , puede crear un rectángulo redondeado con el contorno relleno sólido, como se muestra `<v:stroke filltype="solid" />` en la siguiente representación de `<roundrect>` VML:

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Si cambia el atributo de propiedad **filltype** a "pattern", apunta el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón y establece el atributo de propiedad **color2** en el segundo color de patrón, puede crear un rectángulo redondeado con un contorno de patrón, como se muestra en la siguiente representación de VML:

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Si cambia el atributo de propiedad **filltype** a "tile" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno en mosaico, como se muestra en la siguiente representación de VML:

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Si cambia el atributo de propiedad **filltype** a "frame" y apunta el atributo de propiedad **src** a la ubicación del archivo de imagen, puede crear un rectángulo redondeado con un contorno de imagen, como se muestra en la siguiente representación de VML:

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 