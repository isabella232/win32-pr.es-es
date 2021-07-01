---
description: 'Windows GDI+ usa tres espacios de coordenadas: mundo, página y dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120630"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="3d0e6-103">Tipos de sistemas de coordenadas</span><span class="sxs-lookup"><span data-stu-id="3d0e6-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="3d0e6-104">Windows GDI+ usa tres espacios de coordenadas: mundo, página y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="3d0e6-105">Al realizar la llamada , los puntos que se pasan al método `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` [**Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0, 0) y (160, 80) están en el espacio de coordenadas mundial.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="3d0e6-106">Antes de que GDI+ pueda dibujar la línea en la pantalla, las coordenadas pasan a través de una secuencia de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="3d0e6-107">Una transformación convierte las coordenadas globales en coordenadas de página y otra transformación convierte las coordenadas de página en coordenadas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="3d0e6-108">Imagine que quiere trabajar con un sistema de coordenadas que tenga su origen en el cuerpo del área cliente en lugar de en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="3d0e6-109">Por ejemplo, si quiere que el origen sea 100 píxeles desde el borde izquierdo del área cliente y 50 píxeles desde la parte superior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="3d0e6-110">En la ilustración siguiente se muestra este tipo de sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-110">The following illustration shows such a coordinate system.</span></span>

![captura de pantalla de una ventana que contiene ejes de coordenadas etiquetados](images/aboutgdip05-art01.png)

<span data-ttu-id="3d0e6-112">Al realizar la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` a , obtiene la línea que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![captura de pantalla de la ventana anterior, pero con una línea azul que se extiende diagonalmente desde el origen](images/aboutgdip05-art02.png)

<span data-ttu-id="3d0e6-114">Las coordenadas de los puntos de conexión de la línea en los tres espacios de coordenadas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="3d0e6-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="3d0e6-115">Space</span><span class="sxs-lookup"><span data-stu-id="3d0e6-115">Space</span></span>       |  <span data-ttu-id="3d0e6-116">Coordenadas del punto de conexión</span><span class="sxs-lookup"><span data-stu-id="3d0e6-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="3d0e6-117">World</span><span class="sxs-lookup"><span data-stu-id="3d0e6-117">World</span></span>  | <span data-ttu-id="3d0e6-118">(0, 0) a (160, 80)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="3d0e6-119">Página</span><span class="sxs-lookup"><span data-stu-id="3d0e6-119">Page</span></span>   | <span data-ttu-id="3d0e6-120">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="3d0e6-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d0e6-121">Device</span></span> | <span data-ttu-id="3d0e6-122">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="3d0e6-123">Tenga en cuenta que el espacio de coordenadas de página tiene su origen en la esquina superior izquierda del área cliente; este siempre será el caso.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="3d0e6-124">Tenga en cuenta también que, dado que la unidad de medida es el píxel, las coordenadas del dispositivo son las mismas que las coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="3d0e6-125">Si establece la unidad de medida en algo distinto de píxeles (por ejemplo, pulgadas), las coordenadas del dispositivo serán diferentes de las coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="3d0e6-126">La transformación que asigna coordenadas globales a coordenadas de página se denomina *transformación* del mundo y se mantiene mediante un [**objeto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="3d0e6-127">En el ejemplo anterior, la transformación del mundo es una traducción de 100 unidades en la dirección x y 50 unidades en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="3d0e6-128">En el ejemplo siguiente se establece la transformación del mundo de un **objeto Graphics** y, a continuación, se usa ese objeto **Graphics** para dibujar la línea mostrada en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="3d0e6-129">La transformación que asigna coordenadas de página a coordenadas de dispositivo se denomina transformación *de página*.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="3d0e6-130">La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona cuatro métodos para manipular e inspeccionar la transformación de página: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)y [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="3d0e6-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="3d0e6-131">La **clase Graphics** también proporciona dos métodos, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) y [**Graphics::GetDpiY,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)para examinar los puntos horizontales y verticales por pulgada del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="3d0e6-132">Puede usar el método [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar una unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="3d0e6-133">En el ejemplo siguiente se dibuja una línea de (0, 0) a (2, 1) donde el punto (2, 1) está 2 pulgadas a la derecha y 1 pulgada hacia abajo desde el punto (0, 0).</span><span class="sxs-lookup"><span data-stu-id="3d0e6-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="3d0e6-134">Si no especifica un ancho de lápiz al construir el lápiz, en el ejemplo anterior se dibujará una línea de una pulgada de ancho.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="3d0e6-135">Puede especificar el ancho del lápiz en el segundo argumento para el constructor [**Pen:**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="3d0e6-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="3d0e6-137">Si suponemos que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los puntos de conexión de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="3d0e6-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="3d0e6-138">Space</span><span class="sxs-lookup"><span data-stu-id="3d0e6-138">Space</span></span>       | <span data-ttu-id="3d0e6-139">Coordenadas del punto de conexión</span><span class="sxs-lookup"><span data-stu-id="3d0e6-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="3d0e6-140">World</span><span class="sxs-lookup"><span data-stu-id="3d0e6-140">World</span></span>  | <span data-ttu-id="3d0e6-141">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="3d0e6-142">Página</span><span class="sxs-lookup"><span data-stu-id="3d0e6-142">Page</span></span>   | <span data-ttu-id="3d0e6-143">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="3d0e6-144">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d0e6-144">Device</span></span> | <span data-ttu-id="3d0e6-145">(0, 0, a (192, 96)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="3d0e6-146">Puede combinar el mundo y las transformaciones de página para lograr diversos efectos.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="3d0e6-147">Por ejemplo, supongamos que quiere usar pulgadas como unidad de medida y desea que el origen del sistema de coordenadas esté a 2 pulgadas del borde izquierdo del área cliente y 1/2 pulgada desde la parte superior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="3d0e6-148">En el ejemplo siguiente se establecen las transformaciones de página y mundo de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibuja una línea de (0, 0) a (2, 1).</span><span class="sxs-lookup"><span data-stu-id="3d0e6-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="3d0e6-149">En la ilustración siguiente se muestra el sistema de líneas y coordenadas.</span><span class="sxs-lookup"><span data-stu-id="3d0e6-149">The following illustration shows the line and coordinate system.</span></span>

![captura de pantalla de la ventana anterior, pero más ancha, con los ejes situados a la izquierda y etiquetados de forma diferente](images/aboutgdip05-art03.png)

<span data-ttu-id="3d0e6-151">Si suponemos que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los puntos de conexión de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="3d0e6-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="3d0e6-152">Space</span><span class="sxs-lookup"><span data-stu-id="3d0e6-152">Space</span></span>       | <span data-ttu-id="3d0e6-153">Coordenadas del punto de conexión</span><span class="sxs-lookup"><span data-stu-id="3d0e6-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="3d0e6-154">World</span><span class="sxs-lookup"><span data-stu-id="3d0e6-154">World</span></span>  | <span data-ttu-id="3d0e6-155">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="3d0e6-156">Página</span><span class="sxs-lookup"><span data-stu-id="3d0e6-156">Page</span></span>   | <span data-ttu-id="3d0e6-157">(2, 0,5) a (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="3d0e6-158">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d0e6-158">Device</span></span> | <span data-ttu-id="3d0e6-159">(192, 48) a (384, 144)</span><span class="sxs-lookup"><span data-stu-id="3d0e6-159">(192, 48) to (384, 144)</span></span> |



 

 

 
