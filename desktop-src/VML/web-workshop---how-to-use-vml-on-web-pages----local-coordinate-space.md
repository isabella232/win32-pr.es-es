---
title: Usar el espacio de coordenadas local
description: Usar el espacio de coordenadas local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, espacio de coordenadas local
- diseñar páginas web, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores), espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
- Formas VML, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupar formas
- gráficos vectoriales, agrupar formas
- Formas VML, agrupación
- agrupar formas
- Lenguaje de marcado de vectores (VML), ajustar el tamaño de las formas
- VML (Lenguaje de marcado de vectores), ajustar el tamaño de las formas
- gráficos vectoriales, ajustar el tamaño de las formas
- Formas VML, escalado
- ajustar el tamaño de las formas
- Lenguaje de marcado de vectores (VML), ajustar el tamaño de las formas
- VML (Lenguaje de marcado de vectores), ajustar el tamaño de las formas
- gráficos vectoriales, ajustar el tamaño de las formas
- Formas VML, ajustar tamaño
- cambiar el tamaño de las formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793450"
---
# <a name="using-local-coordinate-space"></a>Usar el espacio de coordenadas local

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede especificar los atributos de estilo **ancho** y **alto** para definir el tamaño de un cuadro contenedor en el que se representará el contenido de una forma o un grupo. En este tema, explicaremos qué espacio de coordenadas local es y cómo se usa en VML para escalar formas.

Si se le pidió que dibujara un rectángulo de una pulgada por dos pulgadas en una parte del papel de la cuadrícula, lo primero que desfigurarías es dónde empezar (el punto de origen). A continuación, debería averiguar cómo asignar una pulgada a las celdas del papel de la cuadrícula (la coordenada).

Del mismo modo, cuando el contenido de una forma o un grupo se representan dentro de su cuadro contenedor en una página web, se deben definir el punto de origen y la coordenada. VML proporciona el espacio de coordenadas local para permitir que cada forma o grupo defina su propio punto de origen y coordenada. Si no especifica un espacio de coordenadas, se usará el predeterminado. De forma predeterminada, el origen comienza en la esquina superior izquierda del cuadro contenedor.

Por ejemplo, la representación VML del óvalo rojo que se muestra a continuación no especifica los atributos de la propiedad **coordsize** y **coordorigin** . Por lo tanto, se utiliza un espacio de coordenadas local predeterminado. El tamaño del óvalo es 100 puntos (ancho) por 75 puntos (alto). Puede cambiar el tamaño del óvalo especificando otro ancho o alto, como ha aprendido en el tema formas de [escala](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .

![oval1.gif (627 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Cuando la forma se vuelve más complicada, o cuando desea agrupar varias formas y escalarlas juntas, debe usar la característica de espacio de coordenadas local que se proporciona en VML.

Para cada forma o grupo, puede usar los atributos de la propiedad **coordsize** y **coordorigin** para definir el espacio de coordenadas local del grupo o de la forma. El atributo **coordsize** especifica el número de unidades a lo largo del ancho y el alto del cuadro contenedor. El atributo **coordorigin** define la coordenada en la esquina superior izquierda del cuadro contenedor. Toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local.

Por ejemplo, como se muestra en la representación VML siguiente, `width: 100pt; height: 100pt;` define el tamaño del cuadro contenedor para que la forma sea 100 puntos por 100 puntos.

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` define el tamaño del espacio de coordenadas local para que la forma sea 21600 unidades por 21600 unidades. Por lo tanto, una unidad en el espacio de coordenadas local es equivalente a 1/216 punto.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` define el contorno de la forma como una forma de rombo. Como hemos aprendido, toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local. Por lo tanto, 10800 en el `<path>` significa 10800 unidades, que es equivalente a 50 puntos.

Si desea cambiar el tamaño de esta forma de rombo, solo tiene que especificar un ancho o un alto distintos; es decir, no tiene que cambiar ningún valor de `<path>` . Para esta forma complicada, si no usó la característica de espacio de coordenadas local, tendría que cambiar todos los valores de cada vez que deseara cambiar su `<path>` tamaño.

Por ejemplo, puede escalar la forma de rombo simplemente especificando un ancho o un alto distintos, tal como se muestra en la siguiente representación de VML:

![cord2.gif (1692 bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





También puede usar el espacio de coordenadas local en el `<group>` elemento para que el contenido de todas las formas dentro del grupo se escale juntos según la misma coordenada. Después, siempre que quiera escalar o trasladar un grupo de formas, solo tiene que cambiar el ancho y el alto, o la configuración **coordsize** y **coordorigin** del grupo.

Por ejemplo, en la representación VML siguiente, `<v:group style='... width:200pt;height:200pt;'>` define el tamaño del cuadro contenedor para que el grupo sea 200 puntos por 200 puntos.

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` define el tamaño del espacio de coordenadas local para que el grupo sea 1000 unidades por 1000 unidades. Por lo tanto, 1 unidad en el espacio de coordenadas local es equivalente a 1/5 punto.
-   `coordorigin="-500,-500"` define la esquina superior izquierda del cuadro contenedor para que sea "-500,-500". Por lo tanto, el sistema de coordenadas dentro del cuadro que contiene va de-500 a 500 a lo largo del eje x y de-500 a 500 a lo largo del eje y. En otras palabras, el centro del cuadro contenedor es "0,0".
-   `<v:oval style='... width:400;height:300;'>` define el tamaño del cuadro contenedor para que el óvalo rojo sea 400 unidades (ancho) de 300 unidades (alto). Dado que una unidad en el espacio de coordenadas local es equivalente a 1/5 punto, el tamaño del cuadro contenedor para el óvalo rojo es de 80 puntos (ancho) de 60 puntos (alto).

Del mismo modo, el tamaño del cuadro contenedor para el roundrect verde es 50 puntos (ancho) por 40 puntos (alto).

Cuando desee cambiar el tamaño del óvalo rojo y del roundrect verde, simplemente cambie `<v:group style='... width:200pt;height:200pt;'>` . Es decir, no tiene que cambiar el tamaño de las dos formas de forma individual.

Por ejemplo, si cambia `<v:group style='... width:200pt;height:200pt;'>` a `<v:group style='... width:300pt;height:300pt;'>` , las formas serán mayores, tal como se muestra en la siguiente imagen:

![cord4.gif (943 bytes)](images/cord4.gif)



También observará que las formas se encuentran de forma diferente. Esto se debe a que las formas se dibujan desde "0,0", que se encuentra en el centro del cuadro contenedor. Como aumenta el tamaño del cuadro contenedor, también se mueve el centro del cuadro contenedor.

Si cambia `coordorigin="-500,-500"` a `coordorigin="0,0"` , como se muestra en la siguiente imagen, observará que el óvalo rojo y el roundrect verde se desplazan hacia arriba en la nueva ubicación. Esto se debe a que "0,0" ahora busca en la esquina superior izquierda del cuadro contenedor.

![cord5.gif (648 bytes)](images/cord5.gif)



También es importante tener en cuenta que el cuadro contenedor no establece una región de recorte. Los gráficos se pueden dibujar fuera de los límites del cuadro contenedor. El cuadro contenedor solo sirve para asignar el espacio de coordenadas local al espacio de la página.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 