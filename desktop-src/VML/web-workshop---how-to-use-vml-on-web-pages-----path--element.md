---
title: Usar el elemento path
description: Usar el elemento path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento path
- diseñar páginas web, elemento path
- Lenguaje de marcado de vectores (VML), elemento path
- VML (Lenguaje de marcado de vectores), elemento path
- gráficos vectoriales, elemento path
- elemento path
- Elementos VML, ruta de acceso
- Formas VML, elemento path
- Lenguaje de marcado de vectores (VML), personalizar contornos de formas
- VML (Lenguaje de marcado de vectores), personalizar contornos de formas
- gráficos vectoriales, personalizar contornos de formas
- Formas VML, personalizar esquemas
- personalizar contornos de formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793462"
---
# <a name="using-the-path-element"></a>Usar el elemento path

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Ha aprendido que puede usar los elementos de forma predefinidos de VML, como `<oval>` ,, `<line>` , `<polyline>` , `<curve>` `<rect>` , `<roundrect>` y `<arc>` --para dibujar una forma. En este tema, se muestra cómo usar el `<path>` subelemento para personalizar el contorno de una forma.

Puede colocar el `<path>` subelemento dentro del `<shape>` `<shapetype>` elemento o. Después, puede usar los atributos de propiedad del `<path>` subelemento para personalizar el contorno de la forma.

Por ejemplo, para dibujar la forma personalizada que se muestra en la siguiente imagen, puede usar el `<path>` subelemento para definir el contorno de la forma, como se muestra en la siguiente representación de VML:

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





-   Los valores `m 8,65` indican que el dibujo comienza en el punto (8, 65).
-   Los valores `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indican que una línea recta comienza en el punto actual (8, 65) y termina en el punto especificado (72, 65), que se convierte en el nuevo punto actual. Una nueva línea comienza en el punto actual (72, 65) y termina en el punto dado, que se convierte en el nuevo punto actual, y así sucesivamente, al punto final (60, 100).
-   `x` indica que la ruta de acceso se cerrará con una línea recta que comienza en el punto actual (60, 100) y termina en el punto original (8, 65).
-   `e` indica detener dibujo.

Para obtener más información sobre este elemento, vea la [especificación de VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 