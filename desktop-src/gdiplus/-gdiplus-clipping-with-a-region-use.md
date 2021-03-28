---
description: Una de las propiedades de la clase Graphics es la región de recorte. Todo el dibujo realizado por un objeto gráfico determinado está restringido a la región de recorte de ese objeto gráfico. Puede establecer la región de recorte llamando al método SetClip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Recorte con una región
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562416"
---
# <a name="clipping-with-a-region"></a><span data-ttu-id="d6a77-105">Recorte con una región</span><span class="sxs-lookup"><span data-stu-id="d6a77-105">Clipping with a Region</span></span>

<span data-ttu-id="d6a77-106">Una de las propiedades de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="d6a77-106">One of the properties of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the clipping region.</span></span> <span data-ttu-id="d6a77-107">Todo el dibujo realizado por un objeto **gráfico** determinado está restringido a la región de recorte de ese objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="d6a77-107">All drawing done by a given **Graphics** object is restricted to the clipping region of that **Graphics** object.</span></span> <span data-ttu-id="d6a77-108">Puede establecer la región de recorte llamando al método **SetClip** .</span><span class="sxs-lookup"><span data-stu-id="d6a77-108">You can set the clipping region by calling the **SetClip** method.</span></span>

<span data-ttu-id="d6a77-109">En el ejemplo siguiente se crea una ruta de acceso que consta de un solo polígono.</span><span class="sxs-lookup"><span data-stu-id="d6a77-109">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="d6a77-110">A continuación, el código crea una región basada en esa ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d6a77-110">Then the code constructs a region based on that path.</span></span> <span data-ttu-id="d6a77-111">La dirección de la región se pasa al método **SetClip** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibujan dos cadenas.</span><span class="sxs-lookup"><span data-stu-id="d6a77-111">The address of the region is passed to the **SetClip** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and then two strings are drawn.</span></span>


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



<span data-ttu-id="d6a77-112">En la ilustración siguiente se muestran las cadenas recortadas.</span><span class="sxs-lookup"><span data-stu-id="d6a77-112">The following illustration shows the clipped strings.</span></span>

![Ilustración que muestra partes de dos oraciones que aparecen dentro de una forma de cuatro lados](images/clip1.png)

 

 



