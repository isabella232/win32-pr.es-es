---
description: Este programa de ejemplo muestra cómo hacer zoom y desplazar la entrada manuscrita.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Ejemplo de zoom de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540406"
---
# <a name="ink-zoom-sample"></a><span data-ttu-id="33deb-103">Ejemplo de zoom de tinta</span><span class="sxs-lookup"><span data-stu-id="33deb-103">Ink Zoom Sample</span></span>

<span data-ttu-id="33deb-104">Este programa de ejemplo muestra cómo hacer zoom y desplazar la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="33deb-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="33deb-105">En concreto, permite al usuario acercar y alejar la entrada de lápiz en incrementos.</span><span class="sxs-lookup"><span data-stu-id="33deb-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="33deb-106">También muestra cómo hacer zoom en una región determinada mediante un rectángulo de zoom.</span><span class="sxs-lookup"><span data-stu-id="33deb-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="33deb-107">Por último, en este ejemplo se muestra cómo recopilar la entrada de lápiz con distintas proporciones de zoom y cómo configurar el desplazamiento dentro del área de dibujo ampliada.</span><span class="sxs-lookup"><span data-stu-id="33deb-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="33deb-108">En el ejemplo, las transformaciones vista y objeto del objeto [representador](/previous-versions/ms828481(v=msdn.10)) se utilizan para realizar el zoom y el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="33deb-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="33deb-109">La transformación de la vista se aplica a los puntos y al ancho del lápiz.</span><span class="sxs-lookup"><span data-stu-id="33deb-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="33deb-110">La transformación de objeto solo se aplica a los puntos.</span><span class="sxs-lookup"><span data-stu-id="33deb-110">The object transform applies only to the points.</span></span> <span data-ttu-id="33deb-111">El usuario puede controlar qué transformación se usa cambiando el elemento ancho del lápiz de escala en el menú modo.</span><span class="sxs-lookup"><span data-stu-id="33deb-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="33deb-112">Es problemático realizar algunas llamadas COM en determinados métodos de interfaz ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) y [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), por ejemplo) cuando se ha enviado un mensaje.</span><span class="sxs-lookup"><span data-stu-id="33deb-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="33deb-113">Cuando se envían mensajes, deben calcularse en la cola de mensajes posteriores.</span><span class="sxs-lookup"><span data-stu-id="33deb-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="33deb-114">Para abordar este escenario, pruebe si está controlando un mensaje desde POST llamando a [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) y envíe el mensaje a sí mismo si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="33deb-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="33deb-115">En este ejemplo se usan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="33deb-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="33deb-116">El objeto [InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="33deb-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="33deb-117">El método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="33deb-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="33deb-118">El método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="33deb-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="33deb-119">Inicializar el formulario</span><span class="sxs-lookup"><span data-stu-id="33deb-119">Initializing the Form</span></span>

<span data-ttu-id="33deb-120">En primer lugar, el ejemplo hace referencia a las interfaces de automatización de Tablet PC que se proporcionan en el kit de desarrollo de software (SDK) de Windows Vista o Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="33deb-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="33deb-121">En el ejemplo se declara un [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , y algunos miembros privados para ayudar con el escalado.</span><span class="sxs-lookup"><span data-stu-id="33deb-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



<span data-ttu-id="33deb-122">A continuación, el ejemplo crea y habilita [InkCollector](/previous-versions/ms583683(v=vs.100)) en el controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="33deb-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="33deb-123">Además, la propiedad [ancho](/previous-versions/ms837941(v=msdn.10)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector está establecida.</span><span class="sxs-lookup"><span data-stu-id="33deb-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="33deb-124">Por último, se definen los intervalos de la barra de desplazamiento y se llama al método de la aplicación `UpdateZoomAndScroll` .</span><span class="sxs-lookup"><span data-stu-id="33deb-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="33deb-125">Actualizar los valores de zoom y desplazamiento</span><span class="sxs-lookup"><span data-stu-id="33deb-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="33deb-126">Muchos eventos afectan al área de dibujo del recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="33deb-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="33deb-127">En el `UpdateZoomAndScroll` método, una matriz de transformación se usa para escalar y trasladar el recolector de tinta dentro de la ventana.</span><span class="sxs-lookup"><span data-stu-id="33deb-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="33deb-128">El método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10)) aplica la transformación a los trazos y al ancho del lápiz, mientras que el método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) solo aplica la transformación a los trazos.</span><span class="sxs-lookup"><span data-stu-id="33deb-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="33deb-129">Por último, se llama al método de la aplicación `UpdateScrollBars` y se fuerza la actualización del formulario.</span><span class="sxs-lookup"><span data-stu-id="33deb-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="33deb-130">Administrar las barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="33deb-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="33deb-131">El `UpdateScrollBars` método configura las barras de desplazamiento para que funcionen correctamente con el tamaño de la ventana actual, la configuración del zoom y la ubicación de desplazamiento en [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="33deb-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="33deb-132">Este método calcula el cambio grande y los valores pequeños para las barras de desplazamiento vertical y horizontal.</span><span class="sxs-lookup"><span data-stu-id="33deb-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="33deb-133">También calcula el valor actual de las barras de desplazamiento y si deben ser visibles.</span><span class="sxs-lookup"><span data-stu-id="33deb-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="33deb-134">El método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto de [representador](/previous-versions/ms828481(v=msdn.10)) controla la conversión de píxeles al espacio de coordenadas y a las cuentas de zoom para cualquier ajuste de escala y desplazamiento que se aplique a través de las transformaciones de objeto y vista.</span><span class="sxs-lookup"><span data-stu-id="33deb-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="33deb-135">Acercar un rectángulo</span><span class="sxs-lookup"><span data-stu-id="33deb-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="33deb-136">Los `pnlDrawingArea` controladores de eventos de panel administran el dibujo del rectángulo en la ventana.</span><span class="sxs-lookup"><span data-stu-id="33deb-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="33deb-137">Si el comando zoom to Rect está activado en el menú modo, el controlador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) llama al método de la aplicación `ZoomToRectangle` .</span><span class="sxs-lookup"><span data-stu-id="33deb-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="33deb-138">El `ZoomToRectangle` método calcula el ancho y el alto del rectángulo, comprueba las condiciones de límite, actualiza los valores de la barra de desplazamiento y el factor de escala y, a continuación, llama al método de la aplicación `UpdateZoomAndScroll` para aplicar la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="33deb-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="33deb-139">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="33deb-139">Closing the Form</span></span>

<span data-ttu-id="33deb-140">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="33deb-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
