---
description: Búfer de superficie de DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Búfer de superficie de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153639"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="af0cc-103">Búfer de superficie de DirectX</span><span class="sxs-lookup"><span data-stu-id="af0cc-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="af0cc-104">El objeto de búfer de superficie de DirectX es un búfer multimedia que administra una superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="af0cc-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="af0cc-105">Para crear una instancia de este objeto, llame a [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) y pase un puntero a la superficie de DirectX.</span><span class="sxs-lookup"><span data-stu-id="af0cc-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="af0cc-106">El búfer de superficie de DirectX expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="af0cc-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="af0cc-107">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="af0cc-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="af0cc-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="af0cc-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="af0cc-109">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="af0cc-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="af0cc-110">Hay varias maneras de tener acceso a la memoria de la superficie desde el objeto de búfer:</span><span class="sxs-lookup"><span data-stu-id="af0cc-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="af0cc-111">Recomendado: llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el búfer.</span><span class="sxs-lookup"><span data-stu-id="af0cc-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="af0cc-112">Use el **\_ \_ servicio de búfer** del identificador de servicio Mr.</span><span class="sxs-lookup"><span data-stu-id="af0cc-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="af0cc-113">El método devuelve un puntero a la superficie de Direct3D subyacente.</span><span class="sxs-lookup"><span data-stu-id="af0cc-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="af0cc-114">Llame a [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span><span class="sxs-lookup"><span data-stu-id="af0cc-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="af0cc-115">Este método llama a **IDirect3DSurface9:: LockRect** directamente en la superficie.</span><span class="sxs-lookup"><span data-stu-id="af0cc-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="af0cc-116">El método [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) llama a **UnlockRect** en la superficie.</span><span class="sxs-lookup"><span data-stu-id="af0cc-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="af0cc-117">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="af0cc-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="af0cc-118">Por lo general, esto no es recomendable, ya que obliga al objeto a copiar la memoria de la superficie de Direct3D y volver a hacerla de nuevo.</span><span class="sxs-lookup"><span data-stu-id="af0cc-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="af0cc-119">El método [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="af0cc-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="af0cc-120">Se puede producir un error en [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) y [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) si la superficie subyacente no es bloqueable.</span><span class="sxs-lookup"><span data-stu-id="af0cc-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="af0cc-121">El búfer de superficie de DirectX implementa estos dos métodos principalmente para los componentes que no están diseñados para funcionar con superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="af0cc-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="af0cc-122">El representador de vídeo mejorado (EVR) crea búferes de superficie de DirectX cuando el descodificador no está configurado para la aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="af0cc-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="af0cc-123">Para obtener más información, vea [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="af0cc-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="af0cc-124">Obtención de la superficie de Direct3D</span><span class="sxs-lookup"><span data-stu-id="af0cc-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="af0cc-125">Para obtener una superficie de Direct3D de un ejemplo de vídeo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="af0cc-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="af0cc-126">Llame a [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valor de índice de cero.</span><span class="sxs-lookup"><span data-stu-id="af0cc-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="af0cc-127">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especifique el identificador de servicio del **\_ \_ servicio de búfer Mr** .</span><span class="sxs-lookup"><span data-stu-id="af0cc-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="af0cc-128">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="af0cc-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="af0cc-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af0cc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af0cc-130">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="af0cc-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="af0cc-131">Ejemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="af0cc-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



