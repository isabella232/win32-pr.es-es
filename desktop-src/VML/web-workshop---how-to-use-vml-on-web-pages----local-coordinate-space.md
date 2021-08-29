---
title: Uso del espacio de coordenadas local
description: Uso del espacio de coordenadas local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Taller web, espacio de coordenadas local
- diseñar páginas web, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), espacio de coordenadas local
- VML (Lenguaje de marcado de vectores), espacio de coordenadas local
- gráficos vectoriales, espacio de coordenadas local
- espacio de coordenadas local
- Formas de VML, espacio de coordenadas local
- Lenguaje de marcado de vectores (VML), agrupar formas
- VML (Lenguaje de marcado de vectores), agrupar formas
- gráficos vectoriales, agrupación de formas
- Formas de VML, agrupación
- agrupación de formas
- Lenguaje de marcado de vectores (VML), formas de escalado
- VML (Lenguaje de marcado de vectores), formas de escalado
- gráficos vectoriales, formas de escalado
- Formas de VML, escalado
- formas de escalado
- Lenguaje de marcado de vectores (VML), formas de tamaño
- VML (Lenguaje de marcado de vectores), formas de tamaño
- gráficos vectoriales, formas de tamaño
- Formas de VML, tamaño
- formas de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7449890bc28088f9464976ad89a4cce359655bb1f7a6577001856ccd99155a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057089"
---
# <a name="using-local-coordinate-space"></a>Uso del espacio de coordenadas local

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como ha aprendido, puede especificar  los  atributos de estilo de ancho y alto para definir el tamaño de un cuadro de contenido en el que se representará el contenido de una forma o grupo. En este tema, explicaremos qué es el espacio de coordenadas local y cómo se usa en VML para escalar las formas.

Si se le pide que dibuje un rectángulo de una pulgada por dos pulgadas en un papel de cuadrícula, lo primero que averiguaría es dónde empezar (el punto de origen). A continuación, averiguaría cómo asignar una pulgada a las celdas del papel de cuadrícula (la coordenada).

De forma similar, cuando el contenido de una forma o grupo se representa dentro de su cuadro de contenido en una página web, se deben definir el punto de origen y la coordenada. VML proporciona espacio de coordenadas local para permitir que cada forma o grupo defina su propio punto de origen y coordenada. Si no especifica un espacio de coordenadas, se usará el predeterminado. De forma predeterminada, la originación comienza en la esquina superior izquierda del cuadro de contenido.

Por ejemplo, la representación de VML para el óvalo rojo que se muestra a continuación no especifica los atributos de propiedad **coordsize** y **coordorigin.** Por lo tanto, se usa un espacio de coordenadas local predeterminado. El tamaño del óvalo es de 100 puntos (ancho) por 75 puntos (alto). Puede cambiar el tamaño del óvalo especificando un ancho o alto diferentes, como ha aprendido en el tema [Formas de](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) escala.

