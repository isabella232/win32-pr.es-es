---
title: Uso del elemento de relleno
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- diseñar páginas web, elemento Fill
- Lenguaje de marcado de vectores (VML), elemento Fill
- VML (Lenguaje de marcado de vectores), elemento Fill
- Vector Graphics, Fill (elemento)
- elemento Fill
- Elementos VML, relleno
- Formas VML, elemento Fill
- Lenguaje de marcado de vectores (VML), relleno degradado
- VML (Lenguaje de marcado de vectores), relleno degradado
- gráficos vectoriales, relleno degradado
- Formas VML, relleno degradado
- formas con relleno degradado
- Lenguaje de marcado de vectores (VML), relleno de patrón
- VML (Lenguaje de marcado de vectores), relleno de patrón
- gráficos vectoriales, relleno de patrón
- Formas VML, relleno de patrón
- formas rellenas de patrones
- Lenguaje de marcado de vectores (VML), relleno de imagen
- VML (Lenguaje de marcado de vectores), relleno de imagen
- gráficos vectoriales, relleno de imagen
- Formas VML, relleno de imagen
- formas rellenas de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104556203"
---
# <a name="using-the-fill-element"></a>Uso del elemento de relleno

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede usar el atributo de propiedad **fillColor** de un elemento de forma predefinido, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --para especificar el color que se utiliza para rellenar la forma. En este tema, se muestra cómo dibujar una forma que se rellena con efectos más avanzados.

Puede colocar el `<fill>` subelemento dentro de `<shape>` , o `<shapetype>` , o cualquier elemento de forma predefinido para describir cómo rellenar la forma. Después, puede usar los atributos de propiedad del `<fill>` subelemento para personalizar el efecto de relleno, como [relleno de degradado](#gradient-fill), [relleno de patrón](#pattern-fill), [relleno de imagen](#picture-fill).

En este tema:

-   [Relleno de degradado](#gradient-fill)
-   [Relleno de patrón](#pattern-fill)
-   [Relleno de imagen](#picture-fill)

## <a name="gradient-fill"></a>Relleno de degradado

Para dibujar una forma con relleno degradado, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "gradient" o "gradientRadial" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **método**, **color2**, **Focus** y **Angle**.

**Ejemplos:**

Para crear una forma con relleno degradado horizontalmente, puede establecer el atributo de la propiedad **Type** en "degradado", como se muestra en la siguiente representación VML:

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Si cambia el atributo de la propiedad **fillColor** de la forma, la forma se rellena con un color diferente. Puede Agregar un segundo color especificando el atributo de la propiedad **color2** del `<fill>` subelemento. Por ejemplo, para crear una forma con relleno degradado de dos colores, puede Agregar un segundo color especificando el atributo de propiedad **color2** del `<fill>` subelemento, tal como se muestra en la siguiente representación VML:

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Puede establecer el atributo de la propiedad del **método** en "linear" o "Sigma" o "any" o "none". El efecto del degradado es ligeramente diferente. Además, puede usar el atributo de propiedad **Angle**,**Focus**,**focussize** o **focusposition** para cambiar el modo en que el degradado va.

**Ejemplos:**

 

Para crear una forma con relleno degradado verticalmente, puede establecer el atributo de propiedad de ángulo en Angle = "-90", como se muestra en la siguiente representación de VML:

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Para crear una forma con relleno degradado desde el movimiento diagonal hacia arriba, puede establecer el atributo de propiedad de **ángulo** en Angle = "-135", como se muestra en la siguiente representación de VML:

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Para crear una forma con relleno degradado desde el movimiento diagonal hacia abajo, puede establecer el atributo de propiedad de **ángulo** en Angle = "-45", como se muestra en la siguiente representación de VML:

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Para crear una forma con relleno degradado desde el centro, puede especificar `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , tal como se muestra en la siguiente representación de VML:

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="pattern-fill"></a>Relleno de patrón

Para dibujar una forma con relleno de patrón, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "pattern" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **src** y **color2**.

**Ejemplos:**

Para crear una forma rellenada con una imagen de patrón, puede especificar el atributo de propiedad de **tipo** en "pattern" y apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón, tal y como se muestra en la siguiente representación de VML:

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Si apunta el atributo de propiedad **src** a un archivo de patrón diferente, puede crear una forma que se rellene con un patrón diferente. Además, puede cambiar el color especificando un valor diferente para el atributo de propiedad **fillColor** o **color2** , tal como se muestra en la siguiente representación de VML:

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="picture-fill"></a>Relleno de imagen

Para dibujar una forma con relleno de imagen, puede establecer el atributo de la propiedad **Type** del `<fill>` subelemento en "Frame" y, a continuación, especificar otros atributos de propiedad del `<fill>` subelemento, como **src** y **color2**.

**Ejemplos:**

Para crear una forma rellenada con un archivo de imagen, puede especificar el atributo de propiedad de **tipo** en "Frame" y, a continuación, apuntar el atributo de la propiedad **src** a la ubicación del archivo de imagen, como se muestra en la siguiente representación de VML:

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Puede crear fácilmente una forma rellenada con una imagen diferente si apunta el atributo de propiedad **src** a otro archivo.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 