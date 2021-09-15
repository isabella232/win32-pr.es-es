---
description: 'La clase FontFamily proporciona los métodos siguientes que recuperan varias métricas para una combinación de familia o estilo determinada:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Obtención de métricas de fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567629"
---
# <a name="obtaining-font-metrics"></a>Obtención de métricas de fuente

La [**clase FontFamily proporciona**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) los métodos siguientes que recuperan varias métricas para una combinación de familia y estilo determinada:

-   [**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

Los números devueltos por estos métodos están en unidades de diseño de fuentes, por lo que son independientes del tamaño y las unidades de un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) determinado.

En la ilustración siguiente se muestra el acentamiento, el descenso y el espaciado de línea.

![diagrama de dos caracteres en líneas adyacentes, que muestra el acentamiento de celdas, el descenso de celdas y el espaciado de línea](images/fontstext7a.png)

En el ejemplo siguiente se muestran las métricas del estilo normal de la familia de fuentes de Arial. El código también crea un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basado en la familia Arial) con un tamaño de 16 píxeles y muestra las métricas (en píxeles) de ese objeto **Font** determinado.


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

![captura de pantalla de una ventana con texto que indica el tamaño y el alto de la fuente, así como el aumento, el descenso y el espaciado de línea](images/fontstext8.png)

Observe las dos primeras líneas de salida de la ilustración anterior. El [**objeto Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve un tamaño de 16 y el objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) devuelve una altura em de 2048. Estos dos números (16 y 2048) son la clave para convertir entre las unidades de diseño de fuente y las unidades (en este caso, píxeles) del objeto **Font.**

Por ejemplo, puede convertir la subida de unidades de diseño a píxeles como se muestra a continuación:

![ecuación que multiplica 1854 unidades de diseño por 16 píxeles divididas por unidades de diseño de 2048, igual a 14,484375 píxeles](images/fontstext9.png)

El código anterior coloca el texto verticalmente estableciendo el miembro de datos *y* de un [**objeto PointF.**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) La coordenada y aumenta en para `font.GetHeight(0.0f)` cada nueva línea de texto. El [**método Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) de un [**objeto Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve el espaciado de línea (en píxeles) para ese objeto **Font** determinado. En este ejemplo, el número devuelto por **Font::GetHeight** es 18.398438. Tenga en cuenta que esto es igual que el número obtenido al convertir la métrica de espaciado de línea en píxeles.

 

 