![oval1.gif (627 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Cuando la forma se vuelva más complicada o cuando quiera agrupar varias formas y escalarlas juntas, debe usar la característica Espacio de coordenadas locales que se proporciona en VML.

Para cada forma o grupo, puede usar los atributos de propiedad **coordsize** y **coordorigin** para definir el espacio de coordenadas local de la forma o del grupo. El **atributo coordsize** especifica el número de unidades a lo largo del ancho y el alto del cuadro de contenido. El **atributo coordorigin** define la coordenada en la esquina superior izquierda del cuadro de contenido. Toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local.

Por ejemplo, como se muestra en la siguiente representación de VML, define el tamaño del cuadro de contenido para que la forma sea `width: 100pt; height: 100pt;` de 100 puntos por 100 puntos.

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` define el tamaño del espacio de coordenadas local para que la forma sea de 21600 unidades por 21600 unidades. Por lo tanto, una unidad del espacio de coordenadas local equivale a 1/216 punto.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` define el contorno de la forma como forma de rombo. Como hemos aprendido, toda la información relacionada con la posición (como el ancho, el alto, la izquierda, la parte superior, la ruta de acceso, etc.) se expresa en términos de la unidad en el espacio de coordenadas local. Por lo tanto, 10800 en `<path>` significa 10800 unidades, lo que equivale a 50 puntos.

Si desea cambiar el tamaño de esta forma de rombo, basta con especificar un ancho o alto distintos, eso es todo. no tiene que cambiar ningún valor en `<path>` . Para esta forma complicada, si no usa la característica Espacio de coordenadas locales, tendría que cambiar cada valor de cada vez que quisiera cambiar `<path>` su tamaño.

Por ejemplo, puede escalar la forma de rombo simplemente especificando un ancho o alto diferentes, como se muestra en la siguiente representación de VML:

![cord2.gif (1692 bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





También puede usar espacio de coordenadas locales en el elemento para que el contenido de todas las formas del grupo se escale de forma conjunta según `<group>` la misma coordenada. A continuación, siempre que quiera escalar o mover un grupo de formas, simplemente cambie el ancho y alto, o la configuración de **coordsize** y **coordorigin,** del grupo.

Por ejemplo, en la siguiente representación de VML, define el tamaño del cuadro de contenido para que el grupo sea `<v:group style='... width:200pt;height:200pt;'>` de 200 puntos por 200 puntos.

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` define el tamaño del espacio de coordenadas local para el grupo en 1000 unidades por 1000 unidades. Por lo tanto, 1 unidad en el espacio de coordenadas local equivale a 1/5 punto.
-   `coordorigin="-500,-500"` define la esquina superior izquierda del cuadro de contenido como "-500, -500". Por lo tanto, el sistema de coordenadas dentro del cuadro que lo contiene oscila entre -500 y 500 a lo largo del eje X y -500 a 500 a lo largo del eje Y. En otras palabras, el centro del cuadro de contenido es "0, 0".
-   `<v:oval style='... width:400;height:300;'>` define el tamaño del cuadro de contenido para que el óvalo rojo sea de 400 unidades (ancho) por 300 unidades (alto). Dado que una unidad del espacio de coordenadas local equivale a 1/5 punto, el tamaño del cuadro de contenido del óvalo rojo es de 80 puntos (ancho) por 60 puntos (alto).

De forma similar, el tamaño del cuadro de contención para el redondeo verde es de 50 puntos (ancho) por 40 puntos (alto).

Si desea cambiar el tamaño del óvalo rojo y el de color verde, simplemente cambie `<v:group style='... width:200pt;height:200pt;'>` . Eso es todo: no tiene que cambiar individualmente el tamaño de las dos formas.

Por ejemplo, si cambia a `<v:group style='... width:200pt;height:200pt;'>` , las formas se vuelven más `<v:group style='... width:300pt;height:300pt;'>` grandes, como se muestra en la siguiente imagen:

![cord4.gif (943 bytes)](images/cord4.gif)



También observaría que las formas se encuentran de forma diferente. Esto se debe a que las formas se dibujan a partir de "0, 0", que se encuentra en el centro del cuadro de contenido. Dado que hace que el cuadro de contenido sea más grande, también se mueve el centro del cuadro de contenido.

Si cambia a , como se muestra en la siguiente imagen, observará que tanto el óvalo rojo como el roundrect verde se desplazan hacia arriba hasta `coordorigin="-500,-500"` `coordorigin="0,0"` la nueva ubicación. Esto se debe a que "0, 0" ahora se encuentra en la esquina superior izquierda del cuadro de contenido.

![cord5.gif (648 bytes)](images/cord5.gif)



También es importante tener en cuenta que el cuadro de contenido no establece una región de recorte. Los gráficos se pueden dibujar fuera de los límites del cuadro de contenido. El cuadro de contenido simplemente sirve para asignar el espacio de coordenadas local al espacio de página.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 