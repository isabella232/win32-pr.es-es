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
# <a name="directx-surface-buffer"></a>Búfer de superficie de DirectX

El objeto de búfer de superficie de DirectX es un búfer multimedia que administra una superficie de Direct3D. Para crear una instancia de este objeto, llame a [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) y pase un puntero a la superficie de DirectX. El búfer de superficie de DirectX expone las siguientes interfaces:

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Hay varias maneras de tener acceso a la memoria de la superficie desde el objeto de búfer:

-   Recomendado: llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el búfer. Use el **\_ \_ servicio de búfer** del identificador de servicio Mr. El método devuelve un puntero a la superficie de Direct3D subyacente.
-   Llame a [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Este método llama a **IDirect3DSurface9:: LockRect** directamente en la superficie. El método [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) llama a **UnlockRect** en la superficie.
-   Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Por lo general, esto no es recomendable, ya que obliga al objeto a copiar la memoria de la superficie de Direct3D y volver a hacerla de nuevo. El método [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) es más eficaz.

Se puede producir un error en [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) y [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) si la superficie subyacente no es bloqueable. El búfer de superficie de DirectX implementa estos dos métodos principalmente para los componentes que no están diseñados para funcionar con superficies de Direct3D.

El representador de vídeo mejorado (EVR) crea búferes de superficie de DirectX cuando el descodificador no está configurado para la aceleración de vídeo de DirectX (DXVA). Para obtener más información, vea [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Obtención de la superficie de Direct3D

Para obtener una superficie de Direct3D de un ejemplo de vídeo, haga lo siguiente:

1.  Llame a [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valor de índice de cero.
2.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especifique el identificador de servicio del **\_ \_ servicio de búfer Mr** .

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

 

 



