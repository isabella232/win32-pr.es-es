---
description: Media Foundation eventos
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Media Foundation eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a63beeb3222ffef4151f45be95d13f9cf9ff4f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468740"
---
# <a name="media-foundation-events"></a>Media Foundation eventos



| Evento                                                                                        | Descripción                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Se quitó el dispositivo de audio.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | La sesión de audio se desconectó de una sesión Terminal Windows Services                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | La sesión de audio fue adelantada por una conexión en modo exclusivo.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | Se ha cambiado el formato de audio predeterminado para el dispositivo de audio.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Los parámetros de agrupación han cambiado para la sesión de audio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | Se ha cambiado el icono de la sesión de audio.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | El nombre para mostrar de la sesión de audio ha cambiado.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | El Windows servidor de audio se ha apagado.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | El estado de volumen o exclusión mutua de la sesión de audio ha cambiado                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Un origen de medios empezó a almacenar en búfer los datos.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Un origen de medios detuvo el almacenamiento en búfer de los datos.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | Se quitó el dispositivo.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | La sesión de audio está desconectada porque el usuario ha cerrado sesión de Terminal Windows Services (WTS).                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | El usuario abrió una secuencia de audio en modo exclusivo.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | El formato de audio ha cambiado.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | El servidor de sesión de audio se apaga.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | El volumen ha cambiado.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | El origen de red finalizó la apertura de una dirección URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | El origen de red empezó a abrir una dirección URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | La configuración ha cambiado para un esquema de protección de salida.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | Se ha completado la acción de un objeto habilitador de contenido.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Señala el progreso de un objeto habilitador de contenido.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Lo genera un origen multimedia cuando finaliza una presentación.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Lo genera el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Lo genera una secuencia de medios cuando finaliza la secuencia.                                                                                                           |
| [MEError](meerror.md)                                                                       | Indica un error grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Tipo de evento personalizado.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | Se ha completado la individualización.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | La individualización está a punto de comenzar.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | La adquisición de licencias se ha completado.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | La adquisición de licencias está a punto de comenzar.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Se genera cuando una secuencia multimedia entrega un nuevo ejemplo.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Una nueva presentación está lista para generarse mediante un origen multimedia.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Lo genera un origen multimedia cuando inicia una nueva secuencia.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Se produjo un error no grave durante el streaming.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | La directiva de salida de una secuencia ha cambiado.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Lo genera una salida de confianza si se produce un error al aplicar la directiva de salida.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contiene información de estado sobre el cumplimiento de una directiva de salida.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Se [**completó el método IMFOutputTrustAuthority::SetPolicy.**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy)                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Proporciona comentarios sobre la calidad de reproducción al administrador de calidad.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Lo genera un origen multimedia al final de un intento de reconexión.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Lo genera un origen multimedia al principio de un intento de reconexión.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Lo genera el representador de vídeo mejorado (EVR) cuando recibe un evento de usuario del presentador.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Lo genera el origen del secuenciador cuando el [**método ODBCSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se completa de forma asincrónica. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Lo genera la sesión multimedia cuando cambian las funcionalidades de la sesión.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Se genera cuando el [**método IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se completa de forma asincrónica.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | La genera la sesión multimedia cuando ha terminado de reproducir la última presentación en la cola de reproducción.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Se genera mediante la sesión multimedia cuando se inicia una nueva presentación.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Se genera cuando el [**método IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) se completa de forma asincrónica.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Lo genera la sesión multimedia cuando cambia la velocidad de reproducción.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Lo genera la sesión multimedia cuando completa una solicitud de limpieza.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Se genera cuando el [**método IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se completa de forma asincrónica.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Se genera cuando el [**método IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) se completa de forma asincrónica.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Lo genera la sesión multimedia cuando cambia el formato en un receptor multimedia.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Se genera mediante la sesión multimedia cuando el [**método DESINMEDIASESSION::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se completa de forma asincrónica.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Se genera después de que [**el método IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se complete de forma asincrónica                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Lo genera la sesión multimedia cuando cambia el estado de una topología.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Se genera cuando un receptor multimedia deja de ser válido.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Lo genera un origen multimedia cuando cambian las características del origen.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Lo genera un origen multimedia cuando actualiza sus metadatos.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Lo genera un origen multimedia cuando el [**método :P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) finaliza de forma asincrónica.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Lo genera un origen multimedia cuando cambia la velocidad de reproducción.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Se genera cuando un origen multimedia busca una nueva posición.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Se genera cuando un origen multimedia se inicia sin buscar.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Lo genera un origen multimedia cuando el [**método IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Lo genera una secuencia de medios cuando cambia el tipo de medio de la secuencia.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Lo genera una secuencia de medios cuando el método [**:P AUSE**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) finaliza de forma asincrónica.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | La generación por una secuencia de medios después de una llamada a [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoca una búsqueda en la secuencia.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Se genera mediante los receptores de flujo de la EVR si cambia el dispositivo de vídeo.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Lo genera un receptor de flujo cuando el tipo de medio del receptor ya no es válido.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Lo genera un receptor de flujo después de [**llamar al método :P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Lo genera un receptor de flujo cuando completa la transición al estado en pausa.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Lo genera un receptor de flujo cuando la secuencia ha recibido suficientes datos de inscripción previa para empezar a representarse.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Lo genera un receptor de flujo cuando la velocidad ha cambiado.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Lo genera un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Lo genera un receptor de flujo cuando completa una solicitud de limpieza.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Lo genera un receptor de flujo cuando completa la transición al estado en ejecución.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Lo genera un receptor de flujo cuando completa la transición al estado detenido.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Lo genera una secuencia de medios cuando el origen comienza sin buscar.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Lo genera una secuencia multimedia cuando el [**método IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se completa de forma asincrónica.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Lo genera una secuencia multimedia cuando inicia o detiene la simplificación de la secuencia.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Enviado por una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.                                                             |
| [METransformTransformTransformOutput](metransformhaveoutput.md)                                           | Enviado por un MFT asincrónico cuando hay nuevos datos de salida disponibles desde MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Enviado por un MFT asincrónico en respuesta a un [**mensaje MFT \_ MESSAGE COMMAND \_ \_ MARKER.**](mft-message-command-marker.md)                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Enviado por un MFT asincrónico para solicitar un nuevo ejemplo de entrada.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Tipo de evento desconocido.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | El dispositivo se ha adelantado.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | Se ha quitado el dispositivo.                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Generadores de eventos multimedia](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



