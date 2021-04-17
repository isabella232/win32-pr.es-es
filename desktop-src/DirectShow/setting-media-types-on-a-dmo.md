---
description: Establecimiento de tipos de medios en DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Establecimiento de tipos de medios en DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689665"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="153fe-103">Establecimiento de tipos de medios en DMO</span><span class="sxs-lookup"><span data-stu-id="153fe-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="153fe-104">Antes de que un DMO pueda procesar los datos, el cliente debe establecer el tipo de medio para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="153fe-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="153fe-105">(Hay una excepción secundaria a esta regla; consulte [secuencias opcionales](optional-streams.md)). Para encontrar el número de flujos, llame al método [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :</span><span class="sxs-lookup"><span data-stu-id="153fe-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="153fe-106">Este método devuelve dos valores, el número de entradas y el número de salidas.</span><span class="sxs-lookup"><span data-stu-id="153fe-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="153fe-107">Estos valores son fijos para la duración de DMO.</span><span class="sxs-lookup"><span data-stu-id="153fe-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="153fe-108">**Tipos preferidos**</span><span class="sxs-lookup"><span data-stu-id="153fe-108">**Preferred Types**</span></span>

<span data-ttu-id="153fe-109">Para cada flujo, DMO asigna una lista de posibles tipos de medios, en orden de preferencia.</span><span class="sxs-lookup"><span data-stu-id="153fe-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="153fe-110">Por ejemplo, los tipos preferidos podrían ser 32-RGB, RGB de 24 bits y RGB de 16 bits, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="153fe-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="153fe-111">Cuando el cliente establece los tipos de medios, puede usar estas listas como una sugerencia.</span><span class="sxs-lookup"><span data-stu-id="153fe-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="153fe-112">Para recuperar un tipo preferido para un flujo, llame al método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="153fe-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="153fe-113">Especifique el número de secuencia y un valor de índice para el tipo (empezando desde cero).</span><span class="sxs-lookup"><span data-stu-id="153fe-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="153fe-114">Por ejemplo, el código siguiente recupera el primer tipo preferido del primer flujo de entrada:</span><span class="sxs-lookup"><span data-stu-id="153fe-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="153fe-115">Para enumerar todos los tipos de medios preferidos en un flujo determinado, use un bucle que incremente el índice de tipo hasta que el método devuelva DMO \_ E \_ ningún \_ \_ elemento más, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="153fe-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="153fe-116">Debe tener en cuenta los siguientes puntos acerca de los tipos preferidos:</span><span class="sxs-lookup"><span data-stu-id="153fe-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="153fe-117">DMO podría devolver un tipo que no tiene ningún bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="153fe-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="153fe-118">Por ejemplo, un DMO podría especificar un tipo de vídeo, como RGB de 24 bits, sin proporcionar el ancho y el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="153fe-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="153fe-119">Sin embargo, al establecer el tipo, debe proporcionar un bloque de formato completo.</span><span class="sxs-lookup"><span data-stu-id="153fe-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="153fe-120">(Algunos tipos de medios, como MIDI, nunca requieren un bloque de formato, en cuyo caso no se aplica este comentario).</span><span class="sxs-lookup"><span data-stu-id="153fe-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="153fe-121">No es necesario que DMO admita cada combinación de tipos preferidos que devuelve.</span><span class="sxs-lookup"><span data-stu-id="153fe-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="153fe-122">Por ejemplo, si una DMO tiene dos flujos y cada flujo tiene cuatro tipos preferidos, hay 16 combinaciones posibles, pero no se garantiza que todos ellos sean válidos.</span><span class="sxs-lookup"><span data-stu-id="153fe-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="153fe-123">Cuando el cliente establece el tipo de medio para un flujo, DMO podría actualizar los tipos preferidos para que otras secuencias reflejen el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="153fe-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="153fe-124">Sin embargo, no es necesario hacerlo.</span><span class="sxs-lookup"><span data-stu-id="153fe-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="153fe-125">En algunos flujos, DMO podría no ofrecer ningún tipo preferido.</span><span class="sxs-lookup"><span data-stu-id="153fe-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="153fe-126">Normalmente, un DMO debe proporcionar al menos algunos tipos preferidos en algunas secuencias.</span><span class="sxs-lookup"><span data-stu-id="153fe-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="153fe-127">No es necesario que DMO ofrezca una lista completa de los tipos de medios que puede aceptar.</span><span class="sxs-lookup"><span data-stu-id="153fe-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="153fe-128">Puede haber tipos "sin anunciar" que el DMO admita pero no ofrezca como tipos preferidos.</span><span class="sxs-lookup"><span data-stu-id="153fe-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="153fe-129">En Resumen, el cliente debe tratar solo los tipos preferidos como instrucciones.</span><span class="sxs-lookup"><span data-stu-id="153fe-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="153fe-130">La única forma de saber para determinados tipos que se admiten es probarla, como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="153fe-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="153fe-131">**Establecer el tipo de medio en una secuencia**</span><span class="sxs-lookup"><span data-stu-id="153fe-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="153fe-132">Use los métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) y [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para establecer el tipo de cada flujo.</span><span class="sxs-lookup"><span data-stu-id="153fe-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="153fe-133">Debe proporcionar una estructura **de \_ \_ tipo de medio DMO** que contenga una descripción completa del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="153fe-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="153fe-134">En el ejemplo siguiente se establece el tipo de medio en el flujo de entrada 0, mediante audio PCM estéreo de 16 bits 44,1-kHz:</span><span class="sxs-lookup"><span data-stu-id="153fe-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="153fe-135">Para probar un tipo de medio sin establecerlo, llame a **SetInputType** o **SetOutputType** con la \_ marca DMO set \_ TYPEF \_ Test \_ only.</span><span class="sxs-lookup"><span data-stu-id="153fe-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="153fe-136">El método devuelve S \_ OK si el tipo es aceptable o S \_ false en caso contrario:</span><span class="sxs-lookup"><span data-stu-id="153fe-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="153fe-137">Dado que la configuración de una secuencia puede afectar a otra secuencia, puede que tenga que borrar el tipo de archivo multimedia de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="153fe-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="153fe-138">Para ello, llame a **SetInputType** o **SetOutputType** con la \_ marca DMO set \_ TYPEF \_ Clear.</span><span class="sxs-lookup"><span data-stu-id="153fe-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="153fe-139">Para un descodificador DMO, el cliente normalmente establecería el tipo de entrada primero y, a continuación, elegiría un tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="153fe-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="153fe-140">Para un codificador DMO, el cliente establecería primero el tipo de salida y, a continuación, el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="153fe-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="153fe-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="153fe-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="153fe-142">Hospedar directamente un DMO</span><span class="sxs-lookup"><span data-stu-id="153fe-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



