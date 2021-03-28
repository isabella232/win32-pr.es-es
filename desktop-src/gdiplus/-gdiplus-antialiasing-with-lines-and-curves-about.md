---
description: Cuando se usa Windows GDI+ para dibujar una línea, se proporciona el punto inicial y el punto final de la línea, pero no es necesario proporcionar información sobre los píxeles individuales de la línea.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Suavizado de contorno con líneas y curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812980"
---
# <a name="antialiasing-with-lines-and-curves"></a>Suavizado de contorno con líneas y curvas

Cuando se usa Windows GDI+ para dibujar una línea, se proporciona el punto inicial y el punto final de la línea, pero no es necesario proporcionar información sobre los píxeles individuales de la línea. GDI+ funciona junto con el software del controlador de pantalla para determinar qué píxeles se activarán para mostrar la línea en un dispositivo de pantalla determinado.

Considere una línea roja recta que va desde el punto (4, 2) hasta el punto (16, 10). Suponga que el sistema de coordenadas tiene su origen en la esquina superior izquierda y que la unidad de medida es el píxel. Supongamos también que el eje x apunta hacia la derecha y el eje y apunta hacia abajo. En la ilustración siguiente se muestra una vista ampliada de la línea roja dibujada en un fondo multicolor.

![Ilustración que muestra píxeles rojos sólidos en un fondo multicolor](images/aboutgdip02-art33.png)

Tenga en cuenta que los píxeles rojos utilizados para representar la línea son opacos. No hay píxeles parcialmente transparentes implicados en la visualización de la línea. Este tipo de representación de línea proporciona a la línea una apariencia escalonada y la línea es un poco similar a una escalera. Esta técnica de representar una línea con una escalera se denomina aliasing; la escalera es un alias de la línea teórica.

Una técnica más sofisticada para representar una línea implica el uso de píxeles parcialmente transparentes junto con píxeles rojos puros. Los píxeles se establecen en rojo puro o en alguna mezcla de rojo y el color de fondo en función de la proximidad de la línea. Este tipo de representación se denomina suavizado de contorno y da como resultado una línea que el ojo humano percibe como más suave. En la ilustración siguiente se muestra cómo determinados píxeles se combinan con el fondo para producir una línea alisada.

![Ilustración en la que se muestran los píxeles que son sombras de color rojo en el mismo fondo](images/aboutgdip02-art34.png)

El suavizado de contorno (Smoothing) también se puede aplicar a curvas. En la ilustración siguiente se muestra una vista ampliada de una elipse suavizada.

![Ilustración de una elipse formada por diferentes sombras de píxeles azules en un fondo blanco](images/aboutgdip02-art35.png)

En la ilustración siguiente se muestra la misma elipse en su tamaño real, una vez sin suavizado de contorno y una vez con suavizado de contorno.

![captura de pantalla de dos elipses: la que tiene el suavizado de contorno parece más suave](images/aboutgdip02-art36.png)

Para dibujar líneas y curvas que utilicen el suavizado de contorno, cree un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y pase *SmoothingModeAntiAlias* a su método [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) . A continuación, llame a uno de los métodos de dibujo de ese mismo objeto de **gráficos** .


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** es un elemento de la enumeración [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .

 

 



