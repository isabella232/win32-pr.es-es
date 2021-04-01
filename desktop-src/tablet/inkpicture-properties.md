---
description: Esta sección contiene propiedades para el control InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propiedades de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817726"
---
# <a name="inkpicture-properties"></a><span data-ttu-id="2c399-103">Propiedades de InkPicture</span><span class="sxs-lookup"><span data-stu-id="2c399-103">InkPicture Properties</span></span>

<span data-ttu-id="2c399-104">Esta sección contiene propiedades para el control InkPicture.</span><span class="sxs-lookup"><span data-stu-id="2c399-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c399-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c399-105">Property</span></span></th>
<th><span data-ttu-id="2c399-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c399-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c399-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (propiedad)</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-108">Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> se vuelve a dibujar cuando se invalida la ventana (si el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> asociado actualmente al control InkPicture se vuelve a dibujar automáticamente cuando la ventana asociada a inkpicture recibe un mensaje WM_PAINT).</span><span class="sxs-lookup"><span data-stu-id="2c399-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="2c399-110">Obtiene o establece el color de fondo del control <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="2c399-111">El color de fondo predeterminado es el color de fondo de la ventana del sistema, que suele ser blanco.</span><span class="sxs-lookup"><span data-stu-id="2c399-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propiedad CollectingInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-113">Obtiene el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> está recopilando la entrada de lápiz (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Si CollectionMode es</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="2c399-115">Obtiene o establece el modo de recopilación que determina si se reconocen la tinta, los gestos o la entrada de lápiz y los gestos a medida que el usuario escribe.</span><span class="sxs-lookup"><span data-stu-id="2c399-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor (propiedad)</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-117">Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible para su uso en la región de entrada manuscrita del control <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="2c399-119">Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> que se va a conservar con la entrada de lápiz (solo en tiempo de diseño).</span><span class="sxs-lookup"><span data-stu-id="2c399-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propiedad DefaultDrawingAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-121">Obtiene o establece la colección <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predeterminada que se va a usar al dibujar y mostrar la entrada de lápiz (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propiedad DesiredPacketDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-123">Obtiene o establece la descripción del paquete del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propiedad DynamicRendering</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-125">Obtiene o establece el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> representa dinámicamente la entrada de lápiz a medida que se recopila.</span><span class="sxs-lookup"><span data-stu-id="2c399-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="2c399-127">Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> está en modo de entrada de lápiz, modo de eliminación o modo de edición o selección.</span><span class="sxs-lookup"><span data-stu-id="2c399-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="2c399-129">Obtiene o establece un valor que determina si el control <a href="inkpicture-control-reference.md">InkPicture</a> puede responder a los eventos generados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c399-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c399-130">Esta propiedad es equivalente a la propiedad <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="2c399-132">Obtiene o establece el valor que especifica si la entrada de lápiz se borra por trazo o por punto.</span><span class="sxs-lookup"><span data-stu-id="2c399-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="2c399-134">Obtiene o establece el valor que especifica el ancho de la punta del lápiz de borrador.</span><span class="sxs-lookup"><span data-stu-id="2c399-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Identificador</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="2c399-136">Obtiene el identificador de ventana al que está enlazado el control <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="2c399-137">(solo en tiempo de ejecución)</span><span class="sxs-lookup"><span data-stu-id="2c399-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrada de lápiz</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="2c399-139">Obtiene o establece el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> que está asociado al control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="2c399-141">Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> recopila entradas manuscritas (paquetes en el aire, cursor en eventos de intervalo, etc.).</span><span class="sxs-lookup"><span data-stu-id="2c399-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propiedad MarginX</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-143">Obtiene o establece el margen del eje x alrededor del rectángulo de la ventana en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2c399-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propiedad marginy</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-145">Obtiene o establece el margen del eje y alrededor del rectángulo de la ventana en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2c399-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propiedad MouseIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-147">Obtiene o establece el icono actual del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c399-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer (propiedad)</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-149">Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está encima de una parte determinada del control <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagen</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="2c399-151">Obtiene el archivo de gráficos que se va a mostrar en el control <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="2c399-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propiedad)</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-153">Obtiene o establece el objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> que se usa para dibujar la entrada de lápiz en el control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selección</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="2c399-155">Obtiene la colección <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actualmente seleccionada dentro del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="2c399-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="2c399-157">Obtiene o establece cómo controla el control la posición y el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c399-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propiedad SupportHighContrastInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-159">Obtiene un valor que especifica si la entrada de lápiz se representa como un solo color, color = COLOR_WINDOWTEXT (de la llamada a GetSystemMetrics) cuando el sistema está en modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="2c399-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c399-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="2c399-161">Obtiene o establece un valor que especifica si todas las interfaces de usuario de selección (el cuadro de límite de selección y los controladores de selección) se dibujan en contraste alto cuando el sistema está en modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="2c399-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c399-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propiedad de Tablet PC</strong></a></span><span class="sxs-lookup"><span data-stu-id="2c399-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="2c399-163">Obtiene el objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que el control <a href="inkpicture-control-reference.md">InkPicture</a> está usando actualmente para recopilar la entrada.</span><span class="sxs-lookup"><span data-stu-id="2c399-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

