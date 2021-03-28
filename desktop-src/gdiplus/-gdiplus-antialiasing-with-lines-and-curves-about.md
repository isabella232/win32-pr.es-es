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
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="b3a6e-103">Suavizado de contorno con líneas y curvas</span><span class="sxs-lookup"><span data-stu-id="b3a6e-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="b3a6e-104">Cuando se usa Windows GDI+ para dibujar una línea, se proporciona el punto inicial y el punto final de la línea, pero no es necesario proporcionar información sobre los píxeles individuales de la línea.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="b3a6e-105">GDI+ funciona junto con el software del controlador de pantalla para determinar qué píxeles se activarán para mostrar la línea en un dispositivo de pantalla determinado.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="b3a6e-106">Considere una línea roja recta que va desde el punto (4, 2) hasta el punto (16, 10).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="b3a6e-107">Suponga que el sistema de coordenadas tiene su origen en la esquina superior izquierda y que la unidad de medida es el píxel.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="b3a6e-108">Supongamos también que el eje x apunta hacia la derecha y el eje y apunta hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="b3a6e-109">En la ilustración siguiente se muestra una vista ampliada de la línea roja dibujada en un fondo multicolor.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![Ilustración que muestra píxeles rojos sólidos en un fondo multicolor](images/aboutgdip02-art33.png)

<span data-ttu-id="b3a6e-111">Tenga en cuenta que los píxeles rojos utilizados para representar la línea son opacos.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="b3a6e-112">No hay píxeles parcialmente transparentes implicados en la visualización de la línea.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="b3a6e-113">Este tipo de representación de línea proporciona a la línea una apariencia escalonada y la línea es un poco similar a una escalera.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="b3a6e-114">Esta técnica de representar una línea con una escalera se denomina aliasing; la escalera es un alias de la línea teórica.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="b3a6e-115">Una técnica más sofisticada para representar una línea implica el uso de píxeles parcialmente transparentes junto con píxeles rojos puros.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="b3a6e-116">Los píxeles se establecen en rojo puro o en alguna mezcla de rojo y el color de fondo en función de la proximidad de la línea.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="b3a6e-117">Este tipo de representación se denomina suavizado de contorno y da como resultado una línea que el ojo humano percibe como más suave.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="b3a6e-118">En la ilustración siguiente se muestra cómo determinados píxeles se combinan con el fondo para producir una línea alisada.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![Ilustración en la que se muestran los píxeles que son sombras de color rojo en el mismo fondo](images/aboutgdip02-art34.png)

<span data-ttu-id="b3a6e-120">El suavizado de contorno (Smoothing) también se puede aplicar a curvas.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="b3a6e-121">En la ilustración siguiente se muestra una vista ampliada de una elipse suavizada.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![Ilustración de una elipse formada por diferentes sombras de píxeles azules en un fondo blanco](images/aboutgdip02-art35.png)

<span data-ttu-id="b3a6e-123">En la ilustración siguiente se muestra la misma elipse en su tamaño real, una vez sin suavizado de contorno y una vez con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![captura de pantalla de dos elipses: la que tiene el suavizado de contorno parece más suave](images/aboutgdip02-art36.png)

<span data-ttu-id="b3a6e-125">Para dibujar líneas y curvas que utilicen el suavizado de contorno, cree un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y pase *SmoothingModeAntiAlias* a su método [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="b3a6e-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="b3a6e-126">A continuación, llame a uno de los métodos de dibujo de ese mismo objeto de **gráficos** .</span><span class="sxs-lookup"><span data-stu-id="b3a6e-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="b3a6e-127">**SmoothingModeAntiAlias** es un elemento de la enumeración [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="b3a6e-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



