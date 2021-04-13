---
description: El representador de vídeo mejorado (EVR) es un componente que muestra vídeo en el monitor de usuarios.
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: Representador de vídeo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360097"
---
# <a name="enhanced-video-renderer"></a>Representador de vídeo mejorado

El representador de vídeo mejorado (EVR) es un componente que muestra vídeo en el monitor del usuario. Existen dos versiones de EVR:

-   El receptor de medios EVR, para aplicaciones Media Foundation.
-   El filtro EVR para las aplicaciones de DirectShow.

Ambas versiones usan los mismos objetos internos para representar vídeo y comparten muchas de las mismas interfaces.

EVR puede mezclar hasta 16 secuencias de vídeo. El primer flujo de entrada se denomina *flujo de referencia*. El flujo de referencia siempre aparece primero en el orden z. Los flujos adicionales se denominan *subsecuencias* y se mezclan en la parte superior de la secuencia de referencia. La aplicación puede cambiar el orden z de las subsecuencias, pero no puede haber ningún subflujo en primer lugar en el orden z.

El controlador de gráficos determina qué formatos de vídeo se admiten, pero normalmente se limitan a lo siguiente:

-   Secuencia de referencia: YUV progresivo o entrelazado sin alfa por píxel (como NV12 o YUY2); o RGB progresivo.
-   Subsecuencias: YUV progresivo con alfa por píxel, como AYUV o AI44.

Los formatos de subflujo disponibles pueden depender del formato del flujo de referencia. Para obtener más información, vea [EVR Media Type negociación](evr-media-type-negotiation.md).

Internamente, el EVR usa un objeto denominado *mezclador* para componer los fotogramas de los flujos de entrada en una superficie para su representación. El mezclador también realiza el desentrelazado y la corrección del color. La salida del mezclador es el marco de vídeo compuesto final. Un segundo objeto denominado *Presenter* representa el fotograma de vídeo en la pantalla. El presentador programa Cuándo se representan los fotogramas y administra el dispositivo Direct3D. Una aplicación puede proporcionar una implementación personalizada del mezclador o del presentador.

La velocidad de fotogramas de salida está bloqueada en la secuencia de referencia. Cada vez que los subflujos reciben nuevos marcos, el mezclador los contiene. Cuando el flujo de referencia recibe un nuevo fotograma, el mezclador lo compone con los fotogramas de subsecuencia. (Si la secuencia de referencia está entrelazada, un marco de referencia completo puede requerir más de un ejemplo multimedia). Es posible que un subflujo reciba más de un fotograma mientras el mezclador está esperando un fotograma de referencia. En ese caso, el mezclador simplemente descarta el marco de subsecuencia anterior.

Dado que el presentador crea el dispositivo Direct3D, también es responsable de compartir el dispositivo con otros objetos de canalización que necesiten tener acceso a los servicios de aceleración de vídeo de DirectX (DXVA). En concreto, el mezclador de EVR usa los servicios de procesamiento de vídeo de DXVA para Desentrelazar y mezclar el vídeo. Externos a EVR, los descodificadores de software pueden usar DXVA para la descodificación de vídeo acelerada. El presentador comparte el dispositivo Direct3D mediante el Administrador de dispositivos de [Direct3D](direct3d-device-manager.md). En el diagrama siguiente se muestra la arquitectura interna de EVR. (El descodificador de software, sombreado en gris, no forma parte de la EVR).

![diagrama arquitectónico en el que se muestra el EVR.](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>Interfaces EVR

EVR admite las siguientes interfaces. El mezclador o el presentador implementa algunas de estas interfaces. Para cada interfaz, en el tema de referencia se describe cómo obtener un puntero a la interfaz.

| Interfaz                                                    | Descripción                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | Establece el número de clavijas de entrada en el filtro de EVR (solo DirectShow).                                |
| [**IEVRFilterConfigEx**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | Configura el filtro de EVR (solo DirectShow).                                                      |
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | Habilita un complemento de EVR para representar vídeo protegido.                                                 |
| [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | Permite que el presentador de EVR solicite un fotograma específico del mezclador.                             |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | Permite que el administrador de calidad ajuste la calidad del vídeo EVR.                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | Permite a un ponente o presentador personalizado obtener punteros de interfaz de EVR.                       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | Devuelve el identificador del dispositivo de un mezclador o un presentador de EVR.                                       |
| [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | Controla cómo el EVR muestra el vídeo.                                                              |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alpha: combina una imagen de mapa de bits estática con el vídeo.                                                |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | Controla la forma en que el representador de vídeo mejorado (EVR) combina subsecuencias de vídeo.                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | Controla las preferencias del desentrelazado de vídeo.                                                     |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | Asigna una posición en una secuencia de vídeo de entrada a la posición correspondiente en una secuencia de vídeo de salida. |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | Expuesto por el presentador de EVR.                                                                     |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | Controla el procesamiento de vídeo, incluidos el ajuste, los filtros de ruido y los filtros de detalle.               |
| [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | Establece un mezclador o presentador en el EVR.                                                             |
| [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | Asigna ejemplos de vídeo.                                                                          |



 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                    | Descripción                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Usar el filtro EVR de DirectShow](using-the-directshow-evr-filter.md)   | Cómo usar EVR en una aplicación de DirectShow.                                       |
| [Uso del receptor de medios de EVR](using-the-evr-media-sink.md)                 | Cómo usar EVR en una aplicación Media Foundation.                                 |
| [Usar los controles de presentación de vídeo](using-the-video-display-controls.md) | Cómo controlar el modo en que el EVR muestra el vídeo dentro de la ventana de la aplicación. |
| [Usar los controles de mezclador de vídeo](using-the-video-mixer-controls.md)     | Cómo controlar el modo en que funciona el mezclador de EVR.                               |
| [EVR negociación de tipo de medio](evr-media-type-negotiation.md)             | Describe cómo el EVR determina qué formatos de vídeo puede aceptar como entrada.          |
| [Mezcladores personalizados](custom-mixers.md)                                       | Cómo escribir un mezclador personalizado para el EVR.                                              |
| [Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)       | Cómo escribir un presentador personalizado para el EVR.                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 



