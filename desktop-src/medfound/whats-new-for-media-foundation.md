---
description: Microsoft Media Foundation se presentó en Windows Vista como sustituto de DirectShow. Por supuesto, DirectShow todavía se admite en Windows 7, pero se recomienda que los desarrolladores usen Media Foundation en sus nuevas aplicaciones multimedia digitales.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Novedades de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361872"
---
# <a name="whats-new-for-media-foundation"></a>Novedades de Media Foundation

Microsoft Media Foundation se presentó en Windows Vista como sustituto de DirectShow. Por supuesto, DirectShow todavía se admite en Windows 7, pero se recomienda que los desarrolladores usen Media Foundation en sus nuevas aplicaciones multimedia digitales.

Las mejoras en Media Foundation se pueden resumir de la manera siguiente:

-   Mejor compatibilidad con el formato, incluido MPEG-4
-   Compatibilidad con dispositivos de captura y códecs de hardware
-   Un modelo de programación simplificado
-   Mejoras en la plataforma

## <a name="better-format-support"></a>Mejor compatibilidad con el formato

La canalización de audio y vídeo de Media Foundation se implementó en Windows Vista, pero admitía un conjunto limitado de formatos y contenedores de archivos, lo que significaba que algunas aplicaciones necesitaban revertir a tecnologías anteriores como DirectShow. En Windows 7, Media Foundation incluye los nuevos códecs, orígenes multimedia y receptores multimedia siguientes:

-   Descodificador AAC
-   Codificador AAC
-   Origen de archivo AVI/WAVE
-   Descodificador de vídeo DV
-   Descodificador de vídeo H. 264
-   Codificador de vídeo H. 264
-   Descodificador MJPEG
-   Receptor de archivos MP3\*
-   Origen de archivo MP4/3GP
-   Receptor de archivos MP4/3GP

> [!Note]  
> El receptor de archivos MP3 no incluye un codificador de audio MP3.

 

Para obtener más información, vea [formatos multimedia compatibles en Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Compatibilidad con dispositivos de hardware

Media Foundation ahora admite los siguientes tipos de dispositivos de hardware en la canalización de audio y vídeo:

-   Dispositivos de captura de vídeo de UVC 1,1, como cámaras Web
-   Dispositivos de captura de audio
-   Codificadores y descodificadores de hardware
-   Procesadores de vídeo de hardware, como convertidores de espacio de color

Los códecs de hardware pueden realizar una transcodificación de vídeo muy rápida. Por ejemplo, una aplicación podría transferir archivos de Windows Media Video (WMV) a un teléfono móvil que solo admita archivos 3GP. Con un codificador de hardware, la aplicación puede transcodificar el archivo en Backgound, justo antes de transferirlo al dispositivo.

Los dispositivos de hardware se representan en Media Foundation mediante un objeto proxy, y se usan en la canalización como componentes basados en software.

## <a name="simplified-programming-model"></a>Modelo de programación simplificado

En Windows Vista, Media Foundation expone un conjunto de API de nivel relativamente bajo. Estas API son flexibles, pero demasiado complejas para tareas sencillas. Windows 7 agrega nuevas API de alto nivel que facilitan la escritura de aplicaciones multimedia en C++. Estas nuevas API de alto nivel incluyen lo siguiente.



| API                                | Descripción                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lector de origen](source-reader.md) | El lector de origen extrae datos sin procesar o descodificados de un archivo multimedia. Por ejemplo, puede usar el lector de origen para obtener mapas de bits en miniatura de un archivo de vídeo o para analizar los datos de la imagen de onda en un archivo de audio. También puede usar el lector de origen para obtener datos en directo de un dispositivo de captura de audio o vídeo. <br/> |
| [Escritor de receptor](sink-writer.md)     | El escritor de receptores le permite crear archivos multimedia pasando datos sin comprimir o codificados. Por ejemplo, puede usarlo para volver a codificar un archivo de vídeo o para capturar vídeo en directo desde una cámara web a un archivo.                                                                                                         |
| [API de transcodificación](transcode-api.md) | Esta característica es compatible con los escenarios de codificación de audio y vídeo más comunes.<br/>                                                                                                                                                                                                                               |



 

