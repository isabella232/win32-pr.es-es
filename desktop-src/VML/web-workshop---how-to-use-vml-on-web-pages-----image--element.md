---
title: Usar el elemento Image
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- diseñar páginas web, elemento de imagen
- Lenguaje de marcado de vectores (VML), elemento Image
- VML (Lenguaje de marcado de vectores), elemento de imagen
- gráficos vectoriales, elemento de imagen
- elemento de imagen
- Elementos VML, imagen
- Formas de VML, elemento de imagen
- Lenguaje de marcado de vectores (VML), recortar atributos de propiedad
- VML (Lenguaje de marcado de vectores), atributos de propiedad de recorte
- gráficos vectoriales, recortar atributos de propiedad
- Formas VML, atributos de propiedad de recorte
- recortar atributos de propiedad
- Lenguaje de marcado de vectores (VML), atributo de propiedad de ganancia
- VML (Lenguaje de marcado de vectores), atributo de propiedad de ganancia
- gráficos vectoriales, atributo de propiedad de ganancia
- Formas VML, atributo de propiedad de ganancia
- atributo de propiedad de ganancia
- Lenguaje de marcado de vectores (VML), contraste
- VML (Lenguaje de marcado de vectores), contraste
- gráficos vectoriales, contraste
- Formas VML, contraste
- Lenguaje de marcado de vectores (VML), atributo de propiedad blacklevel
- VML (Lenguaje de marcado de vectores), atributo de propiedad blacklevel
- gráficos vectoriales, atributo de propiedad blacklevel
- Formas VML, atributo de propiedad blacklevel
- atributo de propiedad blacklevel
- Lenguaje de marcado de vectores (VML), brillo
- VML (Lenguaje de marcado de vectores), brillo
- gráficos vectoriales, brillo
- Formas VML, brillo
- Lenguaje de marcado de vectores (VML), atributo de propiedad de escala de grises
- VML (Lenguaje de marcado de vectores), atributo de propiedad de escala de grises
- gráficos vectoriales, atributo de propiedad de escala de grises
- Formas VML, atributo de propiedad de escala de grises
- atributo de propiedad de escala de grises
- Lenguaje de marcado de vectores (VML), atributo de propiedad gamma
- VML (Lenguaje de marcado de vectores), atributo de propiedad gamma
- Vector Graphics, atributo de propiedad gamma
- Formas VML, atributo de propiedad gamma
- atributo de propiedad gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533435"
---
# <a name="using-the-image-element"></a>Usar el elemento Image

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Usar `<image>`

En este tema, se muestra cómo usar el `<image>` elemento para mostrar imágenes con distintos efectos especiales.

Si desea mostrar una imagen que se cargó desde un origen externo, normalmente usaría el `<img>` elemento proporcionado en HTML y, a continuación, apuntaría el atributo de propiedad **src** a la ubicación del archivo de imagen.

