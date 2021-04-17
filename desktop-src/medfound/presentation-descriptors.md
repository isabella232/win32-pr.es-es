---
description: Descriptores de presentación
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descriptores de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677556"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="8cff9-103">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="8cff9-103">Presentation Descriptors</span></span>

<span data-ttu-id="8cff9-104">Una *presentación* es un conjunto de flujos multimedia relacionados que comparten un tiempo de presentación común.</span><span class="sxs-lookup"><span data-stu-id="8cff9-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="8cff9-105">Por ejemplo, una presentación puede constar de secuencias de audio y vídeo de una película.</span><span class="sxs-lookup"><span data-stu-id="8cff9-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="8cff9-106">Un *descriptor de presentación* es un objeto que contiene la descripción de una presentación determinada.</span><span class="sxs-lookup"><span data-stu-id="8cff9-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="8cff9-107">Los descriptores de presentación se usan para configurar orígenes de medios y algunos receptores de medios.</span><span class="sxs-lookup"><span data-stu-id="8cff9-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="8cff9-108">Cada descriptor de presentación contiene una lista de uno o más descriptores de *flujo*.</span><span class="sxs-lookup"><span data-stu-id="8cff9-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="8cff9-109">Describen las secuencias de la presentación.</span><span class="sxs-lookup"><span data-stu-id="8cff9-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="8cff9-110">Los flujos pueden estar seleccionados o desactivados.</span><span class="sxs-lookup"><span data-stu-id="8cff9-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="8cff9-111">Solo las secuencias seleccionadas generan datos.</span><span class="sxs-lookup"><span data-stu-id="8cff9-111">Only the selected streams produce data.</span></span> <span data-ttu-id="8cff9-112">Los flujos desseleccionados no están activos y no generan ningún dato.</span><span class="sxs-lookup"><span data-stu-id="8cff9-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="8cff9-113">Cada descriptor de flujo tiene un *controlador de tipo de medio*, que se usa para cambiar el tipo de archivo multimedia de la secuencia u obtener el tipo de medio actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="8cff9-114">(Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md)).</span><span class="sxs-lookup"><span data-stu-id="8cff9-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="8cff9-115">En la tabla siguiente se muestran las interfaces principales que expone cada uno de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="8cff9-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="8cff9-116">Object</span><span class="sxs-lookup"><span data-stu-id="8cff9-116">Object</span></span>                  | <span data-ttu-id="8cff9-117">Interfaz</span><span class="sxs-lookup"><span data-stu-id="8cff9-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8cff9-118">Descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="8cff9-118">Presentation descriptor</span></span> | [<span data-ttu-id="8cff9-119">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8cff9-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="8cff9-120">Descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="8cff9-120">Stream descriptor</span></span>       | [<span data-ttu-id="8cff9-121">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8cff9-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="8cff9-122">Controlador de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="8cff9-122">Media type handler</span></span>      | [<span data-ttu-id="8cff9-123">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="8cff9-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="8cff9-124">Presentaciones de origen de medios</span><span class="sxs-lookup"><span data-stu-id="8cff9-124">Media Source Presentations</span></span>

<span data-ttu-id="8cff9-125">Cada origen multimedia proporciona un descriptor de presentación que describe la configuración predeterminada del origen.</span><span class="sxs-lookup"><span data-stu-id="8cff9-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="8cff9-126">En la configuración predeterminada, al menos una secuencia está seleccionada y cada flujo seleccionado tiene un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="8cff9-127">Para obtener el descriptor de presentación, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="8cff9-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="8cff9-128">El método devuelve un puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="8cff9-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="8cff9-129">Puede modificar el descriptor de presentación del origen para seleccionar un conjunto diferente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8cff9-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="8cff9-130">No modifique el descriptor de presentación a menos que se detenga el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="8cff9-131">Los cambios se aplican al llamar a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) para iniciar el origen.</span><span class="sxs-lookup"><span data-stu-id="8cff9-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="8cff9-132">Para obtener el número de secuencias, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="8cff9-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="8cff9-133">Para obtener el descriptor de flujo de una secuencia, llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) y pase el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="8cff9-134">Los flujos se indizan desde cero.</span><span class="sxs-lookup"><span data-stu-id="8cff9-134">Streams are indexed from zero.</span></span> <span data-ttu-id="8cff9-135">El método **GetStreamDescriptorByIndex** devuelve un puntero [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="8cff9-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="8cff9-136">También devuelve una marca booleana que indica si la secuencia está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8cff9-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="8cff9-137">Si la secuencia está seleccionada, el origen multimedia genera datos para esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="8cff9-138">De lo contrario, el origen no genera ningún dato para ese flujo.</span><span class="sxs-lookup"><span data-stu-id="8cff9-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="8cff9-139">Para seleccionar una secuencia, llame a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) con el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="8cff9-140">Para anular la selección de un flujo, llame a [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="8cff9-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="8cff9-141">En el código siguiente se muestra cómo obtener el descriptor de la presentación de un origen multimedia y enumerar las secuencias.</span><span class="sxs-lookup"><span data-stu-id="8cff9-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="8cff9-142">Controladores de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="8cff9-142">Media Type Handlers</span></span>

<span data-ttu-id="8cff9-143">Para cambiar el tipo de archivo multimedia de la secuencia o para obtener el tipo de medio actual de la secuencia, use el controlador de tipo de medio del descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="8cff9-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="8cff9-144">Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obtener el controlador de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="8cff9-145">Este método devuelve un puntero [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="8cff9-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="8cff9-146">Si simplemente desea saber qué tipo de datos hay en la secuencia, como audio o vídeo, llame a [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="8cff9-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="8cff9-147">Este método devuelve el GUID para el tipo de medio principal.</span><span class="sxs-lookup"><span data-stu-id="8cff9-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="8cff9-148">Por ejemplo, una aplicación de reproducción normalmente conecta una secuencia de audio al procesador de audio y una secuencia de vídeo al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cff9-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="8cff9-149">Si usa la sesión multimedia o el cargador de topología para compilar una topología, el GUID de tipo principal puede ser la única información de formato que necesite.</span><span class="sxs-lookup"><span data-stu-id="8cff9-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="8cff9-150">Si su aplicación necesita información más detallada sobre el formato actual, llame a [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="8cff9-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="8cff9-151">Este método devuelve un puntero a la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="8cff9-152">Use esta interfaz para obtener los detalles del formato.</span><span class="sxs-lookup"><span data-stu-id="8cff9-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="8cff9-153">El controlador de tipo de medio también contiene una lista de los tipos de medios admitidos para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="8cff9-154">Para obtener el tamaño de la lista, llame a [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="8cff9-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="8cff9-155">Para obtener un tipo de medio de la lista, llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) con el índice del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="8cff9-156">Los tipos de medios se devuelven en el orden de preferencia aproximado.</span><span class="sxs-lookup"><span data-stu-id="8cff9-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="8cff9-157">Por ejemplo, en el caso de los formatos de audio, se prefieren velocidades de ejemplo más altas que las de menor.</span><span class="sxs-lookup"><span data-stu-id="8cff9-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="8cff9-158">Sin embargo, no hay ninguna regla definitiva que rija la ordenación, por lo que debe tratarla simplemente como una directriz.</span><span class="sxs-lookup"><span data-stu-id="8cff9-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="8cff9-159">Es posible que la lista de tipos admitidos no contenga todos los tipos de medios posibles que admita la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cff9-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="8cff9-160">Para probar si se admite un tipo de medio determinado, llame a [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="8cff9-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="8cff9-161">Para establecer el tipo de medio, llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="8cff9-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="8cff9-162">Si el método se ejecuta correctamente, el flujo contendrá datos que se ajustan al formato especificado.</span><span class="sxs-lookup"><span data-stu-id="8cff9-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="8cff9-163">El método **SetCurrentMediaType** no cambia la lista de tipos preferidos.</span><span class="sxs-lookup"><span data-stu-id="8cff9-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="8cff9-164">En el código siguiente se muestra cómo obtener el controlador de tipo de medio, enumerar los tipos de medios preferidos y establecer el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="8cff9-165">En este ejemplo se da por supuesto que la aplicación tiene algún algoritmo, que no se muestra aquí, para seleccionar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8cff9-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="8cff9-166">El específico dependerá en gran medida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cff9-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="8cff9-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cff9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cff9-168">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="8cff9-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="8cff9-169">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="8cff9-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



