---
description: Representa la administración de las asignaciones de entrada manuscrita a la ventana de presentación. Use el objeto InkRenderer para mostrar la entrada de lápiz en una ventana. También se puede usar para cambiar la posición y el tamaño del trazo.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Clase InkRenderer (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279383"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="f620e-105">Clase InkRenderer</span><span class="sxs-lookup"><span data-stu-id="f620e-105">InkRenderer class</span></span>

<span data-ttu-id="f620e-106">Representa la administración de las asignaciones de entrada manuscrita a la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="f620e-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="f620e-107">Use el objeto **InkRenderer** para mostrar la entrada de lápiz en una ventana.</span><span class="sxs-lookup"><span data-stu-id="f620e-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="f620e-108">También se puede usar para cambiar la posición y el tamaño del trazo.</span><span class="sxs-lookup"><span data-stu-id="f620e-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="f620e-109">**InkRenderer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f620e-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="f620e-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f620e-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="f620e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f620e-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="f620e-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f620e-112">Interfaces</span></span>

<span data-ttu-id="f620e-113">La clase **InkRenderer** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f620e-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="f620e-114">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f620e-114">Interface</span></span>        | <span data-ttu-id="f620e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f620e-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="f620e-116">**IInkRenderer**</span><span class="sxs-lookup"><span data-stu-id="f620e-116">**IInkRenderer**</span></span> | <span data-ttu-id="f620e-117">Este objeto implementa la interfaz com **IInkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="f620e-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="f620e-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="f620e-118">Methods</span></span>

<span data-ttu-id="f620e-119">La clase **InkRenderer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f620e-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="f620e-120">Método</span><span class="sxs-lookup"><span data-stu-id="f620e-120">Method</span></span>                                                                     | <span data-ttu-id="f620e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f620e-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f620e-122">**Dibujar**</span><span class="sxs-lookup"><span data-stu-id="f620e-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="f620e-123">Dibuja trazos en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f620e-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="f620e-124">**DrawStroke**</span><span class="sxs-lookup"><span data-stu-id="f620e-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="f620e-125">Dibuja un trazo en el contexto de dispositivo de Windows especificado.</span><span class="sxs-lookup"><span data-stu-id="f620e-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f620e-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="f620e-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="f620e-127">Recupera la transformación de objeto que se usó para representar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f620e-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f620e-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="f620e-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="f620e-129">Recupera la transformación de vista que se usa para representar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f620e-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="f620e-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="f620e-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="f620e-131">Convierte una ubicación en coordenadas de espacio de tinta para que esté en el espacio en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f620e-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="f620e-132">**InkSpaceToPixelFromPoints**</span><span class="sxs-lookup"><span data-stu-id="f620e-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="f620e-133">Convierte una matriz de puntos en las coordenadas del espacio de entrada en el espacio en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f620e-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="f620e-134">**Medi**</span><span class="sxs-lookup"><span data-stu-id="f620e-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="f620e-135">Calcula el rectángulo en el contexto del dispositivo que contendría una colección de trazos si se dibujaron con el objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="f620e-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="f620e-136">**MeasureStroke**</span><span class="sxs-lookup"><span data-stu-id="f620e-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="f620e-137">Calcula el rectángulo en el contexto del dispositivo que contendría un trazo si se dibujó con el objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="f620e-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="f620e-138">**Move**</span><span class="sxs-lookup"><span data-stu-id="f620e-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="f620e-139">Aplica una traslación a la transformación de la vista en coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="f620e-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="f620e-140">**PixelToInkSpace**</span><span class="sxs-lookup"><span data-stu-id="f620e-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="f620e-141">Convierte una ubicación en coordenadas de píxeles para que esté en el espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="f620e-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f620e-142">**PixelToInkSpaceFromPoints**</span><span class="sxs-lookup"><span data-stu-id="f620e-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="f620e-143">Convierte una matriz de puntos en coordenadas de espacio en píxeles en el espacio de la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f620e-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="f620e-144">**Girar**</span><span class="sxs-lookup"><span data-stu-id="f620e-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="f620e-145">Aplica un giro a la transformación de la vista.</span><span class="sxs-lookup"><span data-stu-id="f620e-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="f620e-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="f620e-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="f620e-147">Escala la transformación de la vista en la dimensión X e y.</span><span class="sxs-lookup"><span data-stu-id="f620e-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f620e-148">**SetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="f620e-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="f620e-149">Establece la transformación de objeto que se usa para representar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f620e-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f620e-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="f620e-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="f620e-151">Establece la transformación de la vista que se utiliza para representar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f620e-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="f620e-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f620e-152">Remarks</span></span>

<span data-ttu-id="f620e-153">La impresión también se realiza a través del objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="f620e-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="f620e-154">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="f620e-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="f620e-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f620e-155">Requirements</span></span>



| <span data-ttu-id="f620e-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f620e-156">Requirement</span></span> | <span data-ttu-id="f620e-157">Value</span><span class="sxs-lookup"><span data-stu-id="f620e-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f620e-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f620e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f620e-159">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f620e-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f620e-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f620e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f620e-161">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f620e-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f620e-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f620e-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f620e-163"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f620e-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f620e-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f620e-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="f620e-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f620e-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f620e-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="f620e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f620e-167">**Renderer (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="f620e-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="f620e-168">**Clase InkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="f620e-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="f620e-169">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="f620e-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="f620e-170">[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f620e-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

