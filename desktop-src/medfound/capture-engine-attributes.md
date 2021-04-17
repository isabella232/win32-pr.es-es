---
description: Los siguientes atributos se pueden usar para configurar el motor de captura.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Atributos del motor de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105697982"
---
# <a name="capture-engine-attributes"></a>Atributos del motor de captura

Los siguientes atributos se pueden usar para configurar el motor de captura.

Los siguientes atributos están relacionados con los dispositivos de captura:



| Atributo                                                                                                                              | Descripción                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [\_secuencia de cámara del motor de captura MF \_ \_ \_ \_ bloqueada](mf-capture-engine-camera-stream-blocked.md)                                            | Indica que el controlador está bloqueando la captura de vídeo.                                                         |
| [\_secuencia de cámara del motor de captura MF \_ \_ \_ \_ desbloqueada](mf-capture-engine-camera-stream-unblocked.md)                                        | Indica que la captura de vídeo se restaura después de ser bloqueada.                                                        |
| [\_ \_ Administrador D3D del motor de captura MF \_ \_](mf-capture-engine-d3d-manager.md)                                                                 | Establece un puntero al Administrador de dispositivos de DXGI en el motor de captura.                                                   |
| [MF \_ \_ descodificador del motor de captura del \_ descodificador de \_ MFT \_ FIELDOFUSE \_ Unlock \_ Attribute](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.                                    |
| [\_motor de captura MF \_ \_ deshabilitar \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Especifica si el motor de captura utiliza la aceleración de vídeo DirectX (DXVA) para la descodificación de vídeo.                    |
| [captura de MF \_ \_ deshabilitar \_ \_ transformaciones de hardware](mf-capture-engine-disable-hardware-transforms.md)                                        | Deshabilita el uso de transformaciones de Media Foundation basadas en hardware (MFTs) en el motor de captura.                       |
| [\_procesador de captura MF habilitar la \_ \_ \_ \_ notificación STREAMSTATE de cámara \_](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica si deben habilitarse las notificaciones de estado de secuencia.                                                    |
| [MF \_ codificador del motor de captura del \_ \_ codificador \_ MFT \_ FIELDOFUSE \_ Unlock ( \_ atributo)](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Permite que el motor de captura use un codificador que tenga restricciones de campo de uso.                                   |
| [\_GUID del \_ generador de eventos del motor de captura MF \_ \_ \_](mf-capture-engine-event-generator-guid.md)                                              | Identifica el componente que generó un evento de captura.                                                           |
| [\_Índice de \_ flujo de eventos del motor de captura MF \_ \_ \_](mf-capture-engine-event-stream-index.md)                                                  | Identifica qué secuencia generó un evento de captura.                                                                 |
| [\_configuración de \_ MEDIASOURCE del motor de captura MF \_ \_](mf-capture-engine-mediasource-config.md)                                                   | Contiene las propiedades de configuración para el origen de captura.                                                          |
| [\_ \_ \_ \_ \_ \_ número máximo de \_ muestras procesadas de audio de receptor de registro \_ del motor de captura MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de audio del receptor de registros.                   |
| [\_ \_ \_ \_ \_ \_ número máximo de \_ muestras sin procesar de audio \_ del motor de captura MF](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros. |
| [\_ \_ \_ \_ \_ \_ número máximo de \_ muestras procesadas del vídeo del receptor de registros \_ del motor de captura MF](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de vídeo del receptor de registros.                   |
| [\_ \_ \_ \_ \_ \_ número máximo de \_ muestras sin procesar de vídeo del receptor \_ MF de registro del motor de captura](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de vídeo del receptor de registros.  |
| [\_tipo de \_ receptor del motor de captura MF \_ \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Especifica un tipo de receptor de captura.                                                                                  |
| [el \_ motor de captura MF \_ \_ solo usa el \_ dispositivo de audio \_ \_](mf-capture-engine-use-audio-device-only.md)                                           | Especifica si el motor de captura captura audio pero no vídeo.                                                 |
| [el \_ motor de captura MF \_ \_ solo usa el \_ dispositivo de vídeo \_ \_](mf-capture-engine-use-video-device-only.md)                                           | Especifica si el motor de captura captura vídeo pero no audio.                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



