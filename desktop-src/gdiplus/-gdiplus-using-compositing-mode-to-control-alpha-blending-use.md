---
description: 'Puede haber ocasiones en las que desee crear un mapa de bits sin pantalla que tenga las siguientes características:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Usar el modo de composición para controlar la mezcla alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985115"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Usar el modo de composición para controlar la mezcla alfa

Puede haber ocasiones en las que desee crear un mapa de bits sin pantalla que tenga las siguientes características:

-   Los colores tienen valores alfa inferiores a 255.
-   Los colores no se combinan alfa entre sí a medida que se crea el mapa de bits.
-   Cuando se muestra el mapa de bits terminado, los colores del mapa de bits son alfa combinados con los colores de fondo en el dispositivo de pantalla.

Para crear este tipo de mapa de bits, construya un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) en blanco y, a continuación, construya un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en dicho mapa de bits. Establezca el modo de composición del objeto de **gráficos** en CompositingModeSourceCopy.

En el ejemplo siguiente se crea un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . El código usa el objeto **Graphics** junto con dos pinceles semitransparentes (alfa = 160) para pintar en el mapa de bits. El código rellena una elipse roja y una elipse verde usando los pinceles semitransparentes. La elipse verde se superpone a la elipse roja, pero el color verde no se combina con el rojo porque el modo de composición del objeto **Graphics** se establece en CompositingModeSourceCopy.

A continuación, el código se prepara para dibujar en la pantalla llamando a [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) y creando un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un contexto de dispositivo. El código dibuja el mapa de bits en la pantalla dos veces: una vez en un fondo blanco y una vez en un fondo multicolor. Los píxeles del mapa de bits que forman parte de las dos elipses tienen un componente alfa de 160, por lo que las elipses se combinan con los colores de fondo de la pantalla.


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



En la ilustración siguiente se muestra la salida del código anterior. Tenga en cuenta que las elipses se mezclan con el fondo, pero no se combinan entre sí.

![Ilustración en la que se muestran dos elipses de colores diferentes, cada una de las cuales se combina con su fondo multicolor](images/sourcecopy.png)

El ejemplo de código anterior tiene la siguiente instrucción:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Si desea que los puntos suspensivos se mezclen entre sí y con el fondo, cambie la instrucción a lo siguiente:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



En la ilustración siguiente se muestra la salida del Código revisado.

![usar el modo de composición para controlar la ilustración de la combinación alfa](images/sourceover.png)

 

 



