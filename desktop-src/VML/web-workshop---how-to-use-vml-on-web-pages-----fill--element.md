---
title: Uso del elemento de relleno
description: En este artículo se describe el uso del elemento Fill de VML, una característica que está en desuso a partir Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Taller web, elemento fill
- diseñar páginas web, elemento fill
- Lenguaje de marcado de vectores (VML),elemento fill
- VML (Lenguaje de marcado de vectores),elemento fill
- vector graphics,fill element
- elemento fill
- Elementos VML, fill
- Formas de VML, elemento fill
- Lenguaje de marcado de vectores (VML), relleno de degradado
- VML (Lenguaje de marcado de vectores), relleno de degradado
- gráficos vectoriales, relleno de degradado
- Formas de VML, relleno de degradado
- formas rellenas de degradado
- Lenguaje de marcado de vectores (VML), relleno de patrón
- VML (Lenguaje de marcado de vectores), relleno de patrones
- gráficos vectoriales, relleno de patrón
- Formas de VML, relleno de patrón
- formas rellenas de patrones
- Lenguaje de marcado de vectores (VML),relleno de imagen
- VML (Lenguaje de marcado de vectores), relleno de imagen
- gráficos vectoriales, relleno de imagen
- Formas de VML, relleno de imagen
- formas rellenas de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f6b3e0c92989e037ebf9b95b7bd726134b9099dd5d3755ff4588f7e970586c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057305"
---
# <a name="using-the-fill-element"></a>Uso del elemento de relleno

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede usar el atributo de propiedad **fillcolor** de un elemento de forma predefinido, como , , , , , , , para especificar el color que se usa para rellenar la `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. En este tema, se ilustrará cómo dibujar una forma que se rellena con efectos más avanzados.

Puede colocar el sub element dentro de , o , o cualquier elemento de forma predefinido para `<fill>` describir cómo rellenar la `<shape>` `<shapetype>` forma. A continuación, puede usar los atributos de propiedad del sub elemento para personalizar el efecto de relleno, como relleno de `<fill>` [degradado,](#gradient-fill)relleno [de](#pattern-fill)patrón, relleno [de imagen.](#picture-fill)

En este tema:

-   [Relleno de degradado](#gradient-fill)
-   [Relleno de patrón](#pattern-fill)
-   [Relleno de imagen](#picture-fill)

## <a name="gradient-fill"></a>Relleno de degradado

Para dibujar una forma rellena de  degradado, puede establecer el atributo de propiedad type del sub element en "gradient" o "gradientRadial" y, a continuación, especificar otros atributos de propiedad del sub element, como el método `<fill>` `<fill>` , **color2**,  **focus** y **angle**.

**Ejemplos:**

Para crear una forma con relleno de degradado  horizontalmente, puede establecer el atributo de propiedad de tipo en "degradado", como se muestra en la siguiente representación de VML:

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Si cambia el atributo **de propiedad fillcolor** de la forma, la forma se rellena con degradado con un color diferente. Puede agregar un segundo color especificando el atributo de propiedad **color2** del `<fill>` sub elemento. Por ejemplo, para crear una forma que se rellena con degradado en dos colores, puede agregar un segundo color especificando el atributo de propiedad **color2** del sub elemento, como se muestra en la siguiente representación `<fill>` de VML:

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Puede establecer el atributo **de propiedad** del método en "linear" o "sigma", "any" o "none". El efecto del degradado es ligeramente diferente. Además, puede usar el atributo de propiedad **angle**,**focus**,**focussize** o **focusposition** para cambiar cómo va el degradado.

**Ejemplos:**

 

Para crear una forma que se rellena verticalmente con degradado, puede establecer el atributo de propiedad de ángulo en angle="-90", como se muestra en la siguiente representación de VML:

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Para crear una forma que se rellena con degradado  desde la diagonal hacia arriba, puede establecer el atributo de propiedad de ángulo en angle="-135", como se muestra en la siguiente representación de VML:

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Para crear una forma rellena de degradado desde la  diagonal hacia abajo, puede establecer el atributo de propiedad de ángulo en angle="-45", como se muestra en la siguiente representación de VML:

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Para crear una forma rellena de degradado desde el centro, puede especificar , como se `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` muestra en la siguiente representación de VML:

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="pattern-fill"></a>Relleno de patrón

Para dibujar una forma rellena de  patrón, puede establecer el atributo de propiedad type del sub element en "pattern" y, a continuación, especificar otros atributos de propiedad del sub element, como `<fill>` `<fill>` **src** **y color2.**

**Ejemplos:**

Para crear una forma que se rellena con  una imagen de patrón, puede especificar el atributo de propiedad type en "pattern" y apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen de patrón, como se muestra en la siguiente representación de VML:

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Si apunta el atributo **de propiedad src** a un archivo de patrón diferente, puede crear una forma que se rellena con un patrón diferente. Además, puede cambiar el color especificando un valor diferente para el atributo de propiedad **fillcolor** o **color2,** como se muestra en la siguiente representación de VML:

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="picture-fill"></a>Relleno de imagen

Para dibujar una forma rellena de  imagen, puede establecer el atributo de propiedad type del sub elemento en "frame" y, a continuación, especificar otros atributos de propiedad del sub element, como `<fill>` `<fill>` **src** y **color2.**

**Ejemplos:**

Para crear una forma que se rellena con  un archivo de imagen, puede especificar el atributo de propiedad type en "frame" y, a continuación, apuntar el atributo de propiedad **src** a la ubicación del archivo de imagen, como se muestra en la siguiente representación de VML:

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Puede crear fácilmente una forma que se rellena con una imagen diferente señalando el atributo de propiedad **src** a otro archivo.

Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 