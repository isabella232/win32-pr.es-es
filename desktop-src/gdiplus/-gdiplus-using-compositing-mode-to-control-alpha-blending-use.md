---
description: 'Puede haber ocasiones en las que quiera crear un mapa de bits fuera de la pantalla que tenga las siguientes características:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Usar el modo de composición para controlar la mezcla alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea2fc9d5be10e3a73bacf7f5a6dc5cbecb8c2992ac8cd961701f55fc2cb524d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611995"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Usar el modo de composición para controlar la mezcla alfa

Puede haber ocasiones en las que quiera crear un mapa de bits fuera de la pantalla que tenga las siguientes características:

-   Los colores tienen valores alfa inferiores a 255.
-   Los colores no se mezclan alfa entre sí al crear el mapa de bits.
-   Cuando se muestra el mapa de bits finalizado, los colores del mapa de bits se mezclan alfa con los colores de fondo en el dispositivo de visualización.

Para crear este tipo de mapa de bits, construya un objeto [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) en blanco y, a continuación, construya un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en ese mapa de bits. Establezca el modo de composición del objeto **Graphics** en CompositingModeSourceCopy.

En el ejemplo siguiente se crea un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un [**objeto Bitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) El código usa el **objeto Graphics** junto con dos pinceles semitransparentes (alfa = 160) para pintar en el mapa de bits. El código rellena una elipse roja y una elipse verde mediante los pinceles semitransparentes. La elipse verde se superpone a la elipse roja, pero el verde no se mezcla con el rojo porque el modo de composición del objeto **Graphics** está establecido en CompositingModeSourceCopy.

A continuación, el código se prepara para dibujar en la pantalla mediante una llamada a [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) y la creación de un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un contexto de dispositivo. El código dibuja el mapa de bits en la pantalla dos veces: una vez sobre un fondo blanco y otra en un fondo de color azulado. Los píxeles del mapa de bits que forman parte de los dos puntos suspensivos tienen un componente alfa de 160, por lo que los puntos suspensivos se mezclan con los colores de fondo de la pantalla.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



En la ilustración siguiente se muestra la salida del código anterior. Tenga en cuenta que los puntos suspensivos se mezclan con el fondo, pero no se mezclan entre sí.

![ilustración en la que se muestran dos puntos suspensivos de color diferente, cada uno de los cuales se combina con su fondo de color azulado.](images/sourcecopy.png)

El ejemplo de código anterior tiene la siguiente instrucción:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Si desea que los puntos suspensivos se combinen entre sí, así como con el fondo, cambie esa instrucción a lo siguiente:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



En la ilustración siguiente se muestra la salida del código revisado.

![usar el modo de composición para controlar la ilustración de mezcla alfa](images/sourceover.png)

 

 



