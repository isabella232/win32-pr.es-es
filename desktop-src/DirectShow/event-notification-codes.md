---
description: Códigos de notificación de eventos
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Códigos de notificación de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54792e433535ceefad416033d7758f4398b7777951173256c9be9b83913d61f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015793"
---
# <a name="event-notification-codes"></a>Códigos de notificación de eventos

En esta sección se enumeran DirectShow eventos que no son específicos de DVD. Para eventos específicos de DVD, vea [Códigos de notificación de eventos de DVD.](dvd-notification-codes.md)

Los filtros envían eventos al Administrador de Graph filtro mediante una llamada [**al método IMediaEventSink::Notify.**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) Filter Graph Manager controla algunos eventos y pone en cola otros para la aplicación. La aplicación los recupera llamando al [**método IMediaEvent::GetEvent.**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)

En las secciones siguientes, cada entrada muestra el código de evento, el significado de los parámetros de evento y la acción predeterminada del Administrador de filtros Graph para el evento, si lo hay. Para invalidar la acción predeterminada, llame a [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). Los códigos de evento se definen en los archivos de encabezado Evcode.h y Audevcod.h. Si no hay ninguna acción predeterminada, filter Graph Manager reenvía automáticamente el evento a la aplicación (a través de la cola de eventos).

**Eventos personalizados**

Los filtros pueden definir eventos personalizados con códigos de evento en el intervalo EC \_ USER y superior. El Administrador Graph filtros los colocará directamente en la cola de eventos. Sin embargo, se aplican las siguientes advertencias:

-   Filter Graph Manager no puede liberar los parámetros de evento mediante el método [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) normal. La aplicación debe liberar los recuentos de memoria o de referencia asociados a los parámetros de evento.
-   El filtro solo debe enviar el evento desde dentro de una aplicación que esté preparada para controlar el evento. (Es posible que la aplicación pueda establecer una propiedad personalizada en el filtro para indicar que es seguro enviar el evento).



