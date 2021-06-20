---
title: Uso del elemento Image
description: En este artículo se describe el uso del elemento Image en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Taller web, elemento image
- diseñar páginas web, elemento image
- Lenguaje de marcado de vectores (VML),elemento image
- VML (Lenguaje de marcado de vectores),elemento image
- gráficos vectoriales, elemento image
- elemento de imagen
- Elementos de VML, imagen
- Formas de VML, elemento image
- Lenguaje de marcado de vectores (VML), atributos de propiedad de recorte
- VML (Lenguaje de marcado de vectores), atributos de propiedad de recorte
- gráficos vectoriales, atributos de propiedad de recorte
- Formas de VML, atributos de propiedad de recorte
- atributos de propiedad de recorte
- Lenguaje de marcado de vectores (VML),atributo de propiedad gain
- VML (Lenguaje de marcado de vectores),atributo de propiedad gain
- vector graphics,gain property attribute
- Formas de VML, atributo de propiedad gain
- atributo de propiedad gain
- Lenguaje de marcado de vectores (VML),contrast
- VML (Lenguaje de marcado de vectores),contrast
- gráficos vectoriales, contraste
- Formas de VML, contraste
- Lenguaje de marcado de vectores (VML),atributo de propiedad blacklevel
- VML (Lenguaje de marcado de vectores),atributo de propiedad blacklevel
- vector graphics,blacklevel property attribute
- Formas de VML, atributo de propiedad blacklevel
- atributo de propiedad blacklevel
- Lenguaje de marcado de vectores (VML),brillo
- VML (Lenguaje de marcado de vectores),brillo
- gráficos vectoriales, brillo
- Formas de VML, brillo
- Lenguaje de marcado de vectores (VML), atributo de propiedad de escala de grises
- VML (Lenguaje de marcado de vectores), atributo de propiedad de escala de grises
- gráficos vectoriales, atributo de propiedad de escala de grises
- Atributo de propiedad formas de VML, escala de grises
- atributo de propiedad de escala de grises
- Lenguaje de marcado de vectores (VML),atributo de propiedad gamma
- VML (Lenguaje de marcado de vectores),atributo de propiedad gamma
- vector graphics,gamma property attribute
- Formas de VML, atributo de propiedad gamma
- atributo de propiedad gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407808"
---
# <a name="using-the-image-element"></a>Uso del elemento Image

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Usar `<image>`

En este tema, se muestra cómo usar el `<image>` elemento para mostrar imágenes con varios efectos especiales.

Si quisiera mostrar una imagen cargada desde un origen externo, normalmente usaría el elemento proporcionado en HTML y, a continuación, apuntaría el atributo de propiedad src a la ubicación del archivo `<img>` de imagen. 

También puede usar el elemento `<image>` proporcionado en VML. Cuando se usa el elemento , solo se puede crear un archivo de imagen y, a continuación, mostrar la imagen de forma diferente modificando los atributos `<image>` de propiedad del `<image>` elemento. Además, el elemento proporciona varios efectos especiales que no puede hacer simplemente con el elemento de HTML, como recortar , contraste, brillo, gamma y escala `<image>` `<img>` de [](#brightness) [grises.](#grayscale) [](#crop) [](#contrast) [](#gamma)

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="crop"></a>Cultivo

Puede usar los atributos de propiedad **cropbottom**, **croptop,** **cropleft** y **cropright** del elemento para mostrar imágenes diferentes recortadas del mismo archivo `<image>` de imagen.

El valor de estos atributos de recorte representa el porcentaje de corte del borde de la imagen. El valor puede ser cualquier número entre 0 y 1. De forma predeterminada, el valor se establece en 0, lo que indica que no se recorta desde el borde. El valor 0,1 indica un recorte del 10 % desde el borde, el valor 0,15 indica un recorte del 15 % desde el borde, y así sucesivamente.

Por ejemplo, para mostrar cinco imágenes recortadas del mismo archivo de imagen, puede usar el elemento y especificar distintos valores de recorte, como se muestra en la siguiente representación `<image>` de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![image1 \-2.jpg (1969 bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 bytes)](images/image1-5.jpg)


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





La primera imagen, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , no tiene ningún valor de recorte. Por lo tanto, el 100 % de la imagen original se muestra con un tamaño de 100 puntos por 80 puntos.

La segunda imagen, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tiene algunos valores de recorte. `cropbottom="0.2"` indica que el 20 por ciento de la imagen se recortará desde la parte inferior; `cropright="0.15"` indica que el 15 por ciento de la imagen se recortará desde el borde derecho. A continuación, la imagen restante se muestra con un tamaño de 85 puntos por 64 puntos.

De forma similar, las imágenes tercera, cuarta y quinta tienen algunos valores de recorte. La imagen original se recorta según los valores de recorte y, a continuación, se muestra según el valor de ancho y alto.

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="contrast"></a>contraste

Puede usar el atributo de propiedad **gain** del `<image>` elemento para mostrar varias imágenes con diferentes configuraciones de contraste.

El valor del atributo de propiedad **gain** puede ser cualquier número. De forma predeterminada, el valor es 1, lo que indica el uso del mismo contraste que la imagen original. El valor 0 indica que no hay contraste. Cuanto mayor sea el número, mayor será el contraste.

Por ejemplo, para mostrar cinco imágenes que tienen una configuración de contraste diferente, puede usar el elemento y establecer un valor diferente para el atributo de propiedad gain, como se muestra en la siguiente representación `<image>` de VML: 

![image1.jpg (5770 bytes)](images/image1.jpg)![image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![imagen2 \-3.jpg (1919 bytes)](images/image2-3.jpg)![imagen2 \-4.jpg (3143 bytes)](images/image2-4.jpg)![imagen2 \-5.jpg (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Cuando el **atributo de** propiedad gain se establece en 0, toda la imagen se vuelve gris porque no hay contraste. El contraste es más evidente cuando el atributo de propiedad **gain** se establece en 3 que cuando se establece en 0,5. El contraste se invierte cuando el atributo de propiedad **gain** se establece en un valor negativo como -0,4.

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="brightness"></a>luminosidad

Puede usar el atributo **de propiedad blacklevel** del elemento para mostrar `<image>` varias imágenes que tienen una configuración de brillo diferente.

El valor del atributo **de propiedad blacklevel** puede ser cualquier valor entre 0 y 1. De forma predeterminada, el valor es 0, lo que indica que se conserva el nivel de brillo de la imagen original. El valor 1 indica el nivel más alto de brillo.

Por ejemplo, para mostrar cinco imágenes que tienen una configuración de brillo diferente, puede usar el elemento y establecer un valor diferente para el atributo de propiedad blacklevel, como se muestra en la siguiente representación `<image>` de VML: 

![image1.jpg (5770 bytes)](images/image1.jpg)![image3 \-2.jpg (2579 bytes)](images/image3-2.jpg)![imagen3 \-3.jpg (2330 bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="grayscale"></a>escala de grises

Puede usar el atributo **de propiedad de escala** de grises del elemento para mostrar imágenes con o sin escala de `<image>` grises.

El valor del atributo **de propiedad de escala** de grises puede ser true o false. De forma predeterminada, el valor se establece en false para que la imagen se muestre en color. Si el valor se establece en true, la imagen se mostrará en escala de grises.

Por ejemplo, como se muestra en la imagen siguiente, la primera imagen usa la configuración predeterminada (false) del atributo de escala de grises ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Por lo tanto, la imagen se muestra en color.

La segunda imagen establece el atributo de escala de grises en true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Por lo tanto, la imagen se muestra en escala de grises, como se muestra en la siguiente representación de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![image4 \-2.jpg (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="gamma"></a>gamma

Puede usar el atributo de propiedad **gamma** del elemento para mostrar imágenes `<image>` con diferentes configuraciones gamma.

El valor del atributo de propiedad gamma puede ser cualquier valor entre 0 y 1. De forma predeterminada, el valor se establece en 1.

Por ejemplo, para mostrar tres imágenes que tienen una configuración gamma diferente, puede usar el elemento y establecer un valor diferente del atributo de propiedad gamma, como se muestra en la siguiente representación `<image>` de VML: 

![image5 \-1.jpg (2714 bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 