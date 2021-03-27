---
description: Un polígono es una figura cerrada con tres o más lados rectos.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809638"
---
# <a name="polygons"></a><span data-ttu-id="8d9f7-103">Polígonos</span><span class="sxs-lookup"><span data-stu-id="8d9f7-103">Polygons</span></span>

<span data-ttu-id="8d9f7-104">Un polígono es una figura cerrada con tres o más lados rectos.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="8d9f7-105">Por ejemplo, un triángulo es un polígono con tres lados, un rectángulo es un polígono con cuatro lados y un Pentágono es un polígono con cinco lados.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="8d9f7-106">En la ilustración siguiente se muestran varios polígonos.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-106">The following illustration shows several polygons.</span></span>

![Ilustración que muestra cinco polígonos de diferentes formas, tamaños y colores](images/aboutgdip02-art07.png)

<span data-ttu-id="8d9f7-108">Para dibujar un polígono, se necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y una matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (o [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).</span><span class="sxs-lookup"><span data-stu-id="8d9f7-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="8d9f7-109">El objeto **Graphics** proporciona el método [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="8d9f7-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="8d9f7-110">El objeto **Pen** almacena los atributos del polígono, como el ancho y el color de línea, y la matriz de objetos **Point** almacena los puntos que se van a conectar mediante líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="8d9f7-111">Las direcciones del objeto **Pen** y la matriz de objetos **Point** se pasan como argumentos al método DrawPolygon.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="8d9f7-112">En el ejemplo siguiente se dibuja un polígono de tres lados.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="8d9f7-113">Tenga en cuenta que solo hay tres puntos en **myPointArray**: (0,0), (50, 30) y (30, 60).</span><span class="sxs-lookup"><span data-stu-id="8d9f7-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="8d9f7-114">El método DrawPolygon cierra automáticamente el polígono dibujando una línea de (30, 60) de nuevo al punto inicial (0,0);</span><span class="sxs-lookup"><span data-stu-id="8d9f7-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="8d9f7-115">En la ilustración siguiente se muestra el polígono.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-115">The following illustration shows the polygon.</span></span>

![Ilustración en la que se muestra un triángulo en los ejes de coordenadas](images/aboutgdip02-art08.png)

 

 



