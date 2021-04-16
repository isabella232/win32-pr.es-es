---
description: La interfaz IMediaDet recupera información sobre un archivo multimedia, como el número de flujos y el tipo de medio, la duración y la velocidad de fotogramas de cada flujo.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaz IMediaDet (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679071"
---
# <a name="imediadet-interface"></a><span data-ttu-id="6106a-103">Interfaz IMediaDet</span><span class="sxs-lookup"><span data-stu-id="6106a-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="6106a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6106a-104">\[Deprecated.</span></span> <span data-ttu-id="6106a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6106a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6106a-106">La `IMediaDet` interfaz recupera información sobre un archivo multimedia, como el número de flujos y el tipo de medio, la duración y la velocidad de fotogramas de cada flujo.</span><span class="sxs-lookup"><span data-stu-id="6106a-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="6106a-107">También contiene métodos para recuperar fotogramas individuales de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6106a-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="6106a-108">El objeto de [detección de medios (MediaDet)](media-detector--mediadet.md) expone esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6106a-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="6106a-109">Para obtener información acerca de un archivo mediante esta interfaz, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6106a-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="6106a-110">Cree una instancia del objeto MediaDet llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="6106a-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="6106a-111">El identificador de clase es CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="6106a-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="6106a-112">Llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT para especificar el nombre del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6106a-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="6106a-113">Llame a [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de flujos de salida en el origen.</span><span class="sxs-lookup"><span data-stu-id="6106a-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="6106a-114">Llame a [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) para especificar una secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="6106a-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="6106a-115">Llame a cualquiera de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6106a-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="6106a-116">**IMediaDet:: get \_ velocidad de fotogramas**</span><span class="sxs-lookup"><span data-stu-id="6106a-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="6106a-117">**IMediaDet:: get \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="6106a-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="6106a-118">**IMediaDet:: get \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="6106a-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="6106a-119">**IMediaDet:: get \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="6106a-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="6106a-120">Para recuperar un fotograma de vídeo, llame a [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md).</span><span class="sxs-lookup"><span data-stu-id="6106a-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="6106a-121">El marco devuelto siempre tiene el formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="6106a-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="6106a-122">No use el mismo objeto MediaDet con varios archivos.</span><span class="sxs-lookup"><span data-stu-id="6106a-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="6106a-123">Para obtener información o fotogramas de vídeo de más de un archivo, use instancias de MediaDet independientes.</span><span class="sxs-lookup"><span data-stu-id="6106a-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="6106a-124">La interfaz **IMediaDet** no admite formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , por lo que no puede usar esta interfaz para obtener campos entrelazados o información sobre el entrelazado.</span><span class="sxs-lookup"><span data-stu-id="6106a-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="6106a-125">Además, si el descodificador de nivel superior solo admite **VIDEOINFOHEADER2**, no puede usar `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="6106a-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="6106a-126">Este es el caso de un descodificador MPEG-2, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6106a-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="6106a-127">Además, la `IMediaDet` interfaz omite cualquier flujo del archivo que no sea de vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="6106a-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="6106a-128">Por ejemplo, si el archivo contiene una secuencia de audio, un flujo de datos y una secuencia de vídeo, el método **Get \_ OutputStreams** informará solo de dos flujos (audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="6106a-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="6106a-129">Miembros</span><span class="sxs-lookup"><span data-stu-id="6106a-129">Members</span></span>

<span data-ttu-id="6106a-130">La interfaz **IMediaDet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6106a-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6106a-131">**IMediaDet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6106a-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="6106a-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="6106a-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6106a-133">Métodos</span><span class="sxs-lookup"><span data-stu-id="6106a-133">Methods</span></span>

<span data-ttu-id="6106a-134">La interfaz **IMediaDet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6106a-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="6106a-135">Método</span><span class="sxs-lookup"><span data-stu-id="6106a-135">Method</span></span>                                                        | <span data-ttu-id="6106a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="6106a-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6106a-137">**EnterBitmapGrabMode**</span><span class="sxs-lookup"><span data-stu-id="6106a-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="6106a-138">Cambia el detector de medios al modo de agarre de mapa de bits y busca el gráfico de filtro en un tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="6106a-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="6106a-139">**obtener \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="6106a-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="6106a-140">Recupera el número de secuencia utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="6106a-141">**obtener \_ nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="6106a-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="6106a-142">Recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="6106a-143">**obtener \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="6106a-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="6106a-144">Recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="6106a-145">**obtener \_ velocidad de fotogramas**</span><span class="sxs-lookup"><span data-stu-id="6106a-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="6106a-146">Recupera la velocidad de fotogramas de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6106a-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="6106a-147">**obtener \_ OutputStreams**</span><span class="sxs-lookup"><span data-stu-id="6106a-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="6106a-148">Recupera el número de secuencias de audio y vídeo contenidas en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="6106a-149">**obtener \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="6106a-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="6106a-150">Recupera la duración de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6106a-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="6106a-151">**obtener \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="6106a-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="6106a-152">Recupera el tipo de medio de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6106a-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="6106a-153">**obtener \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="6106a-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="6106a-154">Recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6106a-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="6106a-155">**obtener \_ StreamTypeB**</span><span class="sxs-lookup"><span data-stu-id="6106a-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="6106a-156">Recupera una cadena que representa el GUID del tipo de medio para la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6106a-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="6106a-157">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="6106a-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="6106a-158">Recupera un fotograma de vídeo en el tiempo medio especificado.</span><span class="sxs-lookup"><span data-stu-id="6106a-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="6106a-159">**GetSampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="6106a-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="6106a-160">Recupera un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="6106a-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="6106a-161">**Put \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="6106a-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="6106a-162">Especifica el número de secuencia que va a usar el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="6106a-163">**Put \_ FILENAME**</span><span class="sxs-lookup"><span data-stu-id="6106a-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="6106a-164">Especifica el nombre del archivo de origen para el detector de medios que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6106a-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="6106a-165">**colocar \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="6106a-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="6106a-166">Especifica un filtro de origen para que lo use el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="6106a-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="6106a-167">**WriteBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="6106a-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="6106a-168">Recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="6106a-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6106a-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6106a-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6106a-170">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="6106a-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6106a-171">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6106a-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6106a-172">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6106a-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6106a-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6106a-173">Requirements</span></span>



| <span data-ttu-id="6106a-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="6106a-174">Requirement</span></span> | <span data-ttu-id="6106a-175">Value</span><span class="sxs-lookup"><span data-stu-id="6106a-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6106a-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6106a-176">Header</span></span><br/>  | <dl> <span data-ttu-id="6106a-177"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6106a-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6106a-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6106a-178">Library</span></span><br/> | <dl> <span data-ttu-id="6106a-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6106a-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