También puede usar el `<image>` elemento proporcionado en VML. Cuando se usa el `<image>` elemento, solo se puede crear un archivo de imagen y, a continuación, Mostrar la imagen de forma diferente modificando los atributos de propiedad del `<image>` elemento. Además, el `<image>` elemento proporciona varios efectos especiales que no se pueden realizar mediante el uso del `<img>` elemento de HTML, como el [recorte](#crop), el [contraste](#contrast), el [brillo](#brightness), la [gamma](#gamma)y la [escala de grises](#grayscale).

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="crop"></a>CropBox

Puede usar los atributos de propiedad **CropBottom**, **CropTop**, **CropLeft** y **CropRight** del `<image>` elemento para mostrar diferentes imágenes que se recortan del mismo archivo de imagen.

El valor de estos atributos de recorte representa el porcentaje de corte del borde de la imagen. El valor puede ser cualquier número comprendido entre 0 y 1. De forma predeterminada, el valor se establece en 0, lo que indica que no hay ningún recorte del borde. El valor 0,1 indica un recorte del 10 por ciento del borde, el valor 0,15 indica un recorte del 15 por ciento del borde, y así sucesivamente.

Por ejemplo, para mostrar cinco imágenes recortadas del mismo archivo de imagen, puede usar el `<image>` elemento y especificar valores de recorte diferentes, como se muestra en la siguiente representación de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image1 (1969 bytes)](images/image1-2.jpg)![\-3.jpg image1 (1148 bytes)](images/image1-3.jpg)![\-4.jpg image1 (1686 bytes)](images/image1-4.jpg)![\-5.jpg image1 (1364 bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





La primera imagen, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , no tiene ningún valor de recorte. Por lo tanto, el 100 por ciento de la imagen original se muestra en un tamaño de 100 puntos por 80 puntos.

La segunda imagen, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tiene algunos valores de recorte. `cropbottom="0.2"` indica que el 20 por ciento de la imagen se recortará de la parte inferior; `cropright="0.15"` indica que el 15 por ciento de la imagen se recortará desde el borde derecho. A continuación, se muestra la imagen restante en un tamaño de 85 puntos por 64 puntos.

Del mismo modo, las imágenes tercera, cuarta y quinta tienen algunos valores de recorte. La imagen original se recorta según los valores de recorte y, a continuación, se muestra según el valor de ancho y alto.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="contrast"></a>contraste

Puede usar el atributo de propiedad de **ganancia** del `<image>` elemento para mostrar varias imágenes que tienen diferentes valores de contraste.

El valor del atributo de la propiedad de **ganancia** puede ser cualquier número. De forma predeterminada, el valor es 1, que indica el uso del mismo contraste que la imagen original. El valor 0 indica que no hay ningún contraste. Cuanto mayor sea el número, mayor será el contraste.

Por ejemplo, para mostrar cinco imágenes que tienen una configuración de contraste diferente, puede usar el `<image>` elemento y establecer un valor diferente para el atributo de la propiedad de **ganancia** , como se muestra en la siguiente representación de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image2 (270 bytes)](images/image2-2.jpg)![\-3.jpg image2 (1919 bytes)](images/image2-3.jpg)![\-4.jpg image2 (3143 bytes)](images/image2-4.jpg)![\-5.jpg image2 (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Cuando el atributo de la propiedad de **ganancia** se establece en 0, toda la imagen se vuelve atenuada porque no hay ningún contraste. El contraste es más apreciable cuando el atributo de la propiedad de **ganancia** está establecido en 3 que cuando se establece en 0,5. El contraste se invierte cuando el atributo de la propiedad de **ganancia** está establecido en un valor negativo, como-0,4.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="brightness"></a>luminosidad

Puede usar el atributo de la propiedad **blacklevel** del `<image>` elemento para mostrar varias imágenes que tienen diferentes valores de brillo.

El valor del atributo de la propiedad **blacklevel** puede ser cualquier valor entre 0 y 1. De forma predeterminada, el valor es 0, lo que indica que se conserva el nivel de brillo de la imagen original. El valor 1 indica el nivel más alto de brillo.

Por ejemplo, para mostrar cinco imágenes que tienen una configuración de brillo diferente, puede usar el `<image>` elemento y establecer un valor diferente para el atributo de la propiedad **blacklevel** , como se muestra en la siguiente representación de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image3 (2579 bytes)](images/image3-2.jpg)![\-3.jpg image3 (2330 bytes)](images/image3-3.jpg)![\-4.jpg image3 (2727 bytes)](images/image3-4.jpg)![\-5.jpg image3 (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="grayscale"></a>escala de grises

Puede usar el atributo de la propiedad de **escala de grises** del `<image>` elemento para mostrar imágenes con o sin escala de grises.

El valor del atributo de propiedad de **escala de grises** puede ser true o false. De forma predeterminada, el valor se establece en false para que la imagen se muestre en color. Si el valor se establece en true, la imagen se mostrará en escala de grises.

Por ejemplo, como se muestra en la siguiente imagen, la primera imagen utiliza el valor predeterminado (false) del atributo de escala de grises ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Por lo tanto, la imagen se muestra en color.

La segunda imagen establece el atributo de escala de grises en true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Por lo tanto, la imagen se muestra en escala de grises, tal y como se muestra en la siguiente representación VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg archivo image4 (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="gamma"></a>gamma

Puede usar el atributo de propiedad **Gamma** del `<image>` elemento para mostrar las imágenes que tienen una configuración gamma diferente.

El valor del atributo de propiedad gamma puede ser cualquier valor entre 0 y 1. De forma predeterminada, el valor se establece en 1.

Por ejemplo, para mostrar tres imágenes que tienen una configuración gamma diferente, puede usar el `<image>` elemento y establecer un valor diferente del atributo de propiedad **gamma** , como se muestra en la siguiente representación de VML:

![\-1.jpg image5 (2714 bytes)](images/image5-1.jpg)![\-2.jpg image5 (2729 bytes)](images/image5-2.jpg)![\-3.jpg image5 (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 