---
description: 'Puede habilitar la corrección gamma para un pincel de degradado pasando TRUE al método PathGradientBrush:: SetGammaCorrection de ese pincel.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicar la corrección gamma a un degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156233"
---
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="9a9a4-103">Aplicar la corrección gamma a un degradado</span><span class="sxs-lookup"><span data-stu-id="9a9a4-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="9a9a4-104">Puede habilitar la corrección gamma para un pincel de degradado pasando **true** al método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) de ese pincel.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="9a9a4-105">Puede deshabilitar la corrección gamma pasando **false** al método **PathGradientBrush:: SetGammaCorrection** .</span><span class="sxs-lookup"><span data-stu-id="9a9a4-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="9a9a4-106">La corrección gamma está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="9a9a4-107">En el ejemplo siguiente se crea un pincel de degradado lineal y se utiliza ese pincel para rellenar dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="9a9a4-108">El primer rectángulo se rellena sin corrección gamma y el segundo rectángulo se rellena con la corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



<span data-ttu-id="9a9a4-109">En la ilustración siguiente se muestran los dos rectángulos rellenos.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="9a9a4-110">El rectángulo superior, que no tiene corrección gamma, aparece oscuro en el centro.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="9a9a4-111">El rectángulo inferior, que tiene corrección gamma, parece tener una intensidad más uniforme.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![Ilustración que muestra dos rectángulos: el relleno en color de la primera varía en intensidad, el relleno del segundo varía menos](images/gammagradient1.png)

<span data-ttu-id="9a9a4-113">En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un trazado en forma de estrella.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="9a9a4-114">El código usa el pincel de degradado de trazado con la corrección gamma deshabilitada (valor predeterminado) para rellenar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="9a9a4-115">Después, el código pasa **true** al método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar la corrección gamma del pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="9a9a4-116">La llamada a [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) establece la transformación universal de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de modo que la siguiente llamada a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) llene una estrella situada a la derecha de la primera estrella.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="9a9a4-117">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="9a9a4-118">La estrella de la derecha tiene corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="9a9a4-119">Tenga en cuenta que la estrella de la izquierda, que no tiene corrección gamma, tiene áreas que aparecen oscuras.</span><span class="sxs-lookup"><span data-stu-id="9a9a4-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![la ilustración de la señal de 2 5 comienza con un relleno de degradado de color; el primero tiene áreas oscuras, la segunda no](images/gammagradient2.png)

 

 



