---
description: En este ejemplo se muestran dos métodos para buscar la tinta, dada una ubicación de pantalla.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Ejemplo de prueba de posicionamiento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715084"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="10973-103">Ejemplo de prueba de posicionamiento de tinta</span><span class="sxs-lookup"><span data-stu-id="10973-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="10973-104">En este ejemplo se muestran dos métodos para buscar la tinta, dada una ubicación de pantalla.</span><span class="sxs-lookup"><span data-stu-id="10973-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="10973-105">En este ejemplo se usan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="10973-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="10973-106">Usar un recolector de tinta</span><span class="sxs-lookup"><span data-stu-id="10973-106">Using an ink collector</span></span>
-   <span data-ttu-id="10973-107">Realización de una prueba de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="10973-107">Performing a hit test</span></span>
-   <span data-ttu-id="10973-108">Buscar el punto más cercano</span><span class="sxs-lookup"><span data-stu-id="10973-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="10973-109">Acceso a la API de entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="10973-109">Accessing the Ink API</span></span>

<span data-ttu-id="10973-110">En primer lugar, haga referencia a las clases de Tablet PC, que se encuentran en el kit de desarrollo de software (SDK) de Windows Vista o Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="10973-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="10973-111">Controlar los eventos de carga y de dibujo del formulario</span><span class="sxs-lookup"><span data-stu-id="10973-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="10973-112">El controlador de eventos de carga del formulario:</span><span class="sxs-lookup"><span data-stu-id="10973-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="10973-113">Crea un objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, para el formulario.</span><span class="sxs-lookup"><span data-stu-id="10973-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="10973-114">Establece la propiedad [si CollectionMode es](/previous-versions/ms836497(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para omitir los gestos.</span><span class="sxs-lookup"><span data-stu-id="10973-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="10973-115">Habilita [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="10973-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="10973-116">Establece la propiedad [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) en **true**.</span><span class="sxs-lookup"><span data-stu-id="10973-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="10973-117">El controlador de eventos Paint del formulario comprueba el modo de aplicación:</span><span class="sxs-lookup"><span data-stu-id="10973-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="10973-118">En el modo HitTest, pinta un círculo alrededor del cursor.</span><span class="sxs-lookup"><span data-stu-id="10973-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="10973-119">La plumilla activa se establece en el método handleHitTest de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10973-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="10973-120">En el modo NearestPoint, pinta una línea roja entre el cursor y el punto más cercano al cursor.</span><span class="sxs-lookup"><span data-stu-id="10973-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="10973-121">El punto más cercano se calcula en el método handleNearestPoint de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10973-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="10973-122">Este ejemplo tiene un algoritmo Repaint muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="10973-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="10973-123">Con su propiedad [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) establecida en **true**, el recopilador de tinta se vuelve a dibujar cuando se vuelve a dibujar el formulario.</span><span class="sxs-lookup"><span data-stu-id="10973-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="10973-124">Para simplificar la redibujo del formulario, la aplicación realiza un seguimiento de un cuadro de límite, la variable miembro invalidateRect, para el área en la que se agrega Paint, que se invalida cada vez que se vuelve a dibujar el formulario.</span><span class="sxs-lookup"><span data-stu-id="10973-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="10973-125">Control de eventos de menú</span><span class="sxs-lookup"><span data-stu-id="10973-125">Handling Menu Events</span></span>

<span data-ttu-id="10973-126">El comando Exit deshabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10973-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="10973-127">El comando de entrada manuscrita actualiza el modo de aplicación y el estado del menú, habilita el recopilador de tinta y invalida la región que se ha pintado previamente del formulario.</span><span class="sxs-lookup"><span data-stu-id="10973-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="10973-128">Los comandos de la prueba de posicionamiento y del punto más cercano cambian el cursor, actualizan el modo de aplicación y el estado del menú, deshabilitan el recopilador de tinta e invalidan la región dibujada anteriormente del formulario.</span><span class="sxs-lookup"><span data-stu-id="10973-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="10973-129">¡ Desactive!</span><span class="sxs-lookup"><span data-stu-id="10973-129">The Clear!</span></span> <span data-ttu-id="10973-130">el comando deshabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) mientras se reemplaza la propiedad de [entrada manuscrita](/previous-versions/ms836505(v=msdn.10)) del objeto InkCollector con un nuevo objeto de [entrada manuscrita](/previous-versions/ms571716(v=vs.100)) , genera un evento de comando de entrada manuscrita y fuerza una actualización en el control.</span><span class="sxs-lookup"><span data-stu-id="10973-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="10973-131">Controlar eventos del mouse</span><span class="sxs-lookup"><span data-stu-id="10973-131">Handling Mouse Events</span></span>

<span data-ttu-id="10973-132">El controlador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación:</span><span class="sxs-lookup"><span data-stu-id="10973-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="10973-133">En el modo de tinta, no hace nada, lo que permite que el recolector de tintas recopile normalmente la tinta.</span><span class="sxs-lookup"><span data-stu-id="10973-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="10973-134">En el modo HitTest, envía los argumentos de evento al método handleHitTest de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10973-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="10973-135">En el modo NearestPoint, envía los argumentos de evento al método handleNearestPoint de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10973-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="10973-136">Realización de una prueba de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="10973-136">Performing a Hit Test</span></span>

<span data-ttu-id="10973-137">El método handleHitTest de la aplicación crea dos puntos, la ubicación del cursor y un punto alcanza los píxeles distantes del cursor y, a continuación, convierte estos dos puntos de píxeles en coordenadas del espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="10973-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="10973-138">A continuación, el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa el método [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para buscar los trazos que se encuentran dentro de PT3. X-PT2. X las unidades de espacio de la tinta del cursor, PT2.</span><span class="sxs-lookup"><span data-stu-id="10973-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="10973-139">A continuación, el método handleHitTest establece el color de la pluma en función de si se han encontrado trazos, invalida la región invalidateRect, calcula una nueva región en la que se dibuja el círculo de la prueba de posicionamiento y, a continuación, invalida la nueva región.</span><span class="sxs-lookup"><span data-stu-id="10973-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="10973-140">Buscar el punto más cercano</span><span class="sxs-lookup"><span data-stu-id="10973-140">Locating the Nearest Point</span></span>

<span data-ttu-id="10973-141">El método handleNearestPoint de la aplicación crea dos puntos iguales a la ubicación del cursor, uno de estos puntos, PT, se convierte en el espacio de la tinta y se usa en la llamada al método NearestPoint del objeto de [entrada de lápiz](/previous-versions/ms836505(v=msdn.10)) de [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="10973-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="10973-142">El método NearestPoint devuelve el objeto de [trazo](/previous-versions/ms827842(v=msdn.10)) más cercano al punto y establece el parámetro de salida de índice de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="10973-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="10973-143">Si no hay trazos presentes, el método NearestPoint devuelve **null** y la ubicación del cursor se usa como el punto más cercano.</span><span class="sxs-lookup"><span data-stu-id="10973-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="10973-144">De lo contrario, se calcula la ubicación en el trazo que corresponde al índice de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="10973-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="10973-145">A continuación, las coordenadas de punto más cercanas se convierten a píxeles desde el espacio de tinta, el método handleNearestPoint invalida la región invalidateRect, calcula una nueva región en la que se dibuja la línea en el punto más cercano e invalida también la nueva región.</span><span class="sxs-lookup"><span data-stu-id="10973-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="10973-146">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="10973-146">Closing the Form</span></span>

<span data-ttu-id="10973-147">El método Dispose del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="10973-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
