---
description: Este programa muestra cómo copiar y pegar entradas manuscritas en otra aplicación. También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto de entrada manuscrita existente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Ejemplo de Portapapeles de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541318"
---
# <a name="ink-clipboard-sample"></a><span data-ttu-id="fb32a-104">Ejemplo de Portapapeles de lápiz</span><span class="sxs-lookup"><span data-stu-id="fb32a-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="fb32a-105">Este programa muestra cómo copiar y pegar entradas manuscritas en otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb32a-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="fb32a-106">También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto de entrada manuscrita existente.</span><span class="sxs-lookup"><span data-stu-id="fb32a-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="fb32a-107">Están disponibles los siguientes modos del portapapeles:</span><span class="sxs-lookup"><span data-stu-id="fb32a-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="fb32a-108">Formato serializado de tinta (ISF)</span><span class="sxs-lookup"><span data-stu-id="fb32a-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="fb32a-109">Metarchivo de </span><span class="sxs-lookup"><span data-stu-id="fb32a-109">Metafile</span></span>
-   <span data-ttu-id="fb32a-110">Metarchivo mejorado (EMF)</span><span class="sxs-lookup"><span data-stu-id="fb32a-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="fb32a-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="fb32a-111">Bitmap</span></span>
-   <span data-ttu-id="fb32a-112">Entrada de texto</span><span class="sxs-lookup"><span data-stu-id="fb32a-112">Text Ink</span></span>
-   <span data-ttu-id="fb32a-113">Boceto de tinta</span><span class="sxs-lookup"><span data-stu-id="fb32a-113">Sketch Ink</span></span>

<span data-ttu-id="fb32a-114">La tinta de texto y el boceto son dos tipos de controles de entrada de lápiz que se usan como texto o dibujo respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fb32a-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="fb32a-115">Es posible pegar el ISF, la tinta de texto y el boceto de la tinta en una entrada manuscrita existente.</span><span class="sxs-lookup"><span data-stu-id="fb32a-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="fb32a-116">Además del portapapeles, este ejemplo también muestra cómo seleccionar trazos con la herramienta lazo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="fb32a-117">El usuario puede Desplace los trazos seleccionados y modificar sus atributos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="fb32a-118">Esta funcionalidad es un subconjunto de la funcionalidad de selección ya proporcionada por el control de superposición de tinta; se implementa aquí con fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="fb32a-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="fb32a-119">En este ejemplo se usan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="fb32a-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="fb32a-120">El objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="fb32a-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="fb32a-121">Compatibilidad con el portapapeles de lápiz.</span><span class="sxs-lookup"><span data-stu-id="fb32a-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="fb32a-122">El uso del lazo con el método [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="fb32a-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="fb32a-123">En este ejemplo se muestra la representación de la entrada manuscrita, la copia de esa tinta y la posterior pegada en otra aplicación, como Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="fb32a-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="fb32a-124">Recopilación de entradas manuscritas y configuración del formulario</span><span class="sxs-lookup"><span data-stu-id="fb32a-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="fb32a-125">En primer lugar, haga referencia a las interfaces de automatización de Tablet PC, que se instalan con el <entity type="reg"/> Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="fb32a-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="fb32a-126">A continuación, el formulario declara algunas constantes y campos que se indican más adelante en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



<span data-ttu-id="fb32a-127">Por último, en el controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, se inicializa el formulario, se crea un objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para el formulario y se habilita el recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="fb32a-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="fb32a-128">Control de eventos de menú</span><span class="sxs-lookup"><span data-stu-id="fb32a-128">Handling Menu Events</span></span>

<span data-ttu-id="fb32a-129">Los controladores de eventos del elemento de menú actualizan principalmente el estado del formulario.</span><span class="sxs-lookup"><span data-stu-id="fb32a-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="fb32a-130">El comando CLEAR quita el rectángulo de selección y elimina los trazos del objeto [Ink](/previous-versions/ms583670(v=vs.100)) del recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="fb32a-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="fb32a-131">El comando Exit deshabilita el recolector de tinta antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb32a-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="fb32a-132">El menú Edición habilita los comandos cortar y copiar según el estado de selección del formulario y permite el comando pegar basado en el contenido del portapapeles, determinado mediante el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="fb32a-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="fb32a-133">Los comandos cortar y copiar usan un método auxiliar para copiar la entrada manuscrita en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="fb32a-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="fb32a-134">El comando cortar usa un método auxiliar para eliminar los trazos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="fb32a-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="fb32a-135">El comando pegar comprueba primero el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) para ver si se puede pegar el objeto en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="fb32a-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="fb32a-136">A continuación, el comando pegar calcula la esquina superior izquierda de la región de pegado, convierte las coordenadas de píxeles al espacio de entrada y pega los trazos del portapapeles en el recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="fb32a-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="fb32a-137">Por último, se actualiza el cuadro de selección.</span><span class="sxs-lookup"><span data-stu-id="fb32a-137">Finally, the selection box is updated.</span></span>


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