| Código de notificación de eventos                                                 | Descripción                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                                     | Se está activando o desactivando una ventana de vídeo.                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | No compatible.                                                                                                            |
| [**DATOS \_ DE ALMACENAMIENTO EN BÚFER DE \_ EC**](ec-buffering-data.md)                        | El gráfico almacena en búfer los datos o ha detenido el almacenamiento en búfer de los datos.                                                               |
| [**EC \_ BUILT**](ec-built.md)                                           | Envíe por el Control de vídeo cuando se haya creado un gráfico. No se reenvía a las aplicaciones.                                     |
| [**CAMBIO \_ DEL RELOJ DE LA \_ EC**](ec-clock-changed.md)                          | El reloj de referencia ha cambiado.                                                                                          |
| [**EC \_ CLOCK \_ UNSET**](ec-clock-unset.md)                              | El proveedor de reloj se desconectó.                                                                                      |
| [**EVENTO \_ CODECAPI \_ DE EC**](ec-codecapi-event.md)                        | Enviado por un codificador para indicar un evento de codificación.                                                                           |
| [**EC \_ COMPLETE**](ec-complete.md)                                     | Se han representado todos los datos de una secuencia determinada.                                                                      |
| [**EC \_ CONTENTPROPERTY \_ HA CAMBIADO**](ec-contentproperty-changed.md)      | No compatible.                                                                                                            |
| [**DISPOSITIVO \_ EC \_ PERDIDO**](ec-device-lost.md)                              | Un Plug and Play se quitó o ha vuelto a estar disponible.                                                         |
| [**EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md)                      | El modo de presentación ha cambiado.                                                                                             |
| [**FIN \_ DE SEGMENTO DE \_ \_ EC**](ec-end-of-segment.md)                       | Se ha alcanzado el final de un segmento.                                                                                    |
| [**EC \_ EOS \_ SOON**](ec-eos-soon.md)                                    | No compatible.                                                                                                            |
| [**\_ERROR DE EC \_ STILLPLAYING**](ec-error-stillplaying.md)                | Error en un comando asincrónico para ejecutar el gráfico.                                                                      |
| [**\_ERROR DE ECABORT**](ec-errorabort.md)                                 | Se anuló una operación debido a un error.                                                                             |
| [**\_ERROR DE ECABORTEX**](ec-errorabortex.md)                             | Se anuló una operación debido a un error.                                                                             |
| [**CAMBIO \_ DEL MODO EXTDEVICE DE \_ \_ EC**](ec-extdevice-mode-change.md)         | No compatible.                                                                                                            |
| [**ARCHIVO \_ EC \_ CERRADO**](ec-file-closed.md)                              | El archivo de origen se cerró debido a un evento inesperado.                                                                |
| [**EC \_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md)                      | El representador de vídeo está cambiando del modo de pantalla completa.                                                                  |
| [**EC \_ GRAPH \_ HA CAMBIADO**](ec-graph-changed.md)                          | El gráfico de filtro ha cambiado.                                                                                             |
| [**EC \_ LENGTH \_ CHANGED**](ec-length-changed.md)                        | La longitud de un origen ha cambiado.                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | Notifica a la aplicación el progreso al abrir un archivo de red.                                                         |
| [**EC \_ MARKER \_ HIT**](ec-marker-hit.md)                                | No compatible.                                                                                                            |
| [**EC \_ NEED \_ RESTART**](ec-need-restart.md)                            | Un filtro solicita que se reinicie el gráfico.                                                                       |
| [**NUEVO \_ \_ PIN de EC**](ec-new-pin.md)                                      | No compatible.                                                                                                            |
| [**VENTANA \_ DE NOTIFICACIÓN DE \_ EC**](ec-notify-window.md)                          | Notifica a un filtro la ventana del representador de vídeo.                                                                         |
| [**EVENTO \_ OLE \_ DE EC**](ec-ole-event.md)                                  | Un filtro pasa una cadena de texto a la aplicación.                                                                     |
| [**ARCHIVO \_ DE APERTURA DE \_ EC**](ec-opening-file.md)                            | El gráfico está abriendo un archivo o ha terminado de abrir un archivo.                                                              |
| [**CAMBIO DE \_ LA PALETA \_ DE EC**](ec-palette-changed.md)                      | La paleta de vídeos ha cambiado.                                                                                            |
| [**EC \_ PAUSED**](ec-paused.md)                                         | Se ha completado una solicitud de pausa.                                                                                            |
| [**EC \_ PLEASE \_ REOPEN**](ec-please-reopen.md)                          | El archivo de origen ha cambiado.                                                                                              |
| [**EC \_ PREPROCESS \_ COMPLETE**](ec-preprocess-complete.md)              | Enviado por el [filtro WM ASF Writer](wm-asf-writer-filter.md) cuando completa el procesamiento previo para la codificación multipass. |
| [**LATENCIA \_ DE PROCESAMIENTO DE \_ EC**](ec-processing-latency.md)                | Indica la cantidad de tiempo que un componente está tardando en procesar cada muestra.                                           |
| [**CAMBIO \_ DE CALIDAD DE \_ EC**](ec-quality-change.md)                        | El gráfico quita muestras para el control de calidad.                                                                       |
| [**EC \_ RENDER \_ FINISHED**](ec-render-finished.md)                      | No compatible.                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                                       | Un representador de vídeo requiere un repintado.                                                                                      |
| [**LATENCIA \_ DE EJEMPLO DE \_ EC**](ec-sample-latency.md)                        | Especifica el retraso en la programación de un componente para el procesamiento de muestras.                                                  |
| [**EJEMPLO \_ DE EC \_ NECESARIO**](ec-sample-needed.md)                          | Solicita un nuevo ejemplo de entrada del filtro Representador de vídeo mejorado (EVR).                                                |
| [**TIEMPO DE \_ LIMPIEZA \_ DE EC**](ec-scrub-time.md)                                | Especifica la marca de tiempo para el paso de fotograma más reciente.                                                                  |
| [**EC \_ SEGMENT \_ STARTED**](ec-segment-started.md)                      | Se ha iniciado un nuevo segmento.                                                                                                |
| [**EC \_ SHUTTING \_ DOWN**](ec-shutting-down.md)                          | El gráfico de filtros se está cerrando, antes de destruirse.                                                              |
| [**ERROR \_ DE SNDDEV \_ DE \_ EC**](ec-snddev-in-error.md)                     | Se ha producido un error de dispositivo en un filtro de captura de audio.                                                                   |
| [**\_ERROR DE SALIDA DE SNDDEV DE \_ \_ EC**](ec-snddev-out-error.md)                   | Se ha producido un error de dispositivo en un filtro de representador de audio.                                                                  |
| [**EC \_ STARVATION**](ec-starvation.md)                                 | Un filtro no recibe suficientes datos.                                                                                    |
| [**CAMBIO \_ DE ESTADO DE \_ EC**](ec-state-change.md)                            | El gráfico de filtros ha cambiado de estado.                                                                                       |
| [**ESTADO \_ DE LA EC**](ec-status.md)                                         | Contiene dos cadenas de estado arbitrarias.                                                                                    |
| [**PASO \_ DE EC \_ COMPLETADO**](ec-step-complete.md)                          | Un filtro que realiza la ejecución paso a paso del marco ha escalonado el número especificado de fotogramas.                                            |
| [**EC \_ STREAM \_ CONTROL \_ STARTED**](ec-stream-control-started.md)       | Un comando stream-control start ha tenido efecto.                                                                          |
| [**EC \_ STREAM \_ CONTROL \_ STOPPED**](ec-stream-control-stopped.md)       | Un comando stream-control stop ha tenido efecto.                                                                           |
| [**ERROR \_ DE EC STREAM \_ \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | Se ha producido un error en una secuencia. La secuencia todavía se está reproduciendo.                                                           |
| [**ERROR \_ DE EC STREAM \_ \_ DETENIDO**](ec-stream-error-stopped.md)           | Una secuencia se ha detenido debido a un error.                                                                                 |
| [**EC \_ TIMECODE \_ DISPONIBLE**](ec-timecode-available.md)                | No compatible.                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | Enviar por el control de vídeo cuando se ha desandado un gráfico. No se reenvía a las aplicaciones.                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | El usuario ha finalizado la reproducción.                                                                                         |
| [**CAMBIO \_ EN EL TAMAÑO DEL VÍDEO DE \_ \_ EC**](ec-video-size-changed.md)               | El tamaño del vídeo nativo ha cambiado.                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | Un fotograma de vídeo está listo para mostrarse.                                                                                       |
| [**ERROR \_ DE RECONEXIÓN DE VMR \_ DE \_ EC**](ec-vmr-reconnection-failed.md)     | Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico desde el descodificador ascendente.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ SET**](ec-vmr-renderdevice-set.md)           | Se envía cuando vmr ha seleccionado su mecanismo de representación.                                                                   |
| [**SUPERFICIE \_ DE VMR \_ DE EC \_ VOLTEADO**](ec-vmr-surface-flipped.md)             | Se envía cuando el presentador del asignador de VMR-7 ha llamado al método DirectDraw Flip en la superficie que se presenta.           |
| [**VENTANA \_ EC \_ DESTRUYEDA**](ec-window-destroyed.md)                    | El representador de vídeo se destruyó o quitó del gráfico.                                                               |
| [**EVENTO \_ WMT \_ DE EC**](ec-wmt-event.md)                                  | Enviado por el filtro lector de ASF de WM cuando lee archivos ASF protegidos por administración de derechos digitales (DRM).                    |
| [**EVENTO \_ DE ÍNDICE WMT DE \_ \_ EC**](ec-wmt-index-event.md)                     | Se envía cuando una aplicación usa WM ASF Writer para indexar Windows archivos de vídeo multimedia.                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



