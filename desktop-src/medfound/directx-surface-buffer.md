---
description: Búfer de superficie de DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Búfer de superficie de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cff1489a644fd5c4144c8c0d923f11e5ca4555886e8defbce3b9b26a16a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828275"
---
# <a name="directx-surface-buffer"></a>Búfer de superficie de DirectX

El objeto de búfer de superficie de DirectX es un búfer multimedia que administra una superficie de Direct3D. Para crear una instancia de este objeto, llame a [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) y pase un puntero a la superficie de DirectX. El búfer de superficie de DirectX expone las interfaces siguientes:

-   [**BUFFERMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Hay varias maneras de acceder a la memoria de la superficie desde el objeto de búfer:

-   Recomendado: llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el búfer. Use el identificador de servicio **MR \_ BUFFER \_ SERVICE**. El método devuelve un puntero a la superficie subyacente de Direct3D.
-   Llame [**a IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Este método llama **a IDirect3DSurface9::LockRect** directamente en la superficie. El [**método IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) llama a **UnlockRect** en la superficie.
-   Llame [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Por lo general, esto no se recomienda, ya que obliga al objeto a copiar memoria de la superficie de Direct3D y, a continuación, a volver a hacerlo. El [**método Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) es más eficaz.

Tanto [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) como [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) pueden producir un error si la superficie subyacente no se puede bloquear. El búfer de superficie de DirectX implementa estos dos métodos principalmente para los componentes que no están diseñados para funcionar con superficies de Direct3D.

El representador de vídeo mejorado (EVR) crea búferes de superficie de DirectX cuando el descodificador no está configurado para la aceleración de vídeo de DirectX (DXVA). Para obtener más información, [**vea IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Obtención de la superficie de Direct3D

Para obtener una superficie de Direct3D a partir de un ejemplo de vídeo, haga lo siguiente:

1.  Llame [**a IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valor de índice de cero.
2.  Llame [**a MFGetService y**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) especifique el identificador del servicio MR **\_ BUFFER \_** SERVICE.

El siguiente código muestra estos pasos:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes multimedia](media-buffers.md)
</dt> <dt>

[Ejemplos de vídeo](video-samples.md)
</dt> </dl>

 

 



