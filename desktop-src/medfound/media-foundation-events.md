---
description: Eventos de Media Foundation
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Eventos de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a63beeb3222ffef4151f45be95d13f9cf9ff4f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707535"
---
# <a name="media-foundation-events"></a>Eventos de Media Foundation



| Evento                                                                                        | Descripción                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Se quitó el dispositivo de audio.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | La sesión de audio se desconectó de una sesión de Windows Terminal Services                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | Una conexión de modo exclusivo ha adelantado la sesión de audio.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | El formato de audio predeterminado para el dispositivo de audio ha cambiado.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Parámetros de agrupación modificados para la sesión de audio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | El icono de la sesión de audio ha cambiado.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | Cambió el nombre para mostrar de la sesión de audio.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | Se apagó el sistema del servidor de audio de Windows.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | El volumen o silenciar el estado de la sesión de audio cambió                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Un origen de medios comenzó a almacenar en búfer los datos.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Un origen multimedia dejó de almacenar en búfer los datos.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | Se quitó el dispositivo.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | La sesión de audio está desconectada porque el usuario cerró sesión en una sesión de Windows Terminal Services (WTS).                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | El usuario abrió una secuencia de audio en modo exclusivo.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | El formato de audio ha cambiado.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | Cierre del servidor de sesión de audio.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | El volumen cambió.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | El origen de red ha terminado de abrir una dirección URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | El origen de red comenzó a abrir una dirección URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | La configuración cambió para un esquema de protección de salida.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | Se ha completado la acción de un objeto de habilitador de contenido.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Indica el progreso de un objeto de habilitador de contenido.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Lo genera un origen multimedia cuando finaliza una presentación.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Generado por el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Generado por una secuencia de medios cuando finaliza la secuencia.                                                                                                           |
| [MEError](meerror.md)                                                                       | Indica un error grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Tipo de evento personalizado.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | Se ha completado la individualización.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | La individualización está a punto de comenzar.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | La adquisición de la licencia ha finalizado.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | La adquisición de licencias está a punto de comenzar.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Se genera cuando un flujo multimedia entrega un nuevo ejemplo.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Generado por un origen multimedia: una nueva presentación está lista.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Lo genera un origen multimedia cuando inicia una nueva secuencia.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Se produjo un error no irrecuperable durante el streaming.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | Ha cambiado la Directiva de salida de una secuencia.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Generado por una salida de confianza si se produce un error durante la aplicación de la Directiva de salida.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contiene información de estado sobre el cumplimiento de una directiva de salida.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Se completó el método [**IMFOutputTrustAuthority:: SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) .                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Proporciona comentarios sobre la calidad de reproducción al administrador de calidad.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Generado por un origen multimedia al final de un intento de reconexión.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Generado por un origen multimedia al inicio de un intento de reconexión.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Lo genera el representador de vídeo mejorado (EVR) cuando recibe un evento de usuario del presentador.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Generado por el origen del secuenciador cuando el método [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se completa de forma asincrónica. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Lo genera la sesión multimedia cuando cambian las capacidades de la sesión.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Se genera cuando el método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se completa de forma asincrónica.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Lo genera la sesión multimedia cuando ha terminado de reproducir la última presentación en la cola de reproducción.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | La inicia la sesión multimedia cuando se inicia una nueva presentación.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Se genera cuando el método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) se completa de forma asincrónica.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | La inicia la sesión de medios cuando cambia la velocidad de reproducción.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | La inicia la sesión multimedia cuando completa una solicitud de limpieza.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Se genera cuando el método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se completa de forma asincrónica.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Se genera cuando el método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) se completa de forma asincrónica.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | La inicia la sesión de medios cuando el formato cambia en un receptor de medios.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | La inicia la sesión de medios cuando el método [**IMFMediaSession:: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se completa de forma asincrónica.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Se genera después de que el método [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se complete de forma asincrónica.                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | La inicia la sesión de medios cuando cambia el estado de una topología.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Se genera cuando un receptor de medios deja de ser válido.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Generado por un origen multimedia cuando cambian las características del origen.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Lo genera un origen multimedia cuando actualiza sus metadatos.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Generado por un origen multimedia cuando el método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se completa de forma asincrónica.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Generado por un origen de medios cuando cambia la velocidad de reproducción.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Se genera cuando un origen multimedia busca una nueva posición.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Se genera cuando un origen multimedia comienza sin búsquedas.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Generado por un origen multimedia cuando el método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Generado por un flujo multimedia cuando cambia el tipo de medio del flujo.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Generado por un flujo multimedia cuando el método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se completa de forma asincrónica.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Generado por un flujo multimedia después de una llamada a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda en la secuencia.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Producidos por los receptores de flujo de EVR si cambia el dispositivo de vídeo.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Generado por un receptor de flujo cuando el tipo de medio del receptor ya no es válido.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Generado por un receptor de secuencia después de llamar al método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Generado por un receptor de flujo cuando completa la transición al estado de pausa.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Generado por un receptor de flujo cuando la secuencia ha recibido suficientes datos de preprocesamiento para empezar a representar.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Generado por un receptor de flujo cuando la tasa ha cambiado.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Generado por un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Generado por un receptor de flujo cuando completa una solicitud de limpieza.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Generado por un receptor de flujo cuando completa la transición al estado en ejecución.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Generado por un receptor de flujo cuando completa la transición al estado detenido.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Generado por un flujo multimedia cuando el origen comienza sin búsquedas.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Generado por un flujo multimedia cuando el método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Generado por un flujo multimedia cuando se inicia o detiene el ligero flujo de la secuencia.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Lo envía una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Lo envía un MFT asincrónico cuando hay nuevos datos de salida disponibles desde la MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Enviado por un MFT asincrónico en respuesta a un mensaje [**de \_ \_ \_ marcador de comando de mensaje de MFT**](mft-message-command-marker.md) .                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Lo envía un MFT asincrónico para solicitar un nuevo ejemplo de entrada.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Tipo de evento desconocido.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | Se ha cambiado el dispositivo.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | Se ha quitado el dispositivo.                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Generadores de eventos multimedia](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



