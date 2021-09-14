---
description: Ejemplos de vídeo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Ejemplos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363622"
---
# <a name="video-samples"></a>Ejemplos de vídeo

El objeto de ejemplo de vídeo es una implementación especializada de la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para su uso con [el representador de](enhanced-video-renderer.md) vídeo mejorado (EVR). Para crear una instancia de este objeto, llame a [**la función MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) La función toma un puntero a una superficie de Direct3D y devuelve un puntero a la **interfaz IMFSample.** Los siguientes tipos de objetos deben asignar ejemplos mediante esta función:

-   Presentadores evr personalizados. Un presentador asigna ejemplos de vídeo y los envía al método [**MIXERTransform::P rocessOutput del**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) mezclador. Para obtener más información, [vea How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).

-   Descodificadores de vídeo que admiten la aceleración de vídeo. Para obtener más información, [vea Compatibilidad con DXVA 2.0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

El objeto de ejemplo de vídeo implementa las interfaces siguientes:

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Si el *parámetro pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) no es **NULL,** el ejemplo de vídeo resultante contiene un único búfer multimedia que encapsula la superficie de Direct3D. Este objeto de búfer tiene funcionalidad limitada:

-   El método [**IMFMediaBuffer::Lock del**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) búfer devuelve E \_ NOTIMPL.

-   El búfer no implementa la [**interfaz IMF2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

La única manera de acceder a la superficie desde el búfer es llamar a [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)mediante el identificador de servicio MR \_ BUFFER \_ SERVICE.

Si el *parámetro pUnkSurface* es **NULL,** el ejemplo de vídeo se crea con cero búferes multimedia. Para agregar un búfer al ejemplo, haga lo siguiente:

1.  Cree una superficie de Direct3D.

2.  Cree un búfer de superficie mediante una llamada [**a MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Para obtener más información, vea [Búfer de superficie de DirectX.](directx-surface-buffer.md)

3.  Agregue el búfer al ejemplo mediante una llamada [**a IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Use este enfoque si necesita que la memoria de superficie sea accesible a través de la [**interfaz DEO2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de medios](media-buffers.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> </dl>

 

 
