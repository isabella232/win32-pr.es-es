---
description: Microsoft Media Foundation se introdujo en Windows Vista como reemplazo de DirectShow. Por supuesto, DirectShow se admite en Windows 7, pero se recomienda a los desarrolladores que usen Media Foundation en sus nuevas aplicaciones multimedia digitales.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Novedades de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263164"
---
# <a name="whats-new-for-media-foundation"></a>Novedades de Media Foundation

Microsoft Media Foundation se introdujo en Windows Vista como reemplazo de DirectShow. Por supuesto, DirectShow se admite en Windows 7, pero se recomienda a los desarrolladores que usen Media Foundation en sus nuevas aplicaciones multimedia digitales.

Las mejoras en Media Foundation se pueden resumir de la siguiente manera:

-   Mejor compatibilidad con el formato, incluido MPEG-4
-   Compatibilidad con dispositivos de captura y códecs de hardware
-   Un modelo de programación simplificado
-   Mejoras en la plataforma

## <a name="better-format-support"></a>Mejor compatibilidad con el formato

La canalización de audio y vídeo Media Foundation se implementó en Windows Vista, pero admite un conjunto limitado de formatos y contenedores de archivos, lo que significaba que algunas aplicaciones necesitaban volver a usar tecnologías anteriores, como DirectShow. En Windows 7, Media Foundation los siguientes códecs nuevos, orígenes de medios y receptores multimedia:

-   Descodificador de AAC
-   Codificador AAC
-   Origen del archivo AVI/WAVE
-   Descodificador de vídeo DV
-   Descodificador de vídeo H.264
-   Codificador de vídeo H.264
-   Descodificador M JPEG
-   Receptor de archivos MP3\*
-   Origen de archivo MP4/3GP
-   Receptor de archivos MP4/3GP

> [!Note]  
> El receptor de archivos MP3 no incluye un codificador de audio MP3.

 

Para obtener más información, vea [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Compatibilidad con dispositivos de hardware

Media Foundation ahora admite los siguientes tipos de dispositivos de hardware en la canalización de audio y vídeo:

-   Dispositivos de captura de vídeo UVC 1.1, como cámaras web
-   Dispositivos de captura de audio
-   Codificadores y descodificadores de hardware
-   Procesadores de vídeo de hardware, como convertidores de espacio de color

Los códecs de hardware pueden realizar transcodificación de vídeo muy rápida. Por ejemplo, una aplicación podría transferir archivos Windows Media Video (WMV) a un teléfono móvil que solo admita archivos 3GP. Con un codificador de hardware, la aplicación puede transcodificar el archivo en el backgound, justo antes de transferirlo al dispositivo.

Los dispositivos de hardware se representan Media Foundation mediante un objeto proxy y se usan en la canalización igual que los componentes basados en software.

## <a name="simplified-programming-model"></a>Modelo de programación simplificado

En Windows Vista, Media Foundation un conjunto de API de nivel relativamente bajo. Estas API son flexibles, pero demasiado complejas para tareas sencillas. Windows 7 agrega nuevas API de alto nivel que hacen que sea más fácil escribir aplicaciones multimedia en C++. Estas nuevas API de alto nivel incluyen lo siguiente.



| API                                | Descripción                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lector de origen](source-reader.md) | El lector de origen extrae datos sin procesar o descodificados de un archivo multimedia. Por ejemplo, puede usar el lector de origen para obtener mapas de bits en miniatura de un archivo de vídeo o para analizar los datos de forma de onda en un archivo de audio. También puede usar el lector de origen para obtener datos en directo de un dispositivo de captura de audio o vídeo. <br/> |
| [Escritor de receptores](sink-writer.md)     | El escritor receptor permite crear archivos multimedia pasando datos sin comprimir o codificados. Por ejemplo, puede usarlo para volver a codificar un archivo de vídeo o para capturar vídeo en directo desde una cámara web a un archivo.                                                                                                         |
| [Transcodificación de API](transcode-api.md) | Esta característica admite los escenarios de codificación de audio y vídeo más comunes.<br/>                                                                                                                                                                                                                               |



 

