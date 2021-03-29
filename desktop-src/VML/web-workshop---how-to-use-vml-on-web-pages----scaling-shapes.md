---
title: Ajustar el tamaño de las formas
description: Ajustar el tamaño de las formas
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, escalar formas
- diseñar páginas web, ajustar el tamaño de las formas
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792105"
---
# <a name="scaling-shapes"></a>Ajustar el tamaño de las formas

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Ha aprendido cómo dibujar y colorear formas en una página web mediante VML. En este tema, se muestra cómo escalar formas a cualquier tamaño que desee.

VML usa la misma sintaxis definida en la sección de [detalles del modelo de representación visual](https://www.w3.org/TR/PR-CSS2/visudet.mdl) de la [especificación CSS2](https://www.w3.org/TR/PR-CSS2/) para especificar el tamaño del cuadro contenedor de forma que el contenido de una forma se represente (dibuje) dentro del cuadro contenedor. Puede usar los atributos de estilo **ancho** y **alto** para definir el tamaño del cuadro contenedor.

Por ejemplo, si dibuja un óvalo y especifica **Style**= ' width: 75pt; height: 100pt ', el óvalo se dibujará dentro de un cuadro contenedor con un tamaño de 75 puntos (ancho) de 100 puntos (alto), tal como se muestra en la siguiente imagen:

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Si cambia el tamaño a **Style**= ' width: 120pt; height: 140pt ', la elipse se vuelve más grande porque se escala en el nuevo cuadro contenedor con un tamaño de 120 puntos (ancho) de 140 puntos (alto), como se muestra en la siguiente imagen:

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Si cambia el tamaño a **Style**= ' width: 60pt; height: 40pt ', la elipse se vuelve más pequeña porque se escala en el nuevo cuadro contenedor con un tamaño de 60 puntos (ancho) de 40 puntos (alto), tal como se muestra en la siguiente imagen:

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 