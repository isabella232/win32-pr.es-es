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
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="8e9ad-103">Usar el modo de composición para controlar la mezcla alfa</span><span class="sxs-lookup"><span data-stu-id="8e9ad-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="8e9ad-104">Puede haber ocasiones en las que desee crear un mapa de bits sin pantalla que tenga las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="8e9ad-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="8e9ad-105">Los colores tienen valores alfa inferiores a 255.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="8e9ad-106">Los colores no se combinan alfa entre sí a medida que se crea el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="8e9ad-107">Cuando se muestra el mapa de bits terminado, los colores del mapa de bits son alfa combinados con los colores de fondo en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="8e9ad-108">Para crear este tipo de mapa de bits, construya un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) en blanco y, a continuación, construya un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en dicho mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="8e9ad-109">Establezca el modo de composición del objeto de **gráficos** en CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="8e9ad-110">En el ejemplo siguiente se crea un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="8e9ad-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="8e9ad-111">El código usa el objeto **Graphics** junto con dos pinceles semitransparentes (alfa = 160) para pintar en el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="8e9ad-112">El código rellena una elipse roja y una elipse verde usando los pinceles semitransparentes.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="8e9ad-113">La elipse verde se superpone a la elipse roja, pero el color verde no se combina con el rojo porque el modo de composición del objeto **Graphics** se establece en CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="8e9ad-114">A continuación, el código se prepara para dibujar en la pantalla llamando a [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) y creando un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="8e9ad-115">El código dibuja el mapa de bits en la pantalla dos veces: una vez en un fondo blanco y una vez en un fondo multicolor.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="8e9ad-116">Los píxeles del mapa de bits que forman parte de las dos elipses tienen un componente alfa de 160, por lo que las elipses se combinan con los colores de fondo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


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



<span data-ttu-id="8e9ad-117">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="8e9ad-118">Tenga en cuenta que las elipses se mezclan con el fondo, pero no se combinan entre sí.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![Ilustración en la que se muestran dos elipses de colores diferentes, cada una de las cuales se combina con su fondo multicolor](images/sourcecopy.png)

<span data-ttu-id="8e9ad-120">El ejemplo de código anterior tiene la siguiente instrucción:</span><span class="sxs-lookup"><span data-stu-id="8e9ad-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="8e9ad-121">Si desea que los puntos suspensivos se mezclen entre sí y con el fondo, cambie la instrucción a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8e9ad-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="8e9ad-122">En la ilustración siguiente se muestra la salida del Código revisado.</span><span class="sxs-lookup"><span data-stu-id="8e9ad-122">The following illustration shows the output of the revised code.</span></span>

![usar el modo de composición para controlar la ilustración de la combinación alfa](images/sourceover.png)

 

 



