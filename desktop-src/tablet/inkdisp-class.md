---
description: 'Clase InkDisp: representa los trazos de lápiz recopilados dentro de un espacio de entrada de lápiz.'
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Clase InkDisp (Msdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109993"
---
# <a name="inkdisp-class"></a><span data-ttu-id="c01c7-103">InkDisp (clase)</span><span class="sxs-lookup"><span data-stu-id="c01c7-103">InkDisp class</span></span>

<span data-ttu-id="c01c7-104">Representa los trazos de lápiz recopilados dentro de un espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c01c7-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="c01c7-105">**InkDisp** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c01c7-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="c01c7-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="c01c7-106">Events</span></span>](#events)
-   [<span data-ttu-id="c01c7-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c01c7-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="c01c7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c01c7-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="c01c7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c01c7-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="c01c7-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="c01c7-110">Events</span></span>

<span data-ttu-id="c01c7-111">La **clase InkDisp** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="c01c7-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="c01c7-112">Evento</span><span class="sxs-lookup"><span data-stu-id="c01c7-112">Event</span></span>                                    | <span data-ttu-id="c01c7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c01c7-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="c01c7-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="c01c7-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="c01c7-115">Se produce cuando se agrega un trazo al **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="c01c7-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="c01c7-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="c01c7-117">Se produce cuando se elimina un trazo del **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="c01c7-118">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c01c7-118">Interfaces</span></span>

<span data-ttu-id="c01c7-119">La **clase InkDisp** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c01c7-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="c01c7-120">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c01c7-120">Interface</span></span>    | <span data-ttu-id="c01c7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c01c7-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="c01c7-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="c01c7-122">**IInkDisp**</span></span> | <span data-ttu-id="c01c7-123">Este objeto implementa la interfaz COM **IInkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="c01c7-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="c01c7-124">Methods</span></span>

<span data-ttu-id="c01c7-125">La **clase InkDisp** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c01c7-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="c01c7-126">Método</span><span class="sxs-lookup"><span data-stu-id="c01c7-126">Method</span></span>                                                                   | <span data-ttu-id="c01c7-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="c01c7-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c01c7-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="c01c7-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="c01c7-129">Inserta una colección de trazos en el **objeto InkDisp** en el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c01c7-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c01c7-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="c01c7-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="c01c7-131">Indica si el [**objeto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) se puede convertir en un **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c01c7-132">**pinza**</span><span class="sxs-lookup"><span data-stu-id="c01c7-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="c01c7-133">Quita partes de un trazo o colección de trazos que están fuera de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c01c7-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c01c7-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="c01c7-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="c01c7-135">Copia la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c01c7-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="c01c7-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="c01c7-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="c01c7-137">Copia los [**objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenidos en el rectángulo conocido en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c01c7-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="c01c7-138">**ClipboardPaste**</span><span class="sxs-lookup"><span data-stu-id="c01c7-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="c01c7-139">Copia el [**objeto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) del Portapapeles en el **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="c01c7-140">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="c01c7-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="c01c7-141">Crea un objeto **InkDisp** duplicado.</span><span class="sxs-lookup"><span data-stu-id="c01c7-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="c01c7-142">**CreateStroke**</span><span class="sxs-lookup"><span data-stu-id="c01c7-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="c01c7-143">Crea un trazo a partir de puntos o datos de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c01c7-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="c01c7-144">**CreateStrokes**</span><span class="sxs-lookup"><span data-stu-id="c01c7-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="c01c7-145">Crea una [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para este **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="c01c7-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="c01c7-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="c01c7-147">Elimina un trazo del **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="c01c7-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="c01c7-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="c01c7-149">Elimina los trazos del **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="c01c7-150">**ExtractStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="c01c7-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="c01c7-151">Extrae trazos del **objeto InkDisp** y devuelve un nuevo objeto **InkDisp** que contiene los trazos extraídos.</span><span class="sxs-lookup"><span data-stu-id="c01c7-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="c01c7-152">**ExtractWithRectangle (método)**</span><span class="sxs-lookup"><span data-stu-id="c01c7-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="c01c7-153">Corta o copia trazos de un objeto de clase **InkDisp** existente y los pega en un nuevo objeto **InkDisp Class,** mediante el rectángulo conocido para determinar qué trazos extraer.</span><span class="sxs-lookup"><span data-stu-id="c01c7-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="c01c7-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c01c7-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="c01c7-155">Recupera el cuadro de límite de todos los trazos del **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="c01c7-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="c01c7-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="c01c7-157">Recupera la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está completamente dentro de un círculo conocido o que forma una intersección.</span><span class="sxs-lookup"><span data-stu-id="c01c7-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="c01c7-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="c01c7-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="c01c7-159">Recupera los trazos dentro de un área de selección de polilínea.</span><span class="sxs-lookup"><span data-stu-id="c01c7-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="c01c7-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="c01c7-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="c01c7-161">Recupera los trazos contenidos en un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c01c7-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c01c7-162">**Carga**</span><span class="sxs-lookup"><span data-stu-id="c01c7-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="c01c7-163">Rellena un nuevo objeto **InkDisp** con datos binarios conocidos.</span><span class="sxs-lookup"><span data-stu-id="c01c7-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="c01c7-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="c01c7-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="c01c7-165">Recupera el [**elemento IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dentro del **objeto InkDisp** más cercano a un punto conocido y, opcionalmente, proporciona información adicional.</span><span class="sxs-lookup"><span data-stu-id="c01c7-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="c01c7-166">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="c01c7-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="c01c7-167">Convierte la entrada de lápiz en un formato especificado y devuelve los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="c01c7-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="c01c7-168">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c01c7-168">Properties</span></span>

<span data-ttu-id="c01c7-169">La **clase InkDisp** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c01c7-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="c01c7-170">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c01c7-170">Property</span></span>                                                                           | <span data-ttu-id="c01c7-171">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c01c7-171">Access type</span></span>           | <span data-ttu-id="c01c7-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="c01c7-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c01c7-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="c01c7-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="c01c7-174">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c01c7-174">Read-only</span></span><br/>  | <span data-ttu-id="c01c7-175">Obtiene la [**colección IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) que se va a conservar con la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c01c7-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="c01c7-176">**Sucio**</span><span class="sxs-lookup"><span data-stu-id="c01c7-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="c01c7-177">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c01c7-177">Read/write</span></span><br/> | <span data-ttu-id="c01c7-178">Obtiene o establece el valor que indica si se ha modificado un **objeto InkDisp** desde la última vez que se guardó la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c01c7-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="c01c7-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="c01c7-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="c01c7-180">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c01c7-180">Read-only</span></span><br/>  | <span data-ttu-id="c01c7-181">Obtiene la colección de datos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c01c7-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="c01c7-182">**Trazos**</span><span class="sxs-lookup"><span data-stu-id="c01c7-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="c01c7-183">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c01c7-183">Read-only</span></span><br/>  | <span data-ttu-id="c01c7-184">Obtiene la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenida en el **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="c01c7-185">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c01c7-185">Remarks</span></span>

<span data-ttu-id="c01c7-186">Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="c01c7-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="c01c7-187">La primera creación de instancias de este objeto hace que también se cree una instancia de GDI+.</span><span class="sxs-lookup"><span data-stu-id="c01c7-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="c01c7-188">Un efecto secundario es que si usa un único objeto de entrada de lápiz en un bucle y lo crea y destruye dentro del bucle, hará que se cree una instancia de GDI+ una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="c01c7-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="c01c7-189">Esto puede provocar una degradación del rendimiento en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c01c7-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="c01c7-190">Para evitarlo, mantenga una única instancia de un objeto ink en todo momento mientras la aplicación usa la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="c01c7-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="c01c7-191">Un **objeto InkDisp** es un contenedor de datos de trazo (punto).</span><span class="sxs-lookup"><span data-stu-id="c01c7-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="c01c7-192">Los datos de trazo, o los puntos recopilados por el lápiz, se ponen en un **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="c01c7-193">La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene los datos de todos los trazos dentro del **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="c01c7-194">El [**objeto InkCollector,**](inkcollector-class.md) [**el objeto InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) recopilan puntos del dispositivo de entrada y los coloca en un **objeto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="c01c7-195">Estos objetos actúan básicamente como el origen que distribuye la entrada de lápiz en uno o varios objetos **InkDisp** diferentes, que actúan como contenedores que mantienen la entrada manuscrita distribuida.</span><span class="sxs-lookup"><span data-stu-id="c01c7-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="c01c7-196">El espacio de entrada de lápiz es un espacio de coordenadas virtual al que se asignan las coordenadas del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="c01c7-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="c01c7-197">Este espacio se fija en un sistema de coordenadas HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="c01c7-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="c01c7-198">En coordenadas de espacio de entrada de lápiz, un movimiento de 0 a 1 equivale a 1 unidad HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="c01c7-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="c01c7-199">Esta asignación facilita la relación de varios **objetos InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="c01c7-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="c01c7-200">El [**objeto InkRenderer**](inkrenderer-class.md) administra las asignaciones entre la entrada manuscrita y la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="c01c7-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01c7-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c01c7-201">Requirements</span></span>



| <span data-ttu-id="c01c7-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="c01c7-202">Requirement</span></span> | <span data-ttu-id="c01c7-203">Valor</span><span class="sxs-lookup"><span data-stu-id="c01c7-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01c7-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c01c7-204">Minimum supported client</span></span><br/> | <span data-ttu-id="c01c7-205">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="c01c7-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c01c7-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c01c7-206">Minimum supported server</span></span><br/> | <span data-ttu-id="c01c7-207">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c01c7-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c01c7-208">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c01c7-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="c01c7-209"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="c01c7-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c01c7-210">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c01c7-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="c01c7-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c01c7-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c01c7-212">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c01c7-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01c7-213">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="c01c7-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="c01c7-214">[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c01c7-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c01c7-215">**IInkTablet (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="c01c7-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