<span data-ttu-id="fb32a-138">Los comandos SELECT y Ink actualizan el modo de aplicación y los atributos de dibujo predeterminados, borran la selección actual, actualizan el estado del menú y actualizan el formulario.</span><span class="sxs-lookup"><span data-stu-id="fb32a-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="fb32a-139">Otros controladores se basan en el estado de la aplicación para realizar la función correcta, ya sea con el lazo o la colocación de la tinta.</span><span class="sxs-lookup"><span data-stu-id="fb32a-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="fb32a-140">Además, el comando SELECT agrega los controladores de eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) y [Stroke](/previous-versions/ms567622(v=vs.100)) al recopilador de tinta y el comando de entrada manuscrita quita estos controladores de eventos del recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="fb32a-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="fb32a-141">Los formatos que están disponibles en el portapapeles cuando se copian los trazos se muestran en el menú Formato y el usuario selecciona el formato para copiar la tinta de esta lista.</span><span class="sxs-lookup"><span data-stu-id="fb32a-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="fb32a-142">Los tipos de formatos disponibles incluyen el formato serializado de tinta (ISF), el metarchivo, el metarchivo mejorado y el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fb32a-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="fb32a-143">Los formatos de tinta de boceto y de entrada de texto se excluyen mutuamente y dependen de que la tinta se copie en el portapapeles como un objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="fb32a-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="fb32a-144">El menú estilo permite al usuario cambiar las propiedades de color y ancho del lápiz y los trazos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="fb32a-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="fb32a-145">Por ejemplo, el comando rojo establece la propiedad [color](/previous-versions/ms582103(v=vs.100)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) del recopilador de tinta en el color rojo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="fb32a-146">Dado que no se ha establecido la propiedad [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) del objeto [cursor](/previous-versions/ms552104(v=vs.100)) , cualquier nueva entrada de lápiz que se dibuje en el recolector de tintas heredará del color de dibujo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fb32a-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="fb32a-147">Además, si hay trazos seleccionados actualmente, la propiedad color de los atributos de dibujo de cada trazo también se actualiza.</span><span class="sxs-lookup"><span data-stu-id="fb32a-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a><span data-ttu-id="fb32a-148">Controlar eventos del mouse</span><span class="sxs-lookup"><span data-stu-id="fb32a-148">Handling Mouse Events</span></span>

<span data-ttu-id="fb32a-149">El controlador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb32a-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="fb32a-150">Si el modo es MoveInk y un botón del mouse está inactivo, el controlador mueve los trazos usando el método move de la colección [Strokes](/previous-versions/ms552701(v=vs.100)) y actualiza el cuadro de selección.</span><span class="sxs-lookup"><span data-stu-id="fb32a-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="fb32a-151">De lo contrario, el controlador comprueba para determinar si el rectángulo de selección contiene el cursor, habilita la recopilación de entradas de lápiz en consecuencia y también establece el cursor según corresponda.</span><span class="sxs-lookup"><span data-stu-id="fb32a-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="fb32a-152">El controlador de eventos [MouseDown](/previous-versions/ms567616(v=vs.100)) comprueba la configuración del cursor.</span><span class="sxs-lookup"><span data-stu-id="fb32a-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="fb32a-153">Si el cursor se establece en [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), el controlador establece el modo de aplicación en MoveInk y registra la ubicación del cursor.</span><span class="sxs-lookup"><span data-stu-id="fb32a-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="fb32a-154">De lo contrario, si hay una selección actual, desactívela.</span><span class="sxs-lookup"><span data-stu-id="fb32a-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="fb32a-155">El controlador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) comprueba el modo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb32a-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="fb32a-156">Si el modo es MoveInk, el controlador establece el modo de aplicación basado en el estado de activación del comando SELECT.</span><span class="sxs-lookup"><span data-stu-id="fb32a-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="fb32a-157">El evento [NewPackets](/previous-versions/ms567621(v=vs.100)) se desencadena en el modo de selección cuando el recopilador de tinta recibe nuevos datos de paquete.</span><span class="sxs-lookup"><span data-stu-id="fb32a-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="fb32a-158">Si la aplicación está en modo de selección, es necesario interceptar los nuevos paquetes y usarlos para dibujar el lazo de selección.</span><span class="sxs-lookup"><span data-stu-id="fb32a-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="fb32a-159">La coordenada de cada paquete se convierte en píxeles, se restringe al área de dibujo y se agrega a la colección de puntos del lazo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="fb32a-160">A continuación, se llama a un método auxiliar para dibujar el lazo en el formulario.</span><span class="sxs-lookup"><span data-stu-id="fb32a-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="fb32a-161">Controlar un nuevo trazo</span><span class="sxs-lookup"><span data-stu-id="fb32a-161">Handling a New Stroke</span></span>

