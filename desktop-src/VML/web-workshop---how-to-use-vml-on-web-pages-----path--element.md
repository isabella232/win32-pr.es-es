---
title: Usar el elemento Path
description: Usar el elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Taller web, elemento path
- diseñar páginas web, elemento path
- Lenguaje de marcado de vectores (VML),elemento path
- VML (Lenguaje de marcado de vectores),elemento path
- vector graphics,path element
- elemento path
- Elementos de VML, ruta de acceso
- Formas de VML, elemento path
- Lenguaje de marcado de vectores (VML), personalizar contornos de forma
- VML (Lenguaje de marcado de vectores), personalizar contornos de forma
- gráficos vectoriales, personalización de contornos de forma
- Formas de VML, personalización de contornos
- personalizar contornos de formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cbb27dbc2b039478903f697b02cefb14464b71a96ab2165db124d0a0053a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057193"
---
# <a name="using-the-path-element"></a>Usar el elemento Path

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ha aprendido que puede usar los elementos de forma predefinidos de VML , como `<oval>` , , , , , y , para dibujar una `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. En este tema, se ilustrará cómo usar el `<path>` sub elemento para personalizar el contorno de una forma.

Puede colocar el `<path>` sub elemento dentro del elemento o `<shape>` `<shapetype>` . A continuación, puede usar los atributos de propiedad del `<path>` sub elemento para personalizar el contorno de la forma.

Por ejemplo, para dibujar la forma personalizada que se muestra en la siguiente imagen, puede usar el sub element para definir el contorno de la forma, como se muestra en la siguiente representación `<path>` de VML:

![shape1.gif (1301 bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   Los valores `m 8,65` indican que el dibujo comienza en el punto (8,65).
-   Los valores indican que una línea recta comienza en el punto actual (8, 65) y termina en el punto dado `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` (72, 65), que se convierte en el nuevo punto actual. Una nueva línea comienza en el punto actual (72, 65) y termina en el punto dado, que se convierte en el nuevo punto actual, y así sucesivamente, hasta el punto final (60, 100).
-   `x` indica que la ruta de acceso se cerrará mediante una línea recta que comienza en el punto actual (60, 100) y termina en el punto original (8, 65).
-   `e` indica que se detiene el dibujo.

Para obtener más información sobre este elemento, consulte la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 