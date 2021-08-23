---
description: Mezcladores personalizados
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mezcladores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587206f7bc34d1fad4a64a12aeff9ab8ad21e18a84c92c8f2302776fdc126a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605995"
---
# <a name="custom-mixers"></a>Mezcladores personalizados

En este tema se describe cómo escribir un mezclador personalizado para el representador de vídeo mejorado (EVR). Puede usar un mezclador personalizado con el receptor de medios Media Foundation EVR o el DirectShow EVR. Para obtener más información sobre mezcladores y presentadores, vea [Representador de vídeo mejorado.](enhanced-video-renderer.md)

El mezclador es una Media Foundation transformación (MFT) con una o varias entradas (la secuencia de referencia más las subrecciones) y una salida. El flujo de entrada recibe muestras de nivel superior. El flujo de salida entrega ejemplos al presentador. EVR es responsable de llamar a [**LANTRANSFORMTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) en el mezclador, y el presentador es responsable de llamar a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Como mínimo, un mezclador EVR debe implementar las interfaces siguientes:



| Interfaz                                                                | Descripción                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Proporciona la funcionalidad base de MFT.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite que el mezclador obtenga interfaces de la EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Permite que el mezclador obtenga interfaces de la EVR.                                                |
| [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Se usa para exponer [**el atributo MF SA \_ \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) a evr. |



 

Opcionalmente, un MFT puede implementar cualquiera de las interfaces siguientes:



| Interfaz                                                | Descripción                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Necesario para reproducir contenido protegido.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Expone interfaces como [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) y [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) a la aplicación. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Permite al administrador de calidad ajustar la calidad del vídeo.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Permite a la aplicación mezclar un mapa de bits estático en el vídeo.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mapas coordenadas en el fotograma de vídeo de salida a coordenadas en el fotograma de vídeo de entrada.                                                                  |
| [**PROCESSORVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Expone algunas características de procesamiento de vídeo DXVA a la aplicación.                                                                                      |



 

La negociación de formato con el mezclador funciona de la siguiente manera:

1.  EvR establece el tipo de medio en la secuencia de referencia.
2.  EvR llama a [**MFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) en el presentador con el mensaje **\_ \_ INVALIDATEMEDIATYPE DE MFVP MESSAGE.**

3.  El presentador establece el tipo de medio en el flujo de salida del mezclador.
4.  EvR establece el tipo de medio en las substreams.

Si cambia el tipo de medio en la secuencia de referencia, los otros tipos de medios del mezclador ya no son válidos. A continuación, el [**método MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador producirá un error y devolverá **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**. El presentador no debe hacer nada en este momento. La EVR volverá a iniciar el proceso de negociación de formato.

Cuando cualquier flujo de entrada llega al final de la secuencia, el EVR llama a [**LAVTRANSFORMTRANSFORM::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) en el mezclador con [**MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM**](mft-message-notify-end-of-stream.md).

El mezclador envía los siguientes eventos a evr, mediante la interfaz [**IMediaEventSink de la**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) EVR. Esta interfaz se documenta en la documentación DirectShow SDK.



| Evento                                            | Descripción                            |
|--------------------------------------------------|----------------------------------------|
| [**EJEMPLO \_ DE EC \_ NECESARIO**](../directshow/ec-sample-needed.md) | El mezclador requiere un nuevo ejemplo de entrada. |



 

La EVR podría llamar a [**ProcessOutput en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) el mezclador antes de que se inicie el streaming. El mezclador no debe producir un error en estas llamadas. En su lugar, debe rellenar la superficie de salida con píxeles de color negro. El mezclador debe seguir rellenando los ejemplos de salida hasta que reciba un mensaje [**MFT \_ MESSAGE NOTIFY \_ BEGIN \_ \_ STREAMING**](mft-message-notify-begin-streaming.md) o se llame al [**método ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) Si el mezclador recibe un mensaje [**MFT \_ MESSAGE NOTIFY \_ END \_ \_ STREAMING,**](mft-message-notify-end-streaming.md) debe volver al modo de relleno de color.

## <a name="implementing-imfvideodeviceid"></a>Implementación de IMFVideoDeviceID

La [**interfaz IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un método, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)que devuelve un GUID de dispositivo. El GUID del dispositivo garantiza que el presentador y el mezclador usan tecnologías compatibles. Si los GUID del dispositivo no coinciden, la EVR no se inicializa.

Tanto el mezclador estándar como el presentador usan Direct3D 9, con el GUID del dispositivo igual a \_ IID IDirect3DDevice9. Si piensa usar el presentador personalizado con el mezclador estándar, el GUID del dispositivo del presentador debe ser \_ IID IDirect3DDevice9. Si reemplaza ambos componentes, podría definir un nuevo GUID de dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementación de IMFTopologyServiceLookupClient

El mezclador debe implementar la [**interfaz IMFTopologyServiceLookupClient.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) Antes de comenzar el streaming, evr llama a [**LAVTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) y pasa un puntero a la interfaz [**DEVTOPOLOGYServiceLookup.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) El mezclador usa este puntero para obtener punteros de interfaz de evr.

Como mínimo, el mezclador debe consultar la siguiente interfaz:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Cuando el EVR llama [**a LAVTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), el mezclador debe liberar los punteros obtenidos de la llamada a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Mixer Atributos

Un mezclador debe admitir los atributos siguientes.



| Atributo                                                                        | Descripción                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                          | Especifica si el mezclador admite la aceleración de vídeo de DirectX (DXVA).                                                                                                                                                                               |
| [**RECUENTO \_ DE MUESTRAS \_ REQUERIDAS \_ DE \_ MF SA**](mf-sa-required-sample-count-attribute.md) | Número de muestras de vídeo que debe asignar la EVR para cada secuencia mezcladora. Este atributo se aplica a secuencias individuales; use el almacén de atributos devuelto por [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Establecimiento del Mixer en la EVR

Para establecer un mezclador personalizado en evr, llame [**a IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). Tanto el DirectShow EVR como el receptor de medios EVR implementan este método.

**Objeto de activación de EVR**. Si usa el objeto de activación EVR, puede proporcionar un mezclador personalizado estableciendo uno de los siguientes atributos en el objeto de activación evr:



| Atributo                                                                                                 | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md) | Puntero a un objeto de activación para el mezclador. El objeto de activación debe implementar la [**interfaz IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID del mezclador.                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 