Todavía puede usar las API de bajo nivel en Media Foundation. Puede hacerlo si necesita más control sobre la canalización de audio y vídeo.

## <a name="platform-improvements"></a>Mejoras en la plataforma

Windows 7 incluye numerosas mejoras en las API de plataforma Media Foundation subyacentes. Las aplicaciones avanzadas pueden usar estas API directamente; otras aplicaciones obtienen las ventajas indirectamente. Estas mejoras incluyen:

-   Cambios en la canalización de vídeo para reducir el consumo de energía y el uso de memoria de vídeo.
-   [DXVA-HD:](dxva-hd.md)Alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD) es una nueva API para el procesamiento de vídeo acelerado por hardware. DXVA-HD ofrece un modelo de composición más flexible que la API de procesamiento de vídeo DXVA anterior y es más adecuado para formatos de vídeo de alta definición.
-   Un nuevo mecanismo para enumerar los orígenes y descodificadores, que incluye los valores de los valores y una lista preferida o bloqueada. Esta característica mejora la confiabilidad general del sistema. Para obtener más información, vea los temas siguientes:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Codec Codec Codec (Códec de programación](codec-merit.md)

## <a name="sdk-changes"></a>Cambios en el SDK

-   Nuevos encabezados y archivos de biblioteca: [Media Foundation encabezados y bibliotecas](media-foundation-headers-and-libraries.md)
-   Cambios de DLL y .lib: [cambios de biblioteca en Windows 7](media-foundation-headers-and-libraries.md)
-   Nuevos ejemplos de SDK:
    -   [Ejemplo de clip de audio](audio-clip-sample.md)
    -   [Ejemplo de DXVA-HD](dxva-hd-sample.md)
    -   [Ejemplo MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Ejemplo MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Ejemplo de transcodificación](transcode-sample.md)
    -   [Ejemplo videoThumbnail](videothumbnail-sample.md)
-   Mejoras en [TopoEdit:](topoedit.md)
    -   Compatibilidad con la transcodificación. Consulte Building a [Transcode Topology with TopoEdit (Creación de una topología de transcodificación con TopoEdit).](building-a-transcode-topology-with-topoedit.md)
    -   Compatibilidad con la captura de audio y vídeo. Vea [Menú topología](topology-menu.md).

## <a name="new-in-windows-8"></a>Novedades de Windows 8

Algunas de las nuevas actualizaciones para Media Foundation con Windows 8 son:

-   [**EL BOTÓN DE CAPTURA Controla**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) uno o varios dispositivos de captura. Consulte atributos [del motor de captura](capture-engine-attributes.md) para obtener una lista de atributos. Otras nuevas interfaces relacionadas con la captura de medios [**son: IMFCapturePhotoSink,**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink) [**IMFCapturePreviewSink,**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink) [**IMFCaptureRecordSink,**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink) [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)y [**IMFCaptureSource.**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource)
-   Las siguientes Media Foundation de clase son nuevas para Windows 8:
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   [Direct3D 11 Video API son](direct3d-11-video-apis.md) nuevas para Windows 8. Windows 8 Las aplicaciones de escritorio todavía pueden usar Video API de [Direct3D 9,](direct3d-video-apis.md)pero Windows Store debe usar la nueva API de vídeo de Direct3D 11. Para obtener más información sobre Microsoft Direct3D 11 Video, vea [Supporting Direct3D 11 Video Decoding in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Se han realizado actualizaciones y mejoras en las Media Foundation de trabajo. Consulte [Mejoras de cola de trabajo y subprocesamiento](media-foundation-work-queue-and-threading-improvements.md) para obtener más información.
-   [Codificadores de cámara H.264 UVC 1.5](camera-encoder-h264-uvc-1-5.md).
-   Para obtener una lista de la API Media Foundation que se puede usar con las aplicaciones de Windows Store, consulte [Win32 y COM para Windows Store (multimedia).](media-foundation-headers-and-libraries.md)
-   Media Foundation no se incluye con las ediciones N y KN de Windows 8. Para obtener más información, vea [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




