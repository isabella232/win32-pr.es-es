---
description: 'La clase FontFamily proporciona los métodos siguientes que recuperan varias métricas para una combinación determinada de familia y estilo:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Obtener métricas de fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082103"
---
# <a name="obtaining-font-metrics"></a>Obtener métricas de fuente

La clase [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) proporciona los métodos siguientes que recuperan varias métricas para una combinación determinada de familia y estilo:

-   [**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

Los números devueltos por estos métodos están en unidades de diseño de fuente, por lo que son independientes del tamaño y las unidades de un objeto de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) determinado.

En la ilustración siguiente se muestra el ascenso, el descenso y el interlineado.

![diagrama de dos caracteres en líneas adyacentes, mostrando el ascenso de celda, el descenso de celda y el espaciado de líneas](images/fontstext7a.png)

En el ejemplo siguiente se muestran las métricas para el estilo normal de la familia de fuentes Arial. El código también crea un objeto de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basado en la familia Arial) con un tamaño de 16 píxeles y muestra las métricas (en píxeles) de ese objeto de **fuente** concreto.


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



En la ilustración siguiente se muestra la salida del código anterior.

![captura de pantalla de una ventana con texto que indica el tamaño y el alto de la fuente, y el ascenso, el descenso y el espaciado de líneas](images/fontstext8.png)

Tenga en cuenta las dos primeras líneas de la salida de la ilustración anterior. El objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve un tamaño de 16 y el objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) devuelve un alto em de 2.048. Estos dos números (16 y 2.048) son la clave para la conversión entre las unidades de diseño de fuente y las unidades (en este caso píxeles) del objeto de **fuente** .

Por ejemplo, puede convertir el ascenso de las unidades de diseño a píxeles de la siguiente manera:

![ecuación que multiplica las unidades de diseño 1854 por 16 píxeles divididos entre las 2048 unidades de diseño, igual a 14,484375 píxeles](images/fontstext9.png)

El código anterior coloca el texto verticalmente estableciendo el miembro de datos *y* de un objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) . La coordenada y aumenta en `font.GetHeight(0.0f)` cada línea de texto nueva. El método [**Font:: getHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) de un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve el interlineado (en píxeles) de ese objeto **Font** determinado. En este ejemplo, el número devuelto por **Font:: getHeight** es 18,398438. Tenga en cuenta que esto es lo mismo que el número obtenido convirtiendo la métrica de espaciado de línea en píxeles.

 

 
