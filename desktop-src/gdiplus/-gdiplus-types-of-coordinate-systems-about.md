---
description: 'Windows GDI+ usa tres espacios de coordenadas: World, Page y Device.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104557329"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="42557-103">Tipos de sistemas de coordenadas</span><span class="sxs-lookup"><span data-stu-id="42557-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="42557-104">Windows GDI+ usa tres espacios de coordenadas: World, Page y Device.</span><span class="sxs-lookup"><span data-stu-id="42557-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="42557-105">Cuando se realiza la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , los puntos que se pasan al método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0,0) y (160, 80) se encuentran en el espacio de coordenadas del mundo.</span><span class="sxs-lookup"><span data-stu-id="42557-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="42557-106">Antes de que GDI+ pueda dibujar la línea en la pantalla, las coordenadas pasan a través de una secuencia de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="42557-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="42557-107">Una transformación convierte coordenadas universales en coordenadas de página y otra transformación convierte las coordenadas de página en coordenadas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42557-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="42557-108">Supongamos que desea trabajar con un sistema de coordenadas que tiene su origen en el cuerpo del área cliente en lugar de en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="42557-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="42557-109">Por ejemplo, Imagine que desea que el origen sea 100 píxeles desde el borde izquierdo del área cliente y 50 píxeles desde la parte superior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="42557-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="42557-110">En la ilustración siguiente se muestra este tipo de sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="42557-110">The following illustration shows such a coordinate system.</span></span>

![captura de pantalla de una ventana que contiene ejes de coordenadas con etiqueta](images/aboutgdip05-art01.png)

<span data-ttu-id="42557-112">Al realizar la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , se obtiene la línea que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="42557-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![captura de pantalla de la ventana anterior, pero con una línea azul que se extiende diagonalmente desde el origen](images/aboutgdip05-art02.png)

<span data-ttu-id="42557-114">Las coordenadas de los extremos de la línea en los tres espacios de coordenadas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="42557-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="42557-115">World</span><span class="sxs-lookup"><span data-stu-id="42557-115">World</span></span>  | <span data-ttu-id="42557-116">(0,0) a (160, 80)</span><span class="sxs-lookup"><span data-stu-id="42557-116">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="42557-117">Página</span><span class="sxs-lookup"><span data-stu-id="42557-117">Page</span></span>   | <span data-ttu-id="42557-118">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="42557-118">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="42557-119">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="42557-119">Device</span></span> | <span data-ttu-id="42557-120">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="42557-120">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="42557-121">Tenga en cuenta que el espacio de coordenadas de la página tiene su origen en la esquina superior izquierda del área cliente; siempre será el caso.</span><span class="sxs-lookup"><span data-stu-id="42557-121">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="42557-122">Tenga en cuenta también que, dado que la unidad de medida es el píxel, las coordenadas del dispositivo son las mismas que las coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="42557-122">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="42557-123">Si establece la unidad de medida en un valor distinto de píxeles (por ejemplo, pulgadas), las coordenadas del dispositivo serán diferentes de las coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="42557-123">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="42557-124">La transformación que asigna coordenadas universales a coordenadas de página se denomina *transformación universal* y se mantiene mediante un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="42557-124">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="42557-125">En el ejemplo anterior, la transformación universal es una traducción de 100 unidades en la dirección x y 50 unidades en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="42557-125">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="42557-126">En el ejemplo siguiente se establece la transformación universal de un objeto **Graphics** y, a continuación, se usa ese objeto **Graphics** para dibujar la línea mostrada en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="42557-126">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="42557-127">La transformación que asigna coordenadas de página a coordenadas del dispositivo se denomina *transformación de página*.</span><span class="sxs-lookup"><span data-stu-id="42557-127">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="42557-128">La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona cuatro métodos para manipular e inspeccionar la transformación de página: [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)y [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="42557-128">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="42557-129">La clase **Graphics** también proporciona dos métodos, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) y [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), para examinar los puntos verticales y horizontales por pulgada del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="42557-129">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="42557-130">Puede usar el método [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar una unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="42557-130">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="42557-131">En el ejemplo siguiente se dibuja una línea de (0,0) a (2, 1) donde el punto (2, 1) tiene 2 pulgadas a la derecha y una pulgada hacia abajo desde el punto (0,0).</span><span class="sxs-lookup"><span data-stu-id="42557-131">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="42557-132">Si no especifica un ancho de lápiz al crear el lápiz, el ejemplo anterior dibujará una línea de ancho de una pulgada.</span><span class="sxs-lookup"><span data-stu-id="42557-132">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="42557-133">Puede especificar el ancho del lápiz en el segundo argumento del constructor [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :</span><span class="sxs-lookup"><span data-stu-id="42557-133">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="42557-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="42557-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="42557-135">Si damos por hecho que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los extremos de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="42557-135">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                     |
|--------|---------------------|
| <span data-ttu-id="42557-136">World</span><span class="sxs-lookup"><span data-stu-id="42557-136">World</span></span>  | <span data-ttu-id="42557-137">(0,0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="42557-137">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="42557-138">Página</span><span class="sxs-lookup"><span data-stu-id="42557-138">Page</span></span>   | <span data-ttu-id="42557-139">(0,0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="42557-139">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="42557-140">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="42557-140">Device</span></span> | <span data-ttu-id="42557-141">(0, 0, a (192, 96)</span><span class="sxs-lookup"><span data-stu-id="42557-141">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="42557-142">Puede combinar las transformaciones de página y el mundo para lograr una gran variedad de efectos.</span><span class="sxs-lookup"><span data-stu-id="42557-142">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="42557-143">Por ejemplo, supongamos que desea usar pulgadas como unidad de medida y desea que el origen del sistema de coordenadas sea 2 pulgadas desde el borde izquierdo del área de cliente y 1/2 de la pulgada desde la parte superior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="42557-143">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="42557-144">En el ejemplo siguiente se establecen las transformaciones mundo y página de un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibuja una línea de (0,0) a (2, 1).</span><span class="sxs-lookup"><span data-stu-id="42557-144">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="42557-145">En la ilustración siguiente se muestra la línea y el sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="42557-145">The following illustration shows the line and coordinate system.</span></span>

![captura de pantalla de la ventana anterior, pero más ancha, con los ejes situados a la izquierda y etiquetados de manera diferente](images/aboutgdip05-art03.png)

<span data-ttu-id="42557-147">Si damos por hecho que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los extremos de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="42557-147">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="42557-148">World</span><span class="sxs-lookup"><span data-stu-id="42557-148">World</span></span>  | <span data-ttu-id="42557-149">(0,0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="42557-149">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="42557-150">Página</span><span class="sxs-lookup"><span data-stu-id="42557-150">Page</span></span>   | <span data-ttu-id="42557-151">(2, 0,5) a (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="42557-151">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="42557-152">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="42557-152">Device</span></span> | <span data-ttu-id="42557-153">(192, 48) a (384, 144)</span><span class="sxs-lookup"><span data-stu-id="42557-153">(192, 48) to (384, 144)</span></span> |



 

 

 
