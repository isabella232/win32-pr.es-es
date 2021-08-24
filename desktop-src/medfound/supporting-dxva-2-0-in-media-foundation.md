---
description: Compatibilidad con DXVA 2.0 en Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Compatibilidad con DXVA 2.0 en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721935"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Compatibilidad con DXVA 2.0 en Media Foundation

En este tema se describe cómo admitir DirectX Video Acceleration (DXVA) 2.0 en una transformación de Media Foundation (MFT) mediante Microsoft Direct3D 9 Específicamente, se describe la comunicación entre el descodificador y el representador de vídeo, que está mediado por el cargador de topologías. En este tema no se describe cómo implementar la decodificación de DXVA.

En el resto de este  tema, el término descodificador hace referencia al descodificador MFT, que recibe vídeo comprimido y genera vídeo sin comprimir. El término *dispositivo descodificador* hace referencia a un acelerador de vídeo de hardware implementado por el controlador de gráficos.

> [!TIP]
> Para obtener información sobre lacoding de vídeo de Microsoft Direct3D 11, vea Compatibilidad con lacoding de vídeo de [Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Windows Las aplicaciones de la Tienda deben usar Direct3D 11.

 

Estos son los pasos básicos que debe realizar un descodificador para admitir DXVA 2.0 en Media Foundation:

1.  Abra un identificador para el dispositivo Direct3D 9.
2.  Busque una configuración de descodificador DXVA.
3.  Asignar búferes sin comprimir.
4.  Descodificar fotogramas.

Estos pasos se describen con más detalle en el resto de este tema.

## <a name="opening-a-direct3d-device-handle"></a>Apertura de un identificador de dispositivo Direct3D

MFT usa el administrador de dispositivos De Microsoft Direct3D para obtener un identificador para el dispositivo Direct3D 9. Para abrir el identificador del dispositivo, realice los pasos siguientes:

1.  Exponga [el atributo MF SA \_ \_ D3D \_ AWARE](mf-sa-d3d-aware-attribute.md) con el valor **TRUE**. El cargador de topología consulta este atributo mediante una llamada [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Al establecer el atributo en **TRUE,** se notifica al cargador de topologías que MFT admite DXVA.
2.  Cuando se inicia la negociación de formato, el cargador de topologías llama [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el [**mensaje MFT MESSAGE SET \_ \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) El *parámetro ulParam* es un **puntero IUnknown** al administrador de dispositivos Direct3D del representador de vídeo. Consulte este puntero para la [**interfaz IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)
3.  Llame a [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo Direct3D del representador.
4.  Llame [**a IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) y pase el identificador del dispositivo. Este método devuelve un puntero a la [**interfaz IDirectXVideoDecoderService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)
5.  Almacenar en caché los punteros y el identificador del dispositivo.

## <a name="finding-a-decoder-configuration"></a>Buscar una configuración de descodificador

El MFT debe encontrar una configuración compatible para el dispositivo descodificador DXVA. Realice los pasos siguientes dentro del [**método IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) después de validar el tipo de entrada:

1.  Llame [**a IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Este método devuelve una matriz de GUID de dispositivo descodificador.
2.  Recorrer en bucle la matriz de GUID de descodificador para buscar los que admite el descodificador. Por ejemplo, para un descodificador MPEG-2, buscaría **DXVA2 \_ ModeMPEG2 \_ MOCOMP,** **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD**.

3.  Cuando encuentre un GUID de dispositivo descodificador candidato, pase el GUID al método [**IDirectXVideoDecoderService::GetDecoderRenderTargets.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Este método devuelve una matriz de formatos de destino de representación, especificados como **valores D3DFORMAT.**
4.  Recorrer en bucle los formatos de destino de representación y buscar un formato compatible con el descodificador.
5.  Llame [**a IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Pase el mismo GUID de dispositivo descodificador, junto con una [**estructura \_ DxVA2 VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que describe el formato de salida propuesto. El método devuelve una matriz de [**estructuras \_ ConfigPictureDecode de DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) Cada estructura describe una posible configuración para el dispositivo descodificador. Busque una configuración que admita el descodificador.
6.  Almacene el formato y la configuración del destino de representación.

En el [**método IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devuelva un formato de vídeo sin comprimir, en función del formato de destino de representación propuesto.

En el [**método IMFTransform::SetOutputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) compruebe el tipo de medio con el formato de destino de representación.

### <a name="fallback-to-software-decoding"></a>Reserva a lacoding de software

Si MFT no encuentra una configuración dxva (por ejemplo, si el controlador de gráficos no tiene las funcionalidades correctas), debe devolver el código de error **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE** de los métodos [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) y [**SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) El cargador de topologías responderá enviando el mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) con el valor **NULL** para el *parámetro ulParam.* MFT debe liberar su puntero a la [**interfaz IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) A continuación, el cargador de topologías volverá a negociar el tipo de medio y MFT puede usar la decodificación de software.

## <a name="allocating-uncompressed-buffers"></a>Asignación de búferes sin comprimir

En DXVA 2.0, el descodificador es responsable de asignar superficies de Direct3D para usarlas como búferes de vídeo sin comprimir. El descodificador debe asignar 3 superficies para que la EVR la use para desenlazar. Este número es fijo, porque Media Foundation no proporciona una manera de que la EVR especifique cuántas superficies requiere el controlador de gráficos para desenlazar. Tres superficies deben ser suficientes para cualquier controlador.

En el [**método IMFTransform::GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) establezca la marca **MFT \_ OUTPUT STREAM \_ PROVIDES \_ \_ SAMPLES** en la estructura [**\_ MFT OUTPUT STREAM \_ \_ INFO.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Esta marca notifica a la sesión multimedia que MFT asigna sus propios ejemplos de salida.

Para crear las superficies, llame a [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (La [**interfaz IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hereda este método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)). Puede hacerlo en [**SetInputType después**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)de buscar el formato de destino de representación.

Para cada superficie, llame a [**MFCreateVideoSampleFromSurface para**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) crear un ejemplo multimedia para contener la superficie. El método devuelve un puntero a la [**interfaz IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="decoding"></a>Descodificación

Para crear el dispositivo descodificador, llame a [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). El método devuelve un puntero a la [**interfaz IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo descodificador.

Lacoding debe producirse dentro del [**método DETRANSFORMTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) En cada fotograma, llame a [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para probar el identificador del dispositivo. Si el dispositivo ha cambiado, el método devuelve **DXVA2 \_ E NEW VIDEO \_ \_ \_ DEVICE**. Si esto ocurre, haga lo siguiente:

1.  Cierre el identificador del dispositivo mediante una [**llamada a IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere los [**punteros IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) [**e IDirectXVideoDecoder.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)
3.  Abra un nuevo identificador de dispositivo.
4.  Negociar una nueva configuración de descodificador, como se describe en "Búsqueda de una configuración de descodificador" anteriormente en esta página.
5.  Cree un nuevo dispositivo descodificador.

Suponiendo que el identificador del dispositivo es válido, el proceso de descodización funciona de la siguiente manera:

1.  Obtenga una superficie disponible que no esté actualmente en uso. (Inicialmente todas las superficies están disponibles).
2.  Consulte el ejemplo de medios para la [**interfaz IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Llame [**a IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) y proporcione un puntero a la interfaz [**IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementada por el descodificador. Cuando el representador de vídeo libera el ejemplo, se invoca la devolución de llamada del descodificador.
4.  Llame [**a IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Haga lo siguiente una o varias veces:
    1.  Llame [**a IDirectXVideoDecoder::GetBuffer para**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) obtener un búfer de descodificador DXVA.
    2.  Rellene el búfer.
    3.  Llame [**a IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Llame [**a IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para realizar las operaciones de descodificación en el marco.

DXVA 2.0 usa las mismas estructuras de datos que DXVA 1.0 para las operaciones de decodificación. Para el conjunto original de perfiles DXVA (para H.261, H.263 y MPEG-2), estas estructuras de datos se describen en la especificación [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de [**llamadas a BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)Execute, puede llamar a GetBuffer varias veces, pero solo una vez para / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) cada tipo de búfer DXVA. [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) Si lo llama dos veces con el mismo tipo de búfer, sobrescribirá los datos.

Use la devolución de llamada del [**método SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (paso 3) para realizar un seguimiento de qué muestras están disponibles actualmente y cuáles están en uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 