Todavía puede usar las API de bajo nivel en Media Foundation. Podría hacerlo si necesita más control sobre la canalización de audio y vídeo.

## <a name="platform-improvements"></a>Mejoras en la plataforma

Windows 7 incluye numerosas mejoras en las API de la plataforma de Media Foundation subyacente. Las aplicaciones avanzadas pueden usar estas API directamente; otras aplicaciones obtendrán las ventajas indirectamente. Estas mejoras incluyen:

-   Cambios en la canalización de vídeo para reducir el consumo de energía y el uso de memoria de vídeo.
-   [DXVA-HD](dxva-hd.md): alta definición de la aceleración de vídeo de Microsoft DirectX (DXVA-HD) es una nueva API para el procesamiento de vídeo acelerado por hardware. DXVA-HD ofrece un modelo de composición más flexible que la API de procesamiento de vídeo de DXVA anterior y es más adecuado para los formatos de vídeo de alta definición.
-   Un nuevo mecanismo para enumerar orígenes y descodificadores, que incluye valores de méritos y una lista preferida o bloqueada. Esta característica mejora la confiabilidad general del sistema. Para obtener más información, vea los temas siguientes:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Mérito del códec](codec-merit.md)

## <a name="sdk-changes"></a>Cambios en el SDK

-   Nuevos encabezados y archivos de biblioteca: [Media Foundation encabezados y bibliotecas](media-foundation-headers-and-libraries.md)
-   Cambios de DLL y. lib: [cambios de biblioteca en Windows 7](media-foundation-headers-and-libraries.md)
-   Nuevos ejemplos de SDK:
    -   [Ejemplo de clip de audio](audio-clip-sample.md)
    -   [DXVA: ejemplo HD](dxva-hd-sample.md)
    -   [Ejemplo de MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Ejemplo de MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Ejemplo de Transcode](transcode-sample.md)
    -   [Ejemplo de videominiatura](videothumbnail-sample.md)
-   Mejoras en [TopoEdit](topoedit.md):
    -   Compatibilidad con la transcodificación. Vea creación de una [topología de transcodificación con TopoEdit](building-a-transcode-topology-with-topoedit.md).
    -   Compatibilidad con la captura de audio y vídeo. Vea [menú de topología](topology-menu.md).

## <a name="new-in-windows-8"></a>Novedades de Windows 8

Algunas de las nuevas actualizaciones de Media Foundation con Windows 8 son:

-   [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) controla uno o varios dispositivos de captura. Vea los [atributos del motor de captura](capture-engine-attributes.md) para obtener una lista de atributos. Otras interfaces nuevas relacionadas con la captura multimedia son [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)y [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Las siguientes extensiones de clase de Media Foundation son nuevas para Windows 8:
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   La [API de vídeo de Direct3D 11](direct3d-11-video-apis.md) es nueva en Windows 8. Las aplicaciones de escritorio de Windows 8 todavía pueden usar la [API de vídeo Direct3D 9](direct3d-video-apis.md), pero las aplicaciones de la tienda Windows deben usar la nueva API de vídeo Direct3D 11. Para obtener más información sobre el vídeo de Microsoft Direct3D 11, consulte [compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Se han realizado actualizaciones y mejoras en Media Foundation colas de trabajo. Consulte [mejoras en la cola de trabajo y el subproceso](media-foundation-work-queue-and-threading-improvements.md) para obtener más información.
-   [Codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).
-   Para obtener una lista de las API de Media Foundation que se pueden usar con aplicaciones de la tienda Windows [, vea Win32 y com para aplicaciones de la tienda Windows (multimedia)](media-foundation-headers-and-libraries.md).
-   Media Foundation no se incluye con las ediciones N y KN de Windows 8. Para obtener más información, consulte [Microsoft Windows Media Feature Pack para las versiones N y kN de todas las ediciones de Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




