---
description: Los atributos siguientes se pueden usar para configurar el motor de captura.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Atributos del motor de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241161"
---
# <a name="capture-engine-attributes"></a>Atributos del motor de captura

Los atributos siguientes se pueden usar para configurar el motor de captura.

Los atributos siguientes están relacionados con los dispositivos de captura:



| Atributo                                                                                                                              | Descripción                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [FLUJO DE \_ CÁMARA DEL MOTOR DE CAPTURA MF \_ \_ \_ \_ BLOQUEADO](mf-capture-engine-camera-stream-blocked.md)                                            | Indica que el controlador está bloqueando la captura de vídeo.                                                         |
| [FLUJO DE \_ CÁMARA DEL MOTOR DE CAPTURA MF \_ \_ \_ \_ DESBLOQUEADO](mf-capture-engine-camera-stream-unblocked.md)                                        | Indica que la captura de vídeo se restaura después de bloquearse.                                                        |
| [MF \_ CAPTURE \_ ENGINE \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md)                                                                 | Establece un puntero a la Administrador de dispositivos DXGI en el motor de captura.                                                   |
| [MF \_ CAPTURE \_ ENGINE \_ DECODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.                                    |
| [EL MOTOR DE CAPTURA DE MF \_ \_ DESHABILITA \_ \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Especifica si el motor de captura usa la aceleración de vídeo de DirectX (DXVA) para lacodización de vídeo.                    |
| [MF \_ CAPTURE DESHABILITA LAS \_ \_ TRANSFORMACIONES DE \_ HARDWARE](mf-capture-engine-disable-hardware-transforms.md)                                        | Deshabilita el uso de transformaciones de Media Foundation hardware (MTA) en el motor de captura.                       |
| [MF \_ CAPTURE \_ ENGINE \_ ENABLE \_ CAMERA \_ STREAMSTATE \_ NOTIFICATION](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica si se deben habilitar las notificaciones de estado de secuencia.                                                    |
| [MF \_ CAPTURE \_ ENGINE \_ ENCODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Permite que el motor de captura use un codificador que tenga restricciones de campo de uso.                                   |
| [GUID DEL \_ GENERADOR DE EVENTOS DEL MOTOR DE CAPTURA DE \_ \_ \_ \_ MF](mf-capture-engine-event-generator-guid.md)                                              | Identifica el componente que generó un evento de captura.                                                           |
| [ÍNDICE DE \_ FLUJO DE EVENTOS DEL MOTOR DE CAPTURA \_ \_ \_ \_ DE MF](mf-capture-engine-event-stream-index.md)                                                  | Identifica qué secuencia generó un evento de captura.                                                                 |
| [CONFIGURACIÓN DE \_ \_ MEDIASOURCE DEL \_ MOTOR DE CAPTURA \_ DE MF](mf-capture-engine-mediasource-config.md)                                                   | Contiene propiedades de configuración para el origen de captura.                                                          |
| [MUESTRAS \_ PROCESADAS \_ \_ MÁXIMAS DE \_ AUDIO DEL RECEPTOR DE REGISTRO DEL MOTOR \_ \_ \_ DE \_ CAPTURA DE MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de audio del receptor de registros.                   |
| [MUESTRAS MÁXIMAS DE AUDIO SIN PROCESAR DEL RECEPTOR DE REGISTRO DEL MOTOR DE CAPTURA \_ \_ \_ \_ \_ \_ \_ \_ DE MF](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros. |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ PROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso del vídeo receptor de registros.                   |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ UNPROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso del vídeo receptor de registros.  |
| [TIPO DE \_ RECEPTOR DEL MOTOR DE CAPTURA \_ \_ \_ DE MF](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Especifica un tipo de receptor de captura.                                                                                  |
| [MF \_ CAPTURE ENGINE USE AUDIO DEVICE ONLY \_ \_ (USAR SOLO DISPOSITIVO DE \_ \_ \_ AUDIO)](mf-capture-engine-use-audio-device-only.md)                                           | Especifica si el motor de captura captura audio, pero no vídeo.                                                 |
| [EL \_ MOTOR DE CAPTURA DE MF USA SOLO DISPOSITIVO DE \_ \_ \_ \_ \_ VÍDEO](mf-capture-engine-use-video-device-only.md)                                           | Especifica si el motor de captura captura vídeo, pero no audio.                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



