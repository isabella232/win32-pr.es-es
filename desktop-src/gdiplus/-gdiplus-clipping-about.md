---
description: El recorte implica restringir el dibujo a una región determinada. En la ilustración siguiente se muestra la cadena &\# 0034; Hola&\# 0034; se recorta a una región en forma de corazón.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Recorte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082501"
---
# <a name="clipping-gdi"></a>Recorte (GDI+)

El recorte implica restringir el dibujo a una región determinada. En la ilustración siguiente se muestra la cadena "Hello" recortada en una región en forma de corazón.

![Ilustración que muestra partes de la cadena "Hello" dentro de un corazón rojo](images/aboutgdip02-art30.png)

Las regiones se pueden construir a partir de trazados y las rutas de acceso pueden contener los contornos de las cadenas, por lo que puede usar el texto esquematizado para el recorte. En la ilustración siguiente se muestra un conjunto de puntos suspensivos concéntricos recortados en el interior de una cadena de texto.

![Ilustración que muestra la cadena "Hello" rellenada por un patrón de círculos concéntricos](images/aboutgdip02-art31.png)

Para dibujar con recorte, cree un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , llame a su método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) y, a continuación, llame a los métodos de dibujo de ese mismo objeto **Graphics** . En el ejemplo siguiente se dibuja una línea que se recorta a una región rectangular.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



En la ilustración siguiente se muestra la región rectangular junto con la línea recortada.

![Ilustración que muestra un rectángulo con una línea diagonal de arriba abajo](images/aboutgdip02-art31a.png)

 

 



