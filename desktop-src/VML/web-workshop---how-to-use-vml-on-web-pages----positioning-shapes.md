---
title: Colocar formas
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, colocar formas
- diseñar páginas web, colocar formas
- Lenguaje de marcado de vectores (VML), colocar formas
- VML (Lenguaje de marcado de vectores), colocar formas
- gráficos vectoriales, colocar formas
- Formas VML, posición
- colocar formas
- Lenguaje de marcado de vectores (VML), estilo de posición estática
- VML (Lenguaje de marcado de vectores), estilo de posición estática
- gráficos vectoriales, estilo de posición estática
- estilo de posición estática
- Lenguaje de marcado de vectores (VML), estilo de posición relativo
- VML (Lenguaje de marcado de vectores), estilo de posición relativo
- gráficos vectoriales, estilo de posición relativo
- estilo de posición relativa
- Lenguaje de marcado de vectores (VML), estilo de posición absoluta
- VML (Lenguaje de marcado de vectores), estilo de posición absoluta
- gráficos vectoriales, estilo de posición absoluta
- estilo de posición absoluta
- Lenguaje de marcado de vectores (VML), estilo de posición de índice z
- VML (Lenguaje de marcado de vectores), estilo de posición de índice z
- gráficos vectoriales, estilo de posición de índice z
- estilo de posición de índice z
- Lenguaje de marcado de vectores (VML), estilo de posición de giro
- VML (Lenguaje de marcado de vectores), estilo de posición de giro
- gráficos vectoriales, estilo de posición de giro
- estilo de posición de giro
- Lenguaje de marcado de vectores (VML), estilo de posición de volteo
- VML (Lenguaje de marcado de vectores), estilo de posición de volteo
- gráficos vectoriales, estilo de posición de volteo
- estilo de posición de volteo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077909"
---
# <a name="positioning-shapes"></a>Colocar formas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Ha aprendido cómo dibujar y colorear formas en una página web mediante VML. En este tema, usará VML para colocar los gráficos de forma precisa en una página web.

VML usa la misma sintaxis definida en las secciones [modelo de cuadro](https://www.w3.org/TR/PR-CSS2/box.mdl) y modelo de [representación visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para colocar formas en una página web. Puede utilizar [static](#static), [relative](#relative)o [Absolute](#absolute) para determinar dónde se encuentra el punto base en una página web. Después, puede usar los atributos de estilo **superior** e **izquierdo** para especificar el desplazamiento desde el punto base en el que se colocará el cuadro contenedor de la forma.

También puede utilizar [z-index](#z-index) para especificar el orden z de las formas en una página web.

Además, VML proporciona [rotación](#rotation) y [volteo](#flip) para girar o voltear formas.

En este tema:

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [índice z](#z-index)
-   [Rotation](#rotation)
-   [flip](#flip)
-   [Resumen](#summary)

## <a name="static"></a>static

El estilo de posición predeterminado es estático, que indica a los exploradores que coloquen la forma en el punto actual (el punto base) en el flujo de texto y omitan los valores de los atributos de estilo **superior** e **izquierdo** .

Por ejemplo, en la siguiente representación VML, el óvalo rojo se coloca inmediatamente después del texto "Inicio de la forma:", tal como se muestra en la siguiente imagen:

![\-ps.gif shape1 (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="relative"></a>relative

Establecer el atributo de estilo de posición en "Relative" permite colocar el cuadro contenedor con un desplazamiento desde el punto actual (el punto base) en el flujo de texto. El desplazamiento viene determinado por los valores de los atributos de estilo **superior** e **izquierdo** . Tenga en cuenta que el cuadro contenedor que se coloca como relativo ocupa espacio en el flujo de texto.

Por ejemplo, en la siguiente representación VML, el óvalo rojo se coloca 20 puntos desde la izquierda y 10 puntos desde la parte superior respecto al punto actual en el flujo de texto, tal como se muestra en la siguiente imagen:

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="absolute"></a>absolute

Al establecer el atributo de estilo de posición en "Absolute", se puede colocar el cuadro contenedor en una distancia exacta desde la esquina superior izquierda (el punto base) de su elemento primario (el elemento colocado que contiene la forma). Tenga en cuenta que el cuadro contenedor que se coloca como absoluto no ocupa espacio en el flujo de texto.

Por ejemplo, en la siguiente representación VML, el óvalo rojo está contenido dentro del `<body>` elemento (toda la página web); por lo tanto, el punto base se encuentra en la esquina superior izquierda de la Página Web. El cuadro contenedor del óvalo está colocado exactamente 20 puntos desde la izquierda y 10 puntos desde la parte superior, con respecto a la esquina superior izquierda de la página web, como se muestra en la siguiente imagen:

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="z-index"></a>z-index

Es posible colocar una forma que se solape con otra forma. Normalmente, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.

En VML, puede controlar el orden z mediante el atributo de estilo **z-index** . El valor de este atributo puede ser cero, un entero positivo o un entero negativo. El gráfico que tiene un valor de índice z mayor se muestra en la parte superior del gráfico que tiene un valor de índice z más pequeño. Cuando ambos gráficos tienen el mismo valor de índice z, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.

Por ejemplo, en la siguiente representación VML, el óvalo rojo se muestra en la parte superior del rectángulo azul. Esto se debe a que el valor de índice z del óvalo rojo es mayor que el valor de índice z del rectángulo azul.

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Si cambia el índice z, tal y como se muestra en la siguiente representación VML, el óvalo rojo se moverá detrás del rectángulo azul.

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Si proporciona un entero negativo, puede usar el índice z para colocar los gráficos detrás del flujo de texto normal, tal como se muestra en la siguiente representación de VML.

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="rotation"></a>giro

Puede usar el atributo de estilo de **rotación** para especificar el número de grados que desea que una forma Active su eje. Un valor positivo indica un giro en el sentido de las agujas del reloj; un valor negativo indica un giro en el sentido contrario a las agujas del reloj.

Por ejemplo, si especifica **Style**= '... rotación: 90 ', puede girar la forma 90 grados en el sentido de las agujas del reloj.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="flip"></a>voltear

Puede usar el atributo de estilo **Flip** para voltear una forma en su eje x o y según la tabla siguiente:



| Value | Descripción                                                  |
|-------|--------------------------------------------------------------|
| x     | Voltear la forma girada sobre el eje y (invertir coordenadas x) |
| y     | Voltear la forma girada sobre el eje x (invertir las coordenadas y) |



 

Tanto x como y se pueden especificar en la propiedad flip.

Por ejemplo, si escribe **Style**= '... Flip: x y ', se volteará la forma en el eje x e y.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="summary"></a>Resumen

En función de lo que haya aprendido, puede colocar una forma con precisión en una página web siguiendo estos pasos:

1.  Decida dónde desea que aparezca la forma en una página web y el tamaño de la forma.
2.  Especifique **Style**= ' Position: relative (o Relative) ' para determinar el punto base.
3.  Use **left** y **Top** para especificar el desplazamiento desde el punto base.
4.  Use **ancho** y **alto** para especificar el tamaño del cuadro contenedor de la forma.
5.  Utilice **z-index** para especificar el orden z de la forma.

 

 