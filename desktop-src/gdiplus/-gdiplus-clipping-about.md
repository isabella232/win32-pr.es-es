---
description: El recorte implica restringir el dibujo a una región determinada. En la ilustración siguiente se muestra la cadena &\# 0034; Hola&\# 0034; se recorta a una región en forma de corazón.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Recorte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082501"
---
# <a name="clipping-gdi"></a><span data-ttu-id="9dbcb-104">Recorte (GDI+)</span><span class="sxs-lookup"><span data-stu-id="9dbcb-104">Clipping (GDI+)</span></span>

<span data-ttu-id="9dbcb-105">El recorte implica restringir el dibujo a una región determinada.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-105">Clipping involves restricting drawing to a certain region.</span></span> <span data-ttu-id="9dbcb-106">En la ilustración siguiente se muestra la cadena "Hello" recortada en una región en forma de corazón.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-106">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>

![Ilustración que muestra partes de la cadena "Hello" dentro de un corazón rojo](images/aboutgdip02-art30.png)

<span data-ttu-id="9dbcb-108">Las regiones se pueden construir a partir de trazados y las rutas de acceso pueden contener los contornos de las cadenas, por lo que puede usar el texto esquematizado para el recorte.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-108">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="9dbcb-109">En la ilustración siguiente se muestra un conjunto de puntos suspensivos concéntricos recortados en el interior de una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-109">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>

![Ilustración que muestra la cadena "Hello" rellenada por un patrón de círculos concéntricos](images/aboutgdip02-art31.png)

<span data-ttu-id="9dbcb-111">Para dibujar con recorte, cree un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , llame a su método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) y, a continuación, llame a los métodos de dibujo de ese mismo objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="9dbcb-111">To draw with clipping, create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, call its [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method, and then call the drawing methods of that same **Graphics** object.</span></span> <span data-ttu-id="9dbcb-112">En el ejemplo siguiente se dibuja una línea que se recorta a una región rectangular.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-112">The following example draws a line that is clipped to a rectangular region.</span></span>


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



<span data-ttu-id="9dbcb-113">En la ilustración siguiente se muestra la región rectangular junto con la línea recortada.</span><span class="sxs-lookup"><span data-stu-id="9dbcb-113">The following illustration shows the rectangular region along with the clipped line.</span></span>

![Ilustración que muestra un rectángulo con una línea diagonal de arriba abajo](images/aboutgdip02-art31a.png)

 

 



