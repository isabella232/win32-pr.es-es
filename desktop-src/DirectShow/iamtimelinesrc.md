---
description: La interfaz IAMTimelineSrc proporciona métodos para manipular y establecer las propiedades de los objetos de origen en los servicios de edición de DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaz IAMTimelineSrc (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679053"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="186a5-103">Interfaz IAMTimelineSrc</span><span class="sxs-lookup"><span data-stu-id="186a5-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="186a5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="186a5-104">\[Deprecated.</span></span> <span data-ttu-id="186a5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="186a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="186a5-106">La `IAMTimelineSrc` interfaz proporciona métodos para manipular y establecer las propiedades de los objetos de origen en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="186a5-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="186a5-107">Un objeto de origen representa una secuencia de un origen de multimedia.</span><span class="sxs-lookup"><span data-stu-id="186a5-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="186a5-108">Puede usar una parte de los datos de un archivo de código fuente estableciendo las horas de inicio y detención del medio.</span><span class="sxs-lookup"><span data-stu-id="186a5-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="186a5-109">Estos valores especifican el principio y el final del objeto de origen, en relación con el origen del medio original.</span><span class="sxs-lookup"><span data-stu-id="186a5-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="186a5-110">Los tiempos de los medios pueden diferir de los tiempos de inicio y detención del objeto en la escala de tiempo, lo que permite la reproducción rápida o lenta.</span><span class="sxs-lookup"><span data-stu-id="186a5-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="186a5-111">(Con orígenes de audio, se produce el cambio de tono).</span><span class="sxs-lookup"><span data-stu-id="186a5-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="186a5-112">Para crear un objeto de origen, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor de origen de tipo principal de la escala de tiempo \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="186a5-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="186a5-113">Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la interfaz **IAMTimelineSrc** .</span><span class="sxs-lookup"><span data-stu-id="186a5-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="186a5-114">Para obtener más información, vea [crear una escala de tiempo](constructing-a-timeline.md) y [trabajar con orígenes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="186a5-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="186a5-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="186a5-115">Members</span></span>

<span data-ttu-id="186a5-116">La interfaz **IAMTimelineSrc** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="186a5-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="186a5-117">**IAMTimelineSrc** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="186a5-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="186a5-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="186a5-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="186a5-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="186a5-119">Methods</span></span>

<span data-ttu-id="186a5-120">La interfaz **IAMTimelineSrc** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="186a5-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="186a5-121">Método</span><span class="sxs-lookup"><span data-stu-id="186a5-121">Method</span></span>                                                    | <span data-ttu-id="186a5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="186a5-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="186a5-123">**FixMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="186a5-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="186a5-124">Redondea los valores de hora especificados al límite de fotogramas más cercano.</span><span class="sxs-lookup"><span data-stu-id="186a5-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="186a5-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="186a5-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="186a5-126">Redondea los valores de hora especificados, dados como valores de **REFTIME** , al límite de fotogramas más cercano.</span><span class="sxs-lookup"><span data-stu-id="186a5-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="186a5-127">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="186a5-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="186a5-128">Recupera la velocidad de fotogramas predeterminada del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="186a5-129">**GetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="186a5-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="186a5-130">Recupera la longitud del medio de este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="186a5-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="186a5-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="186a5-132">Recupera la longitud del medio de este objeto de origen, como un valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="186a5-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="186a5-133">**GetMediaName**</span><span class="sxs-lookup"><span data-stu-id="186a5-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="186a5-134">Recupera el nombre del archivo de código fuente representado por este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="186a5-135">**GetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="186a5-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="186a5-136">Recupera las horas de inicio y detención del medio.</span><span class="sxs-lookup"><span data-stu-id="186a5-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="186a5-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="186a5-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="186a5-138">Recupera las horas de inicio y detención del medio, como valores de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="186a5-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="186a5-139">**GetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="186a5-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="186a5-140">Recupera el número de secuencia actual para el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="186a5-141">**GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="186a5-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="186a5-142">Recupera el modo de ajuste de una fuente de vídeo.</span><span class="sxs-lookup"><span data-stu-id="186a5-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="186a5-143">**IsNormalRate**</span><span class="sxs-lookup"><span data-stu-id="186a5-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="186a5-144">Indica si el clip se reproducirá a la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="186a5-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="186a5-145">**ModifyStopTime**</span><span class="sxs-lookup"><span data-stu-id="186a5-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="186a5-146">Establece la hora de detención, relativa a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="186a5-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="186a5-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="186a5-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="186a5-148">Establece la hora de detención, como un valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="186a5-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="186a5-149">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="186a5-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="186a5-150">Establece la velocidad de fotogramas predeterminada del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="186a5-151">**SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="186a5-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="186a5-152">Especifica la duración del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="186a5-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="186a5-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="186a5-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="186a5-154">Especifica la duración del archivo de código fuente, como un valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="186a5-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="186a5-155">**SetMediaName**</span><span class="sxs-lookup"><span data-stu-id="186a5-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="186a5-156">Especifica el nombre del archivo de origen representado por este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="186a5-157">**SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="186a5-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="186a5-158">Establece las horas de detención e inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="186a5-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="186a5-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="186a5-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="186a5-160">Establece las horas de detención e inicio del medio, como valores de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="186a5-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="186a5-161">**SetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="186a5-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="186a5-162">Especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="186a5-163">**SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="186a5-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="186a5-164">Establece el modo de stretch de un origen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="186a5-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="186a5-165">**SpliceWithNext**</span><span class="sxs-lookup"><span data-stu-id="186a5-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="186a5-166">Une este objeto de origen a otro objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="186a5-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="186a5-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="186a5-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="186a5-168">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="186a5-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="186a5-169">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="186a5-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="186a5-170">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="186a5-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="186a5-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186a5-171">Requirements</span></span>



| <span data-ttu-id="186a5-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="186a5-172">Requirement</span></span> | <span data-ttu-id="186a5-173">Value</span><span class="sxs-lookup"><span data-stu-id="186a5-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="186a5-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="186a5-174">Header</span></span><br/>  | <dl> <span data-ttu-id="186a5-175"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="186a5-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="186a5-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="186a5-176">Library</span></span><br/> | <dl> <span data-ttu-id="186a5-177"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="186a5-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
