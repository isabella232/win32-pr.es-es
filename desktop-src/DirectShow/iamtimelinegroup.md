---
description: 'La interfaz IAMTimelineGroup establece y recupera propiedades en grupos en los servicios de edición de DirectShow (DES). Un grupo contiene una o más pistas y, posiblemente, una o más composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio. Los grupos son las composiciones más arriba en una escala de tiempo y también exponen la interfaz IAMTimelineComp. Una escala de tiempo puede contener varios grupos. Cada grupo tiene los siguientes atributos. Un tipo de medio asociado. Velocidad de fotogramas en la que se representa el grupo, en fotogramas por segundo (FPS). Todas las ediciones se producen en un momento redondeado al límite de fotogramas más cercano, según se define en la configuración de FPS del grupo. Un nivel de prioridad, para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo). Para crear un objeto de grupo, llame a IAMTimeline:: CreateEmptyNode con el grupo de tipo de escala de tiempo de valor \_ principal \_ \_ . Puede consultar el puntero IAMTimelineObj devuelto para la interfaz IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaz IAMTimelineGroup (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691063"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="353e1-107">Interfaz IAMTimelineGroup</span><span class="sxs-lookup"><span data-stu-id="353e1-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="353e1-108">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="353e1-108">\[Deprecated.</span></span> <span data-ttu-id="353e1-109">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="353e1-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="353e1-110">La `IAMTimelineGroup` interfaz establece y recupera propiedades en grupos en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="353e1-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="353e1-111">Un grupo contiene una o más pistas y, posiblemente, una o más composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="353e1-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="353e1-112">Los grupos son las composiciones más arriba en una escala de tiempo y también exponen la interfaz [**IAMTimelineComp**](iamtimelinecomp.md) .</span><span class="sxs-lookup"><span data-stu-id="353e1-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="353e1-113">Una escala de tiempo puede contener varios grupos.</span><span class="sxs-lookup"><span data-stu-id="353e1-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="353e1-114">Cada grupo tiene los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="353e1-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="353e1-115">Un tipo de medio asociado.</span><span class="sxs-lookup"><span data-stu-id="353e1-115">An associated media type.</span></span>
-   <span data-ttu-id="353e1-116">Velocidad de fotogramas en la que se representa el grupo, en fotogramas por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="353e1-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="353e1-117">Todas las ediciones se producen en un momento redondeado al límite de fotogramas más cercano, según se define en la configuración de FPS del grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="353e1-118">Un nivel de prioridad, para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo).</span><span class="sxs-lookup"><span data-stu-id="353e1-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="353e1-119">Para crear un objeto de grupo, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el grupo de tipo de escala de tiempo de valor \_ principal \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="353e1-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="353e1-120">Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la interfaz **IAMTimelineGroup** .</span><span class="sxs-lookup"><span data-stu-id="353e1-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="353e1-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="353e1-121">Members</span></span>

<span data-ttu-id="353e1-122">La interfaz **IAMTimelineGroup** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="353e1-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="353e1-123">**IAMTimelineGroup** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="353e1-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="353e1-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="353e1-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="353e1-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="353e1-125">Methods</span></span>

<span data-ttu-id="353e1-126">La interfaz **IAMTimelineGroup** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="353e1-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="353e1-127">Método</span><span class="sxs-lookup"><span data-stu-id="353e1-127">Method</span></span>                                                                            | <span data-ttu-id="353e1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="353e1-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="353e1-129">**ClearRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="353e1-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="353e1-130">No se admite.</span><span class="sxs-lookup"><span data-stu-id="353e1-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="353e1-131">**GetGroupName**</span><span class="sxs-lookup"><span data-stu-id="353e1-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="353e1-132">Recupera el nombre definido por la aplicación del grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="353e1-133">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="353e1-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="353e1-134">Recupera el tipo de medio sin comprimir para el grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="353e1-135">**GetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="353e1-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="353e1-136">Recupera el número de fotogramas representados de antemano durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="353e1-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="353e1-137">**GetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="353e1-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="353e1-138">Recupera la velocidad de fotogramas de salida de este grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="353e1-139">**GetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="353e1-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="353e1-140">Recupera el modo de vista previa para el grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="353e1-141">**GetPriority (**</span><span class="sxs-lookup"><span data-stu-id="353e1-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="353e1-142">Recupera la prioridad del grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="353e1-143">**GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="353e1-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="353e1-144">Recupera el formato de compresión actual para la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="353e1-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="353e1-145">**GetTimeline**</span><span class="sxs-lookup"><span data-stu-id="353e1-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="353e1-146">Recupera la escala de tiempo a la que pertenece este grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="353e1-147">**IsRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="353e1-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="353e1-148">No se admite.</span><span class="sxs-lookup"><span data-stu-id="353e1-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="353e1-149">**IsSmartRecompressFormatSet**</span><span class="sxs-lookup"><span data-stu-id="353e1-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="353e1-150">Determina si se ha establecido un formato de compresión inteligente para el grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="353e1-151">**SetGroupName**</span><span class="sxs-lookup"><span data-stu-id="353e1-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="353e1-152">Establece el nombre definido por la aplicación del grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="353e1-153">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="353e1-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="353e1-154">Establece el tipo de medio sin comprimir para el grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="353e1-155">**SetMediaTypeForVB**</span><span class="sxs-lookup"><span data-stu-id="353e1-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="353e1-156">Especifica el tipo de medio de grupo para los clientes de automatización.</span><span class="sxs-lookup"><span data-stu-id="353e1-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="353e1-157">**SetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="353e1-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="353e1-158">Especifica el número de fotogramas representados de antemano durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="353e1-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="353e1-159">**SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="353e1-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="353e1-160">Establece la velocidad de fotogramas de salida sin comprimir para este grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="353e1-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="353e1-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="353e1-162">Establece el modo de vista previa para el grupo.</span><span class="sxs-lookup"><span data-stu-id="353e1-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="353e1-163">**SetRecompFormatFromSource**</span><span class="sxs-lookup"><span data-stu-id="353e1-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="353e1-164">Establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="353e1-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="353e1-165">**SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="353e1-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="353e1-166">Especifica un formato de compresión que se va a utilizar para la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="353e1-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="353e1-167">**SetTimeline**</span><span class="sxs-lookup"><span data-stu-id="353e1-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="353e1-168">No se admite.</span><span class="sxs-lookup"><span data-stu-id="353e1-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="353e1-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353e1-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="353e1-170">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="353e1-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="353e1-171">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="353e1-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="353e1-172">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="353e1-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="353e1-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="353e1-173">Requirements</span></span>



| <span data-ttu-id="353e1-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="353e1-174">Requirement</span></span> | <span data-ttu-id="353e1-175">Value</span><span class="sxs-lookup"><span data-stu-id="353e1-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="353e1-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="353e1-176">Header</span></span><br/>  | <dl> <span data-ttu-id="353e1-177"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="353e1-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="353e1-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="353e1-178">Library</span></span><br/> | <dl> <span data-ttu-id="353e1-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="353e1-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
