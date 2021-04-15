---
description: En este tema se describe cómo implementar una transformación de Media Foundation compatible con Direct3D (MFT) para vídeo.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad50438250c0ee1627cc20aebb49262ec8eec9ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539573"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

En este tema se describe cómo implementar una transformación de Media Foundation *compatible con Direct3D* (MFT) para vídeo.

Un MFT de vídeo se considera *compatible con Direct3D* si puede procesar ejemplos que contienen superficies de Direct3D. La razón típica para admitir Direct3D en un MFT de vídeo es habilitar la descodificación acelerada por hardware mediante la aceleración de vídeo de DirectX (DXVA).

En este tema se describen los pasos necesarios para que la MFT sea compatible con Direct3D. En este tema no se trata la mecánica de la descodificación de DXVA. Para obtener información sobre DXVA, consulte [aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> A partir de Windows 8, se puede usar [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) en lugar de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). En el caso de las aplicaciones de la tienda Windows, debe usar **IMFDXGIDeviceManager** y Microsoft Direct3D 11. Para obtener más información, consulte las [API de vídeo de Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implemente el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Este método devuelve un puntero a un almacén de atributos.
2.  El MFT debe establecer el valor del atributo [**MF de la \_ SA \_ \_**](mf-sa-d3d-aware-attribute.md) de la definición de este en **true** en su propio almacén de atributos. A partir de Windows 8, si usa Direct3D 11, use [MF \_ SA \_ D3D11 \_ ](mf-sa-d3d11-aware.md).
3.  Durante la negociación de formato, si el atributo [**MF \_ SA \_ \_**](mf-sa-d3d-aware-attribute.md) (o [MF \_ SA \_ D3D11 \_ compatible](mf-sa-d3d11-aware.md) con el uso de Direct3D 11) es **true**, el cliente puede enviar el mensaje de [**\_ \_ \_ \_ Administrador de D3D del conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) al MFT. El parámetro de evento *ulParam* es un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . A partir de Windows 8, puede usar [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) en lugar de **IDirect3DDeviceManager9**. No es necesario que el cliente envíe este mensaje.
4.  La MFT llama a [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) para consultar el servicio DXVA que necesita. A partir de Windows 8, si se usó [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , la MFT llama a [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Normalmente, un descodificador consultaría [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)y un procesador de vídeo consultaría [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  Suponiendo que el paso anterior se realiza correctamente, los métodos [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) y [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deben devolver formatos compatibles con DXVA.
6.  El cliente configura los tipos de medios en la MFT. Si un tipo de medio no es compatible con DXVA, el MFT debe devolver el código de error **MF \_ E no \_ compatible \_ \_ tipo D3D**.
7.  En este momento, hay dos opciones, dependiendo de si el cliente encuentra un formato DXVA adecuado.
    -   Si el cliente configura correctamente un formato DXVA, puede comenzar el procesamiento. En este momento, la MFT puede usar DXVA para el procesamiento o revertir al procesamiento de software.
    -   Como alternativa, si el cliente no encuentra un formato DXVA aceptable, el cliente puede enviar otro mensaje [**de \_ \_ Administrador de \_ D3D \_ de conjunto de mensajes de MFT**](mft-message-set-d3d-manager.md) , esta vez estableciendo *ulParam* en **null**. El MFT debe liberar el puntero [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (el puntero [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , si se usó **IMFDXGIDeviceManager** ) y cualquier otra interfaz DXVA, y revertir al procesamiento de software. En este momento, el MFT no debe usar el procesamiento de DXVA.

Un MFT compatible con Direct3D debe estar preparado para controlar ejemplos que contienen una superficie de Direct3D. El ejemplo contendrá exactamente un búfer multimedia. Para obtener la superficie de Direct3D del búfer, llame a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) y especifique el servicio de **\_ \_ servicio de búfer Mr** . Para obtener más información, consulte [búfer de superficie de DirectX](directx-surface-buffer.md).

Un MFT que use DXVA debe asignar sus propios ejemplos de salida, como se indica a continuación:

1.  En el método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , establezca el **flujo de salida de MFT proporciona la marca \_ \_ \_ \_ Samples** .
2.  Cree un grupo de superficies de DXVA, tal como se describe en la especificación de DXVA.
3.  Cree ejemplos de medios mediante una llamada a [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

La MFT siempre debe admitir el procesamiento de software como reserva, ya que es posible que el procesamiento de DXVA no esté disponible por varias razones:

-   Es posible que la GPU no admita DXVA.
-   Es posible que el cliente no use Direct3D.
-   Los perfiles de DXVA no se definen para todos los formatos de vídeo.

Un MFT compatible con Direct3D debe tener un único flujo de salida. No puede tener varias salidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



