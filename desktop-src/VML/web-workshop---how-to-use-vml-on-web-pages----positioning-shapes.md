---
title: Formas de posicionamiento
description: En este artículo se describe el posicionamiento de formas en VML, una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Taller web, colocación de formas
- diseñar páginas web, colocar formas
- Lenguaje de marcado de vectores (VML),formas de posicionamiento
- VML (Lenguaje de marcado de vectores), formas de posicionamiento
- gráficos vectoriales, formas de posicionamiento
- Formas de VML, posicionamiento
- formas de posicionamiento
- Lenguaje de marcado de vectores (VML), estilo de posición estática
- VML (Lenguaje de marcado de vectores), estilo de posición estática
- gráficos vectoriales, estilo de posición estática
- estilo de posición estática
- Lenguaje de marcado de vectores (VML), estilo de posición relativa
- VML (Lenguaje de marcado de vectores), estilo de posición relativa
- gráficos vectoriales, estilo de posición relativa
- estilo de posición relativa
- Lenguaje de marcado de vectores (VML), estilo de posición absoluta
- VML (Lenguaje de marcado de vectores), estilo de posición absoluta
- gráficos vectoriales, estilo de posición absoluta
- estilo de posición absoluta
- Lenguaje de marcado de vectores (VML), estilo de posición de índice z
- VML (Lenguaje de marcado de vectores), estilo de posición de índice z
- gráficos vectoriales, estilo de posición de índice z
- Estilo de posición de índice z
- Lenguaje de marcado de vectores (VML), estilo de posición de rotación
- VML (Lenguaje de marcado de vectores), estilo de posición de rotación
- gráficos vectoriales, estilo de posición de rotación
- estilo de posición de rotación
- Lenguaje de marcado de vectores (VML), estilo de posición de volteo
- VML (Lenguaje de marcado de vectores), estilo de posición de volteo
- gráficos vectoriales, estilo de posición de volteo
- estilo de posición de volteo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407718"
---
# <a name="positioning-shapes"></a>Formas de posicionamiento

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ha aprendido a dibujar y colorear formas en una página web mediante VML. En este tema, usará VML para colocar con precisión los gráficos en una página web.

VML usa la misma sintaxis definida en las secciones [Modelo de Box](https://www.w3.org/TR/PR-CSS2/box.mdl) y Modelo de Representación [visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para colocar formas en una página web. Puede usar [estáticos,](#static) [relativos](#relative)o [absolutos](#absolute) para determinar dónde se encuentra el punto base en una página web. A continuación, puede  usar **los** atributos de estilo superior e izquierdo para especificar el desplazamiento desde el punto base en el que se colocará el cuadro de contenido de la forma.

También puede usar [z-index para](#z-index) especificar el orden Z de las formas en una página web.

Además, VML proporciona rotación [y](#rotation) [volteo para](#flip) girar o voltear formas.

En este tema:

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [z-index](#z-index)
-   [Rotación](#rotation)
-   [flip](#flip)
-   [Resumen](#summary)

## <a name="static"></a>static

El estilo de posición predeterminado es estático, que indica a los exploradores que coloquen la forma  en  el punto actual (el punto base) en el flujo de texto y omitan la configuración de los atributos de estilo superior e izquierdo.

Por ejemplo, en la siguiente representación de VML, el óvalo rojo se coloca inmediatamente después del texto "Principio de la forma:", como se muestra en la siguiente imagen:

![shape1 \-ps.gif (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="relative"></a>relative

Establecer el atributo de estilo de posición en "relativo" permite colocar el cuadro de contenido con un desplazamiento desde el punto actual (el punto base) en el flujo de texto. El desplazamiento viene determinado por la configuración de los **atributos de** estilo superior **e** izquierdo. Tenga en cuenta que el cuadro de contenido que se coloca como relativo ocupa espacio en el flujo de texto.

Por ejemplo, en la siguiente representación de VML, el óvalo rojo se coloca a 20 puntos de la izquierda y a 10 puntos de la parte superior con respecto al punto actual del flujo de texto, como se muestra en la siguiente imagen:

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="absolute"></a>absolute

Establecer el atributo de estilo de posición en "absoluto" permite colocar el cuadro contenedor a una distancia exacta desde la esquina superior izquierda (el punto base) de su elemento primario (el elemento posicionado que contiene la forma). Tenga en cuenta que el cuadro de contenido que se coloca como absoluto no ocupa espacio en el flujo de texto.

Por ejemplo, en la siguiente representación de VML, el óvalo rojo se encuentra dentro del elemento (toda la página web); por lo tanto, el punto base está en la esquina superior izquierda de la `<body>` página web. El cuadro de contenido del óvalo se coloca exactamente a 20 puntos de la izquierda y a 10 puntos de la parte superior, con respecto a la esquina superior izquierda de la página web, como se muestra en la siguiente imagen:

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="z-index"></a>z-index

Es posible colocar una forma que se superponga a otra forma. Normalmente, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.

En VML, puede controlar el orden z mediante el atributo **de estilo z-index.** El valor de este atributo puede ser cero, un entero positivo o un entero negativo. El gráfico que tiene un valor de índice z mayor se muestra encima del gráfico que tiene un valor de índice z más pequeño. Cuando ambos gráficos tienen el mismo valor de índice Z, el gráfico que aparece en último lugar en el código HTML aparece en la parte superior.

Por ejemplo, en la siguiente representación de VML, el óvalo rojo se muestra encima del rectángulo azul. Esto se debe a que el valor de índice z del óvalo rojo es mayor que el valor de índice z del rectángulo azul.

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Si cambia el índice z, como se muestra en la siguiente representación de VML, el óvalo rojo se movería detrás del rectángulo azul.

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Si proporciona un entero negativo, puede usar el índice z para colocar los gráficos detrás del flujo de texto normal, como se muestra en la siguiente representación de VML.

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="rotation"></a>giro

Puede usar el atributo **de** estilo de rotación para especificar cuántos grados desea que una forma active su eje. Un valor positivo indica una rotación en el sentido de las agujas del reloj; un valor negativo indica una rotación en sentido contrario a las agujas del reloj.

Por ejemplo, si especifica **style**='... rotation:90', puede girar la forma 90 grados en el sentido de las agujas del reloj.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="flip"></a>voltear

Puede usar el atributo **de estilo de** volteo para voltear una forma en su eje x o y según la tabla siguiente:



| Valor | Descripción                                                  |
|-------|--------------------------------------------------------------|
| x     | Voltear la forma girada sobre el eje y (invertir x ordinates) |
| y     | Voltear la forma girada sobre el eje x (invertir las ordinales y) |



 

Se pueden especificar x e y en la propiedad flip.

Por ejemplo, si escribe **style**='... flip:x y', se voltea la forma en sus ejes x e y.

[![volver a la parte ](images/top.gif) superior Volver a la parte superior](#top)

## <a name="summary"></a>Resumen

En función de lo que ha aprendido, puede colocar con precisión una forma en una página web siguiendo estos pasos:

1.  Decida dónde desea que la forma aparezca en una página web y el tamaño de la forma.
2.  Especifique **style**='position:relative (o relative)' para determinar el punto base.
3.  Use **izquierda** y **superior** para especificar el desplazamiento desde el punto base.
4.  Use **width** y **height** para especificar el tamaño del cuadro de contenido de la forma.
5.  Use **z-index para** especificar el orden Z de la forma.

 

 