---
description: Cuando se usa Windows GDI+ para dibujar una línea, se proporciona el punto inicial y el punto final de la línea, pero no es necesaria ninguna información sobre los píxeles individuales de la línea.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Suavizado de contorno con líneas y curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697114"
---
# <a name="antialiasing-with-lines-and-curves"></a>Suavizado de contorno con líneas y curvas

Cuando se usa Windows GDI+ para dibujar una línea, se proporciona el punto inicial y el punto final de la línea, pero no es necesaria ninguna información sobre los píxeles individuales de la línea. GDI+ funciona junto con el software del controlador de pantalla para determinar qué píxeles se van a activados para mostrar la línea en un dispositivo de visualización determinado.

Considere una línea roja recta que va desde el punto (4, 2) hasta el punto (16, 10). Suponga que el sistema de coordenadas tiene su origen en la esquina superior izquierda y que la unidad de medida es el píxel. Supongamos también que el eje X apunta a la derecha y el eje Y apunta hacia abajo. En la ilustración siguiente se muestra una vista ampliada de la línea roja dibujada sobre un fondo con forma de fondo.

![ilustración en la que se muestran píxeles rojos sólidos en un fondo con forma de color rojo](images/aboutgdip02-art33.png)

Tenga en cuenta que los píxeles rojos usados para representar la línea son opacos. No hay píxeles parcialmente transparentes implicados en la visualización de la línea. Este tipo de representación de línea proporciona a la línea un aspecto irregular, y la línea tiene un aspecto un poco parecido a un ala. Esta técnica de representar una línea con una marca de puntuación se denomina alias. el ánimo es un alias para la línea teórica.

Una técnica más sofisticada para representar una línea implica el uso de píxeles parcialmente transparentes junto con píxeles rojos puros. Los píxeles se establecen en rojo puro o en alguna combinación de rojo y el color de fondo en función de lo cerca que estén de la línea. Este tipo de representación se denomina suavizado de contorno y da como resultado una línea que el ojo humano percibe como más suave. En la ilustración siguiente se muestra cómo se combinan ciertos píxeles con el fondo para generar una línea suavizada.

![ilustración que muestra píxeles que son tonalidades de rojo en el mismo fondo](images/aboutgdip02-art34.png)

El suavizado de contorno (suavizado) también se puede aplicar a las curvas. En la ilustración siguiente se muestra una vista ampliada de una elipse suavizada.

![ilustración de una elipse de diferentes tonalidades de píxeles azules en un fondo blanco](images/aboutgdip02-art35.png)

En la ilustración siguiente se muestra la misma elipse en su tamaño real, una vez sin suavizado de contorno y otra con suavizado de contorno.

![captura de pantalla de dos puntos suspensivos: el que tiene suavizado de contorno aparece notablemente más suave](images/aboutgdip02-art36.png)

Para dibujar líneas y curvas que usan suavizado de contorno, cree un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y pase *SmoothingModeAntiAlias* a su [**método Graphics::SetSmoothingMode.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) A continuación, llame a uno de los métodos de dibujo de ese mismo **objeto Graphics.**


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** es un elemento de la [**enumeración SmoothingMode.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)

 

 



