---
title: Escalado de formas
description: Escalado de formas
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Taller web, escalado de formas
- diseñar páginas web, escalar formas
- Lenguaje de marcado de vectores (VML),escalado de formas
- VML (Lenguaje de marcado de vectores), escalado de formas
- gráficos vectoriales, formas de escalado
- Formas de VML, escalado
- escalado de formas
- Lenguaje de marcado de vectores (VML), formas de tamaño
- VML (Lenguaje de marcado de vectores), formas de tamaño
- gráficos vectoriales, formas de tamaño
- Formas de VML, tamaño
- formas de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc7f62d802548ef1bc19aabf33c886c5b826098ae1280a9dd0b69413c9a61aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057029"
---
# <a name="scaling-shapes"></a>Escalado de formas

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ha aprendido a dibujar y colorear formas en una página web mediante VML. En este tema, se muestra cómo escalar las formas a cualquier tamaño que desee.

VML usa la misma sintaxis definida en la sección Detalles del modelo de [representación visual](https://www.w3.org/TR/PR-CSS2/visudet.mdl) de la especificación [CSS2](https://www.w3.org/TR/PR-CSS2/) para especificar el tamaño del cuadro de contenido para que el contenido de una forma se represente (se represente) dentro del cuadro de contenido. Puede usar los atributos **de estilo de** ancho **y** alto para definir el tamaño del cuadro de contenido.

Por ejemplo, si dibuja un óvalo y especifica **style**='width:75pt;height:100pt', el óvalo se dibujará dentro de un cuadro de contenido con un tamaño de 75 puntos (ancho) por 100 puntos (alto), como se muestra en la siguiente imagen:

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Si cambia el tamaño a **style**='width:120pt;height:140pt', el óvalo se vuelve mayor porque se escala dentro del nuevo cuadro de contenido con un tamaño de 120 puntos (ancho) por 140 puntos (alto), como se muestra en la siguiente imagen:

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Si cambia el tamaño a **style**='width:60pt;height:40pt', el óvalo se vuelve más pequeño porque se escala dentro del nuevo cuadro de contenido con un tamaño de 60 puntos (ancho) en 40 puntos (alto), como se muestra en la siguiente imagen:

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 