---
description: 'Esta aplicación se basa en el ejemplo de colección de entradas de lápiz mostrando la eliminación de trazos de tinta. En el ejemplo se proporciona al usuario un menú que tiene cuatro modos de elegir: habilitada para tinta, borrado en cúspide, borrado en intersecciones y borrado de trazos.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Ejemplo de borrado de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540414"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="bc3df-104">Ejemplo de borrado de tinta</span><span class="sxs-lookup"><span data-stu-id="bc3df-104">Ink Erasing Sample</span></span>

<span data-ttu-id="bc3df-105">Esta aplicación se basa en el ejemplo de [colección de entradas de lápiz](ink-collection-sample.md) mostrando la eliminación de trazos de tinta.</span><span class="sxs-lookup"><span data-stu-id="bc3df-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="bc3df-106">En el ejemplo se proporciona al usuario un menú que tiene cuatro modos de elegir: habilitada para tinta, borrado en cúspide, borrado en intersecciones y borrado de trazos.</span><span class="sxs-lookup"><span data-stu-id="bc3df-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="bc3df-107">En el modo de entrada de lápiz, el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) recopila entradas de lápiz, tal como se muestra en el [ejemplo de colección de tinta](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bc3df-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="bc3df-108">En un modo de borrado, se borran los segmentos de trazos de tinta existentes que el usuario toca con el cursor.</span><span class="sxs-lookup"><span data-stu-id="bc3df-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="bc3df-109">Además, las cresta o las intersecciones se pueden marcar con un círculo rojo.</span><span class="sxs-lookup"><span data-stu-id="bc3df-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="bc3df-110">Las partes más interesantes de este ejemplo se encuentran en el `InkErase` controlador de eventos del formulario `OnPaint` y en las funciones de borrado a las que se llama desde el controlador de eventos del formulario `OnMouseMove` .</span><span class="sxs-lookup"><span data-stu-id="bc3df-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="bc3df-111">Rodear las elevaciones y las intersecciones</span><span class="sxs-lookup"><span data-stu-id="bc3df-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="bc3df-112">El controlador de `OnPaint` eventos del formulario pinta primero los trazos y, según el modo de aplicación, puede buscar y marcar todas las crestas o intersecciones con un pequeño círculo rojo.</span><span class="sxs-lookup"><span data-stu-id="bc3df-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="bc3df-113">Un cúspide marca el punto en el que un trazo cambia de dirección de repente.</span><span class="sxs-lookup"><span data-stu-id="bc3df-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="bc3df-114">Una intersección marca un punto en el que un trazo se cruza con él mismo u otro trazo.</span><span class="sxs-lookup"><span data-stu-id="bc3df-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="bc3df-115">El evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) se produce cada vez que se vuelve a dibujar un control.</span><span class="sxs-lookup"><span data-stu-id="bc3df-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="bc3df-116">El ejemplo obliga al formulario a dibujarse a sí mismo cada vez que se borra un trazo, o cuando el modo de aplicación cambia, utilizando el método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="bc3df-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="bc3df-117">En `PaintCusps` , el código recorre en iteración cada cúspide en cada trazo y dibuja un círculo rojo alrededor de él.</span><span class="sxs-lookup"><span data-stu-id="bc3df-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="bc3df-118">La propiedad [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del trazo devuelve los índices de los puntos dentro de un Stoke que corresponden a las crestas.</span><span class="sxs-lookup"><span data-stu-id="bc3df-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="bc3df-119">Además, tenga en cuenta el método [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10)) , que convierte el punto en coordenadas relevantes para el método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="bc3df-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="bc3df-120">En `PaintIntersections` , el código recorre en iteración cada trazo para buscar sus intersecciones con todo el conjunto de trazos.</span><span class="sxs-lookup"><span data-stu-id="bc3df-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="bc3df-121">Observe que se pasa al método [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del trazo una colección [Strokes](/previous-versions/ms827799(v=msdn.10)) y se devuelve una matriz de valores de índice de punto flotante que representan las intersecciones.</span><span class="sxs-lookup"><span data-stu-id="bc3df-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="bc3df-122">Después, el código calcula una coordenada X-Y para cada intersección y dibuja un círculo rojo alrededor de ella.</span><span class="sxs-lookup"><span data-stu-id="bc3df-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="bc3df-123">Controlar un lápiz que tiene dos extremos</span><span class="sxs-lookup"><span data-stu-id="bc3df-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="bc3df-124">Se definen tres controladores de eventos para el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para los eventos [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))y [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bc3df-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="bc3df-125">Cada controlador de eventos comprueba la propiedad [invertida](/previous-versions/ms839525(v=msdn.10)) del objeto [cursor](/previous-versions/ms839521(v=msdn.10)) para ver el final del lápiz que se está usando.</span><span class="sxs-lookup"><span data-stu-id="bc3df-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="bc3df-126">Cuando se invierte el lápiz:</span><span class="sxs-lookup"><span data-stu-id="bc3df-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="bc3df-127">El `myInkCollector_CursorDown` método hace que el trazo sea transparente.</span><span class="sxs-lookup"><span data-stu-id="bc3df-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="bc3df-128">El `myInkCollector_NewPackets` método borra los trazos.</span><span class="sxs-lookup"><span data-stu-id="bc3df-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="bc3df-129">El `myInkCollector_Stroke` método cancela el evento.</span><span class="sxs-lookup"><span data-stu-id="bc3df-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="bc3df-130">Los eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) se generan antes del evento [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bc3df-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="bc3df-131">Seguimiento del cursor</span><span class="sxs-lookup"><span data-stu-id="bc3df-131">Tracking the Cursor</span></span>

<span data-ttu-id="bc3df-132">Si el usuario usa un lápiz o un mouse, se generan eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bc3df-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="bc3df-133">El controlador de eventos MouseMove primero comprueba para determinar si el modo actual es un modo de borrado y si se presiona cualquier botón del mouse, y omite el evento si estos Estados no están presentes.</span><span class="sxs-lookup"><span data-stu-id="bc3df-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="bc3df-134">A continuación, el controlador de eventos convierte las coordenadas de píxel del cursor en coordenadas de espacio de la entrada de lápiz mediante el método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto de [representador](/previous-versions/ms828481(v=msdn.10)) y llama a uno de los métodos de borrado del código según el modo de borrado actual.</span><span class="sxs-lookup"><span data-stu-id="bc3df-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="bc3df-135">Borrar trazos</span><span class="sxs-lookup"><span data-stu-id="bc3df-135">Erasing Strokes</span></span>

<span data-ttu-id="bc3df-136">El `EraseStrokes` método toma la ubicación del cursor en el espacio de entrada y genera una colección de trazos que se encuentran en `HitTestRadius` unidades.</span><span class="sxs-lookup"><span data-stu-id="bc3df-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="bc3df-137">El `currentStroke` parámetro especifica un objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) que no se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="bc3df-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="bc3df-138">A continuación, se elimina la colección Strokes del recopilador y se vuelve a dibujar el formulario.</span><span class="sxs-lookup"><span data-stu-id="bc3df-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="bc3df-139">Borrar en intersecciones</span><span class="sxs-lookup"><span data-stu-id="bc3df-139">Erasing at Intersections</span></span>

<span data-ttu-id="bc3df-140">El `EraseAtIntersections` método recorre en iteración cada trazo que se encuentra dentro del radio de prueba y genera una matriz de intersecciones entre ese trazo y todos los demás trazos de la colección.</span><span class="sxs-lookup"><span data-stu-id="bc3df-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="bc3df-141">Si no se encuentra ninguna intersección, se elimina todo el trazo; de lo contrario, se ubica el punto más cercano del trazo al punto de prueba y, a partir de ese momento, se encuentran las intersecciones de cada lado del punto, que describen el segmento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="bc3df-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="bc3df-142">El método [Split](/previous-versions/ms828477(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, lo que deja intacto el resto del trazo.</span><span class="sxs-lookup"><span data-stu-id="bc3df-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="bc3df-143">Como en `EraseStrokes` , el formulario se vuelve a dibujar antes de que el método devuelva.</span><span class="sxs-lookup"><span data-stu-id="bc3df-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="bc3df-144">Borrar en crestas</span><span class="sxs-lookup"><span data-stu-id="bc3df-144">Erasing at Cusps</span></span>

<span data-ttu-id="bc3df-145">Para cada trazo que se encuentra dentro del radio de prueba, el `EraseAtCusps` método recupera la matriz de cresta del método [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc3df-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="bc3df-146">Cada extremo del trazo también es una cúspide, por lo que si el trazo solo tiene dos elevaciones, se elimina todo el trazo; de lo contrario, se ubica el punto más cercano del trazo al punto de prueba y, a partir de ese momento, se encuentran las intersecciones de cada lado del punto, que describen el segmento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="bc3df-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="bc3df-147">El método [Split](/previous-versions/ms828477(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, lo que deja intacto el resto del trazo.</span><span class="sxs-lookup"><span data-stu-id="bc3df-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="bc3df-148">Como en `EraseStrokes` , el formulario se vuelve a dibujar antes de que el método devuelva.</span><span class="sxs-lookup"><span data-stu-id="bc3df-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="bc3df-149">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="bc3df-149">Closing the Form</span></span>

<span data-ttu-id="bc3df-150">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="bc3df-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
