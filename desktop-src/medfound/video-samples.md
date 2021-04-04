---
description: Ejemplos de vídeo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Ejemplos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908628"
---
# <a name="video-samples"></a><span data-ttu-id="75f5a-103">Ejemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="75f5a-103">Video Samples</span></span>

<span data-ttu-id="75f5a-104">El objeto de ejemplo de vídeo es una implementación especializada de la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para su uso con el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="75f5a-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="75f5a-105">Para crear una instancia de este objeto, llame a la función [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) .</span><span class="sxs-lookup"><span data-stu-id="75f5a-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="75f5a-106">La función toma un puntero a una superficie de Direct3D y devuelve un puntero a la interfaz **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="75f5a-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="75f5a-107">Los siguientes tipos de objetos deben asignar ejemplos mediante esta función:</span><span class="sxs-lookup"><span data-stu-id="75f5a-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="75f5a-108">Presentadores de EVR personalizados.</span><span class="sxs-lookup"><span data-stu-id="75f5a-108">Custom EVR presenters.</span></span> <span data-ttu-id="75f5a-109">Un presentador asigna muestras de vídeo y las envía al método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador.</span><span class="sxs-lookup"><span data-stu-id="75f5a-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="75f5a-110">Para obtener más información, consulte [Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="75f5a-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="75f5a-111">Descodificadores de vídeo que admiten la aceleración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75f5a-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="75f5a-112">Para obtener más información, consulte [compatibilidad con DXVA 2,0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="75f5a-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="75f5a-113">El objeto de ejemplo de vídeo implementa las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="75f5a-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="75f5a-114">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="75f5a-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="75f5a-115">**IMFDesiredSample**</span><span class="sxs-lookup"><span data-stu-id="75f5a-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="75f5a-116">**IMFTrackedSample**</span><span class="sxs-lookup"><span data-stu-id="75f5a-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="75f5a-117">Si el parámetro *pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) no es **null**, el ejemplo de vídeo resultante contiene un solo búfer multimedia que encapsula la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="75f5a-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="75f5a-118">Este objeto de búfer tiene una funcionalidad limitada:</span><span class="sxs-lookup"><span data-stu-id="75f5a-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="75f5a-119">El método [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) del búfer devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="75f5a-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="75f5a-120">El búfer no implementa la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="75f5a-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="75f5a-121">La única manera de tener acceso a la superficie desde el búfer es llamar a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), mediante el servicio de búfer del identificador de servicio Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="75f5a-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="75f5a-122">Si el parámetro *pUnkSurface* es **null**, el ejemplo de vídeo se crea con cero búferes de medios.</span><span class="sxs-lookup"><span data-stu-id="75f5a-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="75f5a-123">Para agregar un búfer al ejemplo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="75f5a-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="75f5a-124">Cree una superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="75f5a-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="75f5a-125">Cree un búfer de superficie mediante una llamada a [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span><span class="sxs-lookup"><span data-stu-id="75f5a-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="75f5a-126">Para obtener más información, consulte [búfer de superficie de DirectX](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="75f5a-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="75f5a-127">Agregue el búfer al ejemplo llamando a [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="75f5a-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="75f5a-128">Use este enfoque si necesita que la memoria de la superficie sea accesible a través de la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="75f5a-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75f5a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75f5a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f5a-130">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="75f5a-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="75f5a-131">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="75f5a-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