<span data-ttu-id="fb32a-162">El evento [Stroke](/previous-versions/ms567622(v=vs.100)) se desencadena en el modo de selección cuando se dibuja un nuevo trazo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="fb32a-163">Si la aplicación está en modo de selección, este trazo corresponde al lazo y es necesario actualizar la información de los trazos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="fb32a-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="fb32a-164">El controlador cancela el evento [Stroke](/previous-versions/ms567622(v=vs.100)) , comprueba si hay más de dos puntos de lazo, copia la colección Points en una matriz de objetos [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) y convierte las coordenadas de los puntos de la matriz de píxeles a espacio de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="fb32a-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="fb32a-165">A continuación, el controlador usa el método [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) del objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) para obtener los trazos seleccionados por los puntos de lazo y actualiza el estado de selección del formulario.</span><span class="sxs-lookup"><span data-stu-id="fb32a-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="fb32a-166">Por último, el trazo que provocó el evento se quita de la colección de trazos seleccionados, se vacía la colección de puntos de lazo y un método auxiliar dibuja el rectángulo de selección.</span><span class="sxs-lookup"><span data-stu-id="fb32a-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="fb32a-167">Copiar la entrada manuscrita en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="fb32a-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="fb32a-168">El método auxiliar CopyInkToClipboard crea un valor de [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , comprueba el estado del menú Formato para actualizar los formatos que se van a colocar en el portapapeles y usa el método [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) del objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) para copiar los trazos en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="fb32a-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a><span data-ttu-id="fb32a-169">Actualizar una selección</span><span class="sxs-lookup"><span data-stu-id="fb32a-169">Updating a Selection</span></span>

<span data-ttu-id="fb32a-170">El método auxiliar SetSelection actualiza el selectedStrokes archivado y si la colección es **null** o está **vacía**, el rectángulo de selección se establece en el rectángulo vacío.</span><span class="sxs-lookup"><span data-stu-id="fb32a-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="fb32a-171">Si la colección de [trazos](/previous-versions/ms552701(v=vs.100)) seleccionada no está vacía, el método SetSelection realiza los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="fb32a-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="fb32a-172">Determina el rectángulo delimitador mediante el método [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) de la colección Strokes.</span><span class="sxs-lookup"><span data-stu-id="fb32a-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="fb32a-173">Convierte las coordenadas del rectángulo del espacio de entrada en píxeles</span><span class="sxs-lookup"><span data-stu-id="fb32a-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="fb32a-174">Aumenta el rectángulo para proporcionar un espacio visual entre él y los trazos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="fb32a-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="fb32a-175">Crea controladores de selección para el cuadro de selección actual.</span><span class="sxs-lookup"><span data-stu-id="fb32a-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="fb32a-176">Por último, el método SetSelection establece la visibilidad de los controladores de selección y establece la propiedad [AutoRedraw](/previous-versions/ms571706(v=vs.100)) del recopilador de tinta en **false**, si se seleccionan los trazos.</span><span class="sxs-lookup"><span data-stu-id="fb32a-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a><span data-ttu-id="fb32a-177">Dibujo del lazo</span><span class="sxs-lookup"><span data-stu-id="fb32a-177">Drawing the Lasso</span></span>

<span data-ttu-id="fb32a-178">El lazo se dibuja como una serie de puntos abiertos que siguen la ruta de acceso del trazo de lazo y una línea de conector discontinua entre los dos extremos.</span><span class="sxs-lookup"><span data-stu-id="fb32a-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="fb32a-179">El evento [NewPackets](/previous-versions/ms567621(v=vs.100)) se genera cuando se dibuja el lazo y el controlador de eventos pasa la información del trazo al método DrawLasso.</span><span class="sxs-lookup"><span data-stu-id="fb32a-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="fb32a-180">El método auxiliar DrawLasso quita primero la línea del conector anterior y, a continuación, recorre en iteración los puntos del trazo.</span><span class="sxs-lookup"><span data-stu-id="fb32a-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="fb32a-181">A continuación, DrawLasso calcula dónde se colocan los puntos a lo largo del trazo y los dibuja.</span><span class="sxs-lookup"><span data-stu-id="fb32a-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="fb32a-182">Por último, dibuja una nueva línea de conector.</span><span class="sxs-lookup"><span data-stu-id="fb32a-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="fb32a-183">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="fb32a-183">Closing the Form</span></span>

<span data-ttu-id="fb32a-184">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , myInkCollector.</span><span class="sxs-lookup"><span data-stu-id="fb32a-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
