---
description: Mezcladores personalizados
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mezcladores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714929"
---
# <a name="custom-mixers"></a>Mezcladores personalizados

En este tema se describe cómo escribir un mezclador personalizado para el representador de vídeo mejorado (EVR). Puede usar un mezclador personalizado con el Media Foundation receptor de medios de EVR o el filtro de EVR de DirectShow. Para obtener más información sobre los mezclador y los presentadores, vea [representador de vídeo mejorado](enhanced-video-renderer.md).

El mezclador es una transformación de Media Foundation (MFT) con una o más entradas (el flujo de referencia más las subsecuencias) y una salida. El flujo de entrada recibe ejemplos de nivel superior. El flujo de salida proporciona ejemplos al presentador. EVR es responsable de llamar a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) en el mezclador y el presentador es responsable de llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Como mínimo, un mezclador de EVR debe implementar las siguientes interfaces:



| Interfaz                                                                | Descripción                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Proporciona la funcionalidad básica de MFT.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite al mezclador obtener interfaces de EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Permite al mezclador obtener interfaces de EVR.                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Se usa para exponer el atributo de [**\_ \_ \_ reconocimiento**](mf-sa-d3d-aware-attribute.md) de la SA de MF a EVR. |



 

Opcionalmente, una MFT puede implementar cualquiera de las interfaces siguientes:



| Interfaz                                                | Descripción                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Necesario para reproducir contenido protegido.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Expone interfaces como [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) y [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) a la aplicación. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Permite que el administrador de calidad ajuste la calidad del vídeo.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Permite que la aplicación mezcle un mapa de bits estático en el vídeo.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Asigna coordenadas del fotograma de vídeo de salida a las coordenadas del fotograma de vídeo de entrada.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Expone algunas características de procesamiento de vídeo de DXVA a la aplicación.                                                                                      |



 

La negociación de formato con el mezclador funciona de la siguiente manera:

1.  EVR establece el tipo de medio en el flujo de referencia.
2.  EVR llama a [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) en el presentador con el mensaje **MFVP \_ Message \_ INVALIDATEMEDIATYPE** .

3.  El presentador establece el tipo de medio en el flujo de salida del mezclador.
4.  EVR establece el tipo de medio en las subsecuencias.

Si el tipo de medio en el flujo de referencia cambia, los otros tipos de medios del mezclador ya no son válidos. Se producirá un error en el método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador y se devolverá el **\_ cambio de flujo de \_ transformación \_ \_ MF e**. El presentador no debe hacer nada en este momento. El EVR volverá a iniciar el proceso de negociación de formato.

Cuando un flujo de entrada alcanza el final de la secuencia, el EVR llama a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) en el mezclador con el [**\_ \_ \_ final \_ del \_ flujo de notificación de mensaje de MFT**](mft-message-notify-end-of-stream.md).

El mezclador envía los siguientes eventos a EVR, mediante la interfaz [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR. Esta interfaz se documenta en la documentación del SDK de DirectShow.



| Evento                                            | Descripción                            |
|--------------------------------------------------|----------------------------------------|
| [**ejemplo de EC \_ \_ necesario**](../directshow/ec-sample-needed.md) | El mezclador requiere un nuevo ejemplo de entrada. |



 

EVR puede llamar a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador antes de que se inicie el streaming. El mezclador no debe producir errores en estas llamadas. En su lugar, debe rellenar la superficie de salida con píxeles negros. El mezclador debe continuar con el relleno de colores de las muestras de salida hasta que reciba un [**mensaje de MFT \_ \_ Notify \_ Begin \_ streaming**](mft-message-notify-begin-streaming.md) Message o se llama al método [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . Si el mezclador recibe un [**mensaje de la \_ notificación de \_ \_ finalización de notificación \_**](mft-message-notify-end-streaming.md) de mensaje de MFT, debe volver a cambiar al modo de relleno de color.

## <a name="implementing-imfvideodeviceid"></a>Implementación de IMFVideoDeviceID

La interfaz [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un método, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), que devuelve un GUID de dispositivo. El GUID del dispositivo garantiza que el presentador y el mezclador usan tecnologías compatibles. Si los GUID del dispositivo no coinciden, el EVR no se puede inicializar.

El mezclador y el presentador estándar usan Direct3D 9, con el GUID de dispositivo igual a IID \_ IDirect3DDevice9. Si piensa usar el presentador personalizado con el mezclador estándar, el GUID del dispositivo del presentador debe ser IID \_ IDirect3DDevice9. Si reemplaza ambos componentes, podría definir un nuevo GUID de dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementación de IMFTopologyServiceLookupClient

El mezclador debe implementar la interfaz [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) . Antes de que comience el streaming, EVR llama a [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) y pasa un puntero a la interfaz [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) de EVR. El mezclador usa este puntero para obtener punteros de interfaz de EVR.

Como mínimo, el mezclador debe consultar la siguiente interfaz:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Cuando el EVR llama a [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), el mezclador debe liberar los punteros obtenidos de la llamada a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Atributos de Mixer

Un mezclador debe admitir los siguientes atributos.



| Atributo                                                                        | Descripción                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compatible con el D3D de MF \_ SA \_ \_**](mf-sa-d3d-aware-attribute.md)                          | Especifica si el mezclador es compatible con la aceleración de vídeo DirectX (DXVA).                                                                                                                                                                               |
| [**\_recuento \_ de \_ muestras \_ requerido de MF SA**](mf-sa-required-sample-count-attribute.md) | El número de muestras de vídeo que EVR debe asignar a cada flujo de mezclador. Este atributo se aplica a flujos individuales; Use el almacén de atributos devuelto por [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Establecimiento del mezclador en EVR

Para establecer un mezclador personalizado en EVR, llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). El filtro EVR de DirectShow y el receptor de medios de EVR implementan este método.

**Objeto de activación EVR**. Si usa el objeto de activación EVR, puede proporcionar un mezclador personalizado si establece uno de los siguientes atributos en el objeto de activación EVR:



| Atributo                                                                                                 | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ activar \_ \_ mezclador de vídeo personalizado \_ \_ activar**](mf-activate-custom-video-mixer-activate-attribute.md) | Puntero a un objeto de activación para el mezclador. El objeto de activación debe implementar la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . |
| [**MF \_ activar \_ \_ mezclador de vídeo personalizado \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID del mezclador.                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 
