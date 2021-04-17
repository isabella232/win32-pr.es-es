---
description: Compatibilidad con DXVA 2,0 en Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Compatibilidad con DXVA 2,0 en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce144c24a1aeeda6281ddb423757f3e339903440
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670079"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Compatibilidad con DXVA 2,0 en Media Foundation

En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en una transformación de Media Foundation (MFT) con Microsoft Direct3D 9, en concreto, se describe la comunicación entre el descodificador y el representador de vídeo, que se corrige mediante el cargador de topología. En este tema no se describe cómo implementar la descodificación de DXVA.

En el resto de este tema, el término *descodificador* hace referencia a la MFT del descodificador, que recibe vídeo comprimido y genera vídeo sin comprimir. El término *dispositivo descodificador* hace referencia a un acelerador de vídeo de hardware implementado por el controlador de gráficos.

> [!TIP]
> Para obtener información sobre la descodificación de vídeo de Microsoft Direct3D 11, consulte [compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Las aplicaciones de la tienda Windows deben usar Direct3D 11.

 

Estos son los pasos básicos que debe realizar un descodificador para admitir DXVA 2,0 en Media Foundation:

1.  Abra un identificador para el dispositivo de Direct3D 9.
2.  Busque una configuración de descodificador de DXVA.
3.  Asignar búferes sin comprimir.
4.  Descodificar fotogramas.

Estos pasos se describen con más detalle en el resto de este tema.

## <a name="opening-a-direct3d-device-handle"></a>Apertura de un controlador de dispositivo Direct3D

MFT usa el administrador de dispositivos de Microsoft Direct3D para obtener un identificador para el dispositivo de Direct3D 9. Para abrir el identificador del dispositivo, realice los pasos siguientes:

1.  Exponga el [atributo \_ MF \_ SA \_ compatible](mf-sa-d3d-aware-attribute.md) con el valor **true**. El cargador de topología consulta este atributo mediante una llamada a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Al establecer el atributo en **true** , se notifica al cargador de topología que el MFT admite DXVA.
2.  Cuando comienza la negociación de formato, el cargador de topología llama a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de [**Administrador de D3D del conjunto de mensajes de MFT \_ \_ \_ \_**](mft-message-set-d3d-manager.md) . El parámetro *ulParam* es un puntero **IUnknown** al administrador de dispositivos de Direct3D del representador de vídeo. Consulte este puntero para la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Llame a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo Direct3D del representador.
4.  Llame a [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) y pase el identificador del dispositivo. Este método devuelve un puntero a la interfaz [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Almacene en caché los punteros y el identificador del dispositivo.

## <a name="finding-a-decoder-configuration"></a>Buscar una configuración de descodificador

La MFT debe encontrar una configuración compatible para el dispositivo descodificador de DXVA. Siga los pasos que se indican a continuación en el método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) después de validar el tipo de entrada:

1.  Llame a [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Este método devuelve una matriz de GUID de dispositivo de descodificador.
2.  Recorra en bucle la matriz de GUID del descodificador para buscar los que admite el descodificador. Por ejemplo, para un descodificador MPEG-2, buscará **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ \_** ModeMPEG2 VLD.

3.  Cuando encuentre un GUID de dispositivo descodificador candidato, pase el GUID al método [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Este método devuelve una matriz de formatos de destino de representación, especificados como valores de **D3DFORMAT** .
4.  Recorra los formatos de destino de representación y busque un formato compatible con el descodificador.
5.  Llame a [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Pase el mismo GUID del dispositivo de descodificador, junto con una estructura [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que describe el formato de salida propuesto. El método devuelve una matriz de estructuras [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Cada estructura describe una posible configuración para el dispositivo descodificador. Busque una configuración que admita el descodificador.
6.  Almacene el formato y la configuración del destino de representación.

En el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , devuelve un formato de vídeo sin comprimir, basado en el formato de destino de representación propuesto.

En el método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , compruebe el tipo de medio con el formato de destino de representación.

### <a name="fallback-to-software-decoding"></a>Retroceso a descodificación de software

Si el MFT no puede encontrar una configuración de DXVA (por ejemplo, si el controlador de gráficos no tiene las capacidades adecuadas), debe devolver el **\_ \_ \_ \_ tipo D3D no compatible con** el código de error MF e de los métodos [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) y [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . El cargador de topología responderá enviando el mensaje [**del \_ \_ \_ \_ Administrador D3D del conjunto de mensajes de MFT**](mft-message-set-d3d-manager.md) con el valor **null** para el parámetro *ulParam* . La MFT debe liberar su puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . El cargador de topología volverá a negociar el tipo de medio y el MFT podrá usar la descodificación de software.

## <a name="allocating-uncompressed-buffers"></a>Asignación de búferes sin comprimir

En DXVA 2,0, el descodificador es responsable de asignar las superficies de Direct3D que se usarán como búferes de vídeo sin comprimir. El descodificador debe asignar 3 superficies para que el EVR lo use para el desentrelazado. Este número es fijo, ya que Media Foundation no proporciona una manera para que EVR especifique cuántas superficies necesita el controlador de gráficos para el desentrelazado. Tres superficies deben ser suficientes para cualquier controlador.

En el método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , establezca el **flujo de salida de MFT proporciona la marca \_ \_ \_ \_ Samples** en la estructura de información del flujo de salida de [**MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Esta marca notifica a la sesión de medios que la MFT asigna sus propios ejemplos de salida.

Para crear las superficies, llame a [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (La interfaz [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hereda este método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)). Puede hacer esto en [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype), después de encontrar el formato de destino de representación.

Para cada superficie, llame a [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) para crear un ejemplo multimedia que contenga la superficie. El método devuelve un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="decoding"></a>Descodificación

Para crear el dispositivo descodificador, llame a [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). El método devuelve un puntero a la interfaz [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo descodificador.

La descodificación debe realizarse dentro del método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . En cada fotograma, llame a [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para probar el identificador del dispositivo. Si el dispositivo ha cambiado, el método devuelve **DXVA2 \_ E \_ nuevo \_ \_ dispositivo de vídeo**. Si esto ocurre, haga lo siguiente:

1.  Cierre el identificador del dispositivo mediante una llamada a [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere los punteros [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) y [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Abra un nuevo identificador de dispositivo.
4.  Negocie una nueva configuración del descodificador, tal como se describe en "buscar una configuración de descodificador" anteriormente en esta página.
5.  Cree un nuevo dispositivo descodificador.

Suponiendo que el identificador del dispositivo es válido, el proceso de descodificación funciona de la siguiente manera:

1.  Obtiene una superficie disponible que no está actualmente en uso. (Inicialmente, todas las superficies están disponibles).
2.  Consulte el ejemplo multimedia para la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) y proporcione un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , implementada por el descodificador. Cuando el representador de vídeo libera el ejemplo, se invocará la devolución de llamada del descodificador.
4.  Llame a [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Haga lo siguiente una o varias veces:
    1.  Llame a [**IDirectXVideoDecoder:: getBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obtener un búfer del descodificador de DXVA.
    2.  Rellene el búfer.
    3.  Llame a [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Llame a [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para realizar las operaciones de descodificación en el marco.

DXVA 2,0 utiliza las mismas estructuras de datos que DXVA 1,0 para las operaciones de descodificación. En el conjunto original de perfiles de DXVA (para H. 261, H. 263 y MPEG-2), estas estructuras de datos se describen en la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de llamadas de ejecución de [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , puede llamar a [**getBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) varias veces, pero solo una vez para cada tipo de búfer de DXVA. Si se llama dos veces con el mismo tipo de búfer, se sobrescribirán los datos.

Use la devolución de llamada del método [**SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (paso 3) para realizar un seguimiento de los ejemplos que están disponibles actualmente y que están en uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 
