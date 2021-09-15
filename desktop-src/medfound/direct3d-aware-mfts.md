---
description: En este tema se describe cómo implementar una transformación de Media Foundation con direct3D (MFT) para vídeo.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad50438250c0ee1627cc20aebb49262ec8eec9ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574936"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MTA

En este tema se describe cómo implementar una transformación de Media Foundation con *direct3D* (MFT) para vídeo.

Un MFT de vídeo se considera que tiene en cuenta *Direct3D* si puede procesar muestras que contienen superficies de Direct3D. La razón típica para admitir Direct3D en un MFT de vídeo es habilitar lacodización acelerada por hardware mediante la aceleración de vídeo de DirectX (DXVA).

En este tema se describen los pasos necesarios para que MFT Direct3D sea consciente. En este tema no se trata la mecánica de la decodificación de DXVA. Para obtener información sobre DXVA, vea [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> A partir Windows 8, se puede usar [**IMFDXGIDeviceManager en**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) lugar de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). Para Windows store, debe usar **IMFDXGIDeviceManager** y Microsoft Direct3D 11. Para obtener más información, vea Las API de vídeo de [Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implemente [**el método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Este método devuelve un puntero a un almacén de atributos.
2.  El MFT debe establecer el valor del atributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) en **TRUE** en su propio almacén de atributos. A partir Windows 8, si usa Direct3D 11, use [MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md).
3.  Durante la negociación de formato, si el atributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) (o [MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) si se usa Direct3D 11) es **TRUE,** el cliente puede enviar el mensaje [**MFT MESSAGE SET \_ \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) al MFT. El *parámetro de evento ulParam* es un puntero a la interfaz [**IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) A partir Windows 8, puede usar [**IMFDXGIDeviceManager en**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) lugar de **IDirect3DDeviceManager9**. No es necesario que el cliente envíe este mensaje.
4.  MFT llama a [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) para consultar el servicio DXVA que necesita. A partir Windows 8, si se usó [**IMFDXGIDeviceManager,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) MFT llama a [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Normalmente, un descodificador [**consultaba IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)y un procesador de vídeo consultaba [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  Suponiendo que el paso anterior es correcto, los métodos [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) y [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deben devolver formatos compatibles con DXVA.
6.  El cliente configura los tipos de medios en MFT. Si un tipo de medio no es compatible con DXVA, MFT debe devolver el código de error **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE**.
7.  En este punto, hay dos opciones, en función de si el cliente encuentra un formato DXVA adecuado.
    -   Si el cliente configura correctamente un formato DXVA, puede empezar a procesarse. En este momento, MFT puede usar DXVA para el procesamiento o resalte al procesamiento de software.
    -   Como alternativa, si el cliente no encuentra un formato DXVA aceptable, el cliente puede enviar otro mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER,**](mft-message-set-d3d-manager.md) esta vez estableciendo *ulParam* en **NULL.** El MFT debe liberar el puntero [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (el puntero [**IMFDXGIDeviceManager,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) si se usó **IMFDXGIDeviceManager)** y cualquier otra interfaz DXVA, y revertir al procesamiento de software. En este momento, MFT no debe usar el procesamiento dxva.

Un MFT que tenga en cuenta Direct3D debe estar preparado para controlar muestras que contengan una superficie de Direct3D. El ejemplo contendrá exactamente un búfer multimedia. Para obtener la superficie de Direct3D del búfer, llame a la [**función MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especifique el **servicio MR BUFFER \_ \_ SERVICE.** Para obtener más información, vea [Búfer de superficie de DirectX.](directx-surface-buffer.md)

Un MFT que use DXVA debe asignar sus propios ejemplos de salida, como se muestra a continuación:

1.  En el [**método IMFTransform::GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) establezca la marca **MFT \_ OUTPUT STREAM \_ \_ PROVIDES \_ SAMPLES.**
2.  Cree un grupo de superficies DXVA, como se describe en la especificación de DXVA.
3.  Cree ejemplos de medios mediante una llamada [**a MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

El MFT siempre debe admitir el procesamiento de software como reserva, ya que es posible que el procesamiento de DXVA no esté disponible por varias razones:

-   Es posible que la GPU no admita DXVA.
-   Es posible que el cliente no use Direct3D.
-   Los perfiles dxva no se definen para cada formato de vídeo.

Un MFT que tenga en cuenta Direct3D debe tener un único flujo de salida. No puede tener varias salidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



