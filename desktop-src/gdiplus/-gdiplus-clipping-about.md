---
description: El recorte implica restringir el dibujo a una región determinada. En la ilustración siguiente se muestra la cadena &\# 0034; Hola&\# 0034; recortado a una región con forma de corazón.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Recorte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170277"
---
# <a name="clipping-gdi"></a>Recorte (GDI+)

El recorte implica restringir el dibujo a una región determinada. En la ilustración siguiente se muestra la cadena "Hello" recortada en una región con forma de corazón.

![ilustración que muestra partes de la cadena "hello" dentro de un corazón rojo](images/aboutgdip02-art30.png)

Las regiones se pueden construir a partir de rutas de acceso y las rutas de acceso pueden contener los contornos de las cadenas, por lo que puede usar texto con contorno para el recorte. En la ilustración siguiente se muestra un conjunto de elipses concéntricas recortadas al interior de una cadena de texto.

![ilustración en la que se muestra la cadena "hello" rellenada por un patrón de círculos concéntricas](images/aboutgdip02-art31.png)

Para dibujar con recorte, cree un objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) llame a su [método SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) y, a continuación, llame a los métodos de dibujo de ese mismo **objeto Graphics.** En el ejemplo siguiente se dibuja una línea recortada a una región rectangular.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



En la ilustración siguiente se muestra la región rectangular junto con la línea recortada.

![ilustración que muestra un rectángulo con una línea diagonal de arriba abajo](images/aboutgdip02-art31a.png)

 

 



