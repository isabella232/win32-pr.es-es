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
# <a name="obtaining-font-metrics"></a><span data-ttu-id="5ab85-103">Obtener métricas de fuente</span><span class="sxs-lookup"><span data-stu-id="5ab85-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="5ab85-104">La clase [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) proporciona los métodos siguientes que recuperan varias métricas para una combinación determinada de familia y estilo:</span><span class="sxs-lookup"><span data-stu-id="5ab85-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="5ab85-105">[**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5ab85-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="5ab85-106">[**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5ab85-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="5ab85-107">[**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5ab85-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="5ab85-108">[**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5ab85-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="5ab85-109">Los números devueltos por estos métodos están en unidades de diseño de fuente, por lo que son independientes del tamaño y las unidades de un objeto de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) determinado.</span><span class="sxs-lookup"><span data-stu-id="5ab85-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="5ab85-110">En la ilustración siguiente se muestra el ascenso, el descenso y el interlineado.</span><span class="sxs-lookup"><span data-stu-id="5ab85-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![diagrama de dos caracteres en líneas adyacentes, mostrando el ascenso de celda, el descenso de celda y el espaciado de líneas](images/fontstext7a.png)

<span data-ttu-id="5ab85-112">En el ejemplo siguiente se muestran las métricas para el estilo normal de la familia de fuentes Arial.</span><span class="sxs-lookup"><span data-stu-id="5ab85-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="5ab85-113">El código también crea un objeto de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basado en la familia Arial) con un tamaño de 16 píxeles y muestra las métricas (en píxeles) de ese objeto de **fuente** concreto.</span><span class="sxs-lookup"><span data-stu-id="5ab85-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


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



<span data-ttu-id="5ab85-114">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="5ab85-114">The following illustration shows the output of the preceding code.</span></span>

![captura de pantalla de una ventana con texto que indica el tamaño y el alto de la fuente, y el ascenso, el descenso y el espaciado de líneas](images/fontstext8.png)

<span data-ttu-id="5ab85-116">Tenga en cuenta las dos primeras líneas de la salida de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="5ab85-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="5ab85-117">El objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve un tamaño de 16 y el objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) devuelve un alto em de 2.048.</span><span class="sxs-lookup"><span data-stu-id="5ab85-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="5ab85-118">Estos dos números (16 y 2.048) son la clave para la conversión entre las unidades de diseño de fuente y las unidades (en este caso píxeles) del objeto de **fuente** .</span><span class="sxs-lookup"><span data-stu-id="5ab85-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="5ab85-119">Por ejemplo, puede convertir el ascenso de las unidades de diseño a píxeles de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5ab85-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![ecuación que multiplica las unidades de diseño 1854 por 16 píxeles divididos entre las 2048 unidades de diseño, igual a 14,484375 píxeles](images/fontstext9.png)

<span data-ttu-id="5ab85-121">El código anterior coloca el texto verticalmente estableciendo el miembro de datos *y* de un objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) .</span><span class="sxs-lookup"><span data-stu-id="5ab85-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="5ab85-122">La coordenada y aumenta en `font.GetHeight(0.0f)` cada línea de texto nueva.</span><span class="sxs-lookup"><span data-stu-id="5ab85-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="5ab85-123">El método [**Font:: getHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) de un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) devuelve el interlineado (en píxeles) de ese objeto **Font** determinado.</span><span class="sxs-lookup"><span data-stu-id="5ab85-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="5ab85-124">En este ejemplo, el número devuelto por **Font:: getHeight** es 18,398438.</span><span class="sxs-lookup"><span data-stu-id="5ab85-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="5ab85-125">Tenga en cuenta que esto es lo mismo que el número obtenido convirtiendo la métrica de espaciado de línea en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5ab85-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
