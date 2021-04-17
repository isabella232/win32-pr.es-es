---
description: Códigos de notificación de eventos
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Códigos de notificación de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c41abc3ffc7a93a39e7a97fb210b491ad4fc58
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686425"
---
# <a name="event-notification-codes"></a>Códigos de notificación de eventos

En esta sección se enumeran los eventos de DirectShow que no son específicos de DVD. Para eventos específicos de DVD, consulte [códigos de notificación de eventos de DVD](dvd-notification-codes.md).

Los filtros envían eventos al administrador de gráficos de filtro llamando al método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) . El administrador de gráficos de filtro controla algunos eventos y pone en cola otros para la aplicación. La aplicación los recupera llamando al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) .

En las secciones siguientes, cada entrada muestra el código de evento, el significado de los parámetros de evento y la acción predeterminada del administrador de gráficos de filtro para el evento, si existe. Para invalidar la acción predeterminada, llame a [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). Los códigos de evento se definen en los archivos de encabezado Evcode. h y Audevcod. h. Si no hay ninguna acción predeterminada, el administrador de gráficos de filtro reenvía automáticamente el evento a la aplicación (a través de la cola de eventos).

**Eventos personalizados**

Los filtros pueden definir eventos personalizados con códigos de evento en el \_ usuario de rango y superior. Filter Graph Manager los colocará directamente en la cola de eventos. Sin embargo, se aplican las siguientes advertencias:

-   Filter Graph Manager no puede liberar los parámetros de evento mediante el método [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) normal. La aplicación debe liberar todos los recuentos de memoria o de referencia asociados a los parámetros de evento.
-   El filtro solo debe enviar el evento desde dentro de una aplicación preparada para controlar el evento. (Es posible que la aplicación pueda establecer una propiedad personalizada en el filtro para indicar que es seguro enviar el evento).



| Código de notificación de eventos                                                 | Descripción                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**activación de EC \_**](ec-activate.md)                                     | Una ventana de vídeo se está activando o desactivando.                                                                         |
| [**BANDWIDTHCHANGE de EC \_**](ec-bandwidthchange.md)                       | No se admite.                                                                                                            |
| [**\_datos de almacenamiento en búfer de EC \_**](ec-buffering-data.md)                        | El gráfico está almacenando en búfer datos o ha dejado de almacenar en búfer los datos.                                                               |
| [**creado por EC \_**](ec-built.md)                                           | Envía por el control de vídeo cuando se ha creado un gráfico. No se reenvía a las aplicaciones.                                     |
| [**reloj de EC \_ \_ cambiado**](ec-clock-changed.md)                          | El reloj de referencia ha cambiado.                                                                                          |
| [**reloj de EC no \_ \_ establecido**](ec-clock-unset.md)                              | El proveedor del reloj estaba desconectado.                                                                                      |
| [**\_evento CODECAPI de EC \_**](ec-codecapi-event.md)                        | Enviado por un codificador para señalar un evento de codificación.                                                                           |
| [**EC \_ completado**](ec-complete.md)                                     | Se han representado todos los datos de una secuencia determinada.                                                                      |
| [**CONTENTPROPERTY de EC \_ \_ modificado**](ec-contentproperty-changed.md)      | No se admite.                                                                                                            |
| [**\_dispositivo EC \_ perdido**](ec-device-lost.md)                              | Se quitó un dispositivo Plug and Play o vuelve a estar disponible.                                                         |
| [**visualización de EC \_ \_ modificada**](ec-display-changed.md)                      | El modo de presentación ha cambiado.                                                                                             |
| [**\_fin \_ del \_ segmento EC**](ec-end-of-segment.md)                       | Se ha alcanzado el final de un segmento.                                                                                    |
| [**RE \_ EOS en \_ breve**](ec-eos-soon.md)                                    | No se admite.                                                                                                            |
| [**\_STILLPLAYING de error de EC \_**](ec-error-stillplaying.md)                | Error de un comando asincrónico para ejecutar el gráfico.                                                                      |
| [**ERRORABORT de EC \_**](ec-errorabort.md)                                 | Se anuló una operación debido a un error.                                                                             |
| [**ERRORABORTEX de EC \_**](ec-errorabortex.md)                             | Se anuló una operación debido a un error.                                                                             |
| [**\_cambio de \_ modo \_ EXTDEVICE de EC**](ec-extdevice-mode-change.md)         | No se admite.                                                                                                            |
| [**\_archivo EC \_ cerrado**](ec-file-closed.md)                              | El archivo de origen se cerró debido a un evento inesperado.                                                                |
| [**\_pantalla completa de EC \_ perdida**](ec-fullscreen-lost.md)                      | El representador de vídeo está cambiando del modo de pantalla completa.                                                                  |
| [**gráfico de EC \_ \_ cambiado**](ec-graph-changed.md)                          | El gráfico de filtro ha cambiado.                                                                                             |
| [**longitud de EC \_ \_ cambiada**](ec-length-changed.md)                        | La longitud de un origen ha cambiado.                                                                                       |
| [**LOADSTATUS de EC \_**](ec-loadstatus.md)                                 | Notifica a la aplicación de progreso cuando se abre un archivo de red.                                                         |
| [**\_acierto de marcador de EC \_**](ec-marker-hit.md)                                | No se admite.                                                                                                            |
| [**EC \_ necesidad de \_ reiniciar**](ec-need-restart.md)                            | Un filtro solicita que el gráfico se reinicie.                                                                       |
| [**\_nuevo \_ PIN EC**](ec-new-pin.md)                                      | No se admite.                                                                                                            |
| [**\_ventana notificación de EC \_**](ec-notify-window.md)                          | Notifica a un filtro la ventana del representador de vídeo.                                                                         |
| [**\_evento OLE de EC \_**](ec-ole-event.md)                                  | Un filtro está pasando una cadena de texto a la aplicación.                                                                     |
| [**\_archivo de apertura de EC \_**](ec-opening-file.md)                            | El gráfico está abriendo un archivo o ha terminado de abrir un archivo.                                                              |
| [**paleta de EC \_ \_ modificada**](ec-palette-changed.md)                      | La paleta de vídeo ha cambiado.                                                                                            |
| [**EC en \_ pausa**](ec-paused.md)                                         | Se ha completado una solicitud de pausa.                                                                                            |
| [**EC \_ vuelva a \_ abrirlo**](ec-please-reopen.md)                          | El archivo de código fuente ha cambiado.                                                                                              |
| [**preprocesamiento de EC \_ \_ completado**](ec-preprocess-complete.md)              | Enviado por el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) cuando completa el procesamiento previo para la codificación Multipass. |
| [**\_latencia de procesamiento de EC \_**](ec-processing-latency.md)                | Indica la cantidad de tiempo que un componente está tomando para procesar cada ejemplo.                                           |
| [**\_cambio de calidad de EC \_**](ec-quality-change.md)                        | El gráfico está quitando ejemplos para el control de calidad.                                                                       |
| [**representación de EC \_ \_ finalizada**](ec-render-finished.md)                      | No se admite.                                                                                                            |
| [**repintar EC \_**](ec-repaint.md)                                       | Un representador de vídeo requiere volver a pintar.                                                                                      |
| [**\_latencia de ejemplo de EC \_**](ec-sample-latency.md)                        | Especifica la distancia de programación de un componente para el procesamiento de muestras.                                                  |
| [**ejemplo de EC \_ \_ necesario**](ec-sample-needed.md)                          | Solicita un nuevo ejemplo de entrada del filtro de representador de vídeo mejorado (EVR).                                                |
| [**\_hora de limpieza de EC \_**](ec-scrub-time.md)                                | Especifica la marca de tiempo para el paso más reciente del marco.                                                                  |
| [**segmento de EC \_ \_ iniciado**](ec-segment-started.md)                      | Se ha iniciado un nuevo segmento.                                                                                                |
| [**\_cierre de EC \_**](ec-shutting-down.md)                          | El gráfico de filtro se está cerrando antes de ser destruido.                                                              |
| [**\_ \_ error de SNDDEV de EC \_**](ec-snddev-in-error.md)                     | Se ha producido un error de dispositivo en un filtro de captura de audio.                                                                   |
| [**\_error de SNDDEV de \_ salida de EC \_**](ec-snddev-out-error.md)                   | Se ha producido un error de dispositivo en un filtro de representador de audio.                                                                  |
| [**colapso de EC \_**](ec-starvation.md)                                 | Un filtro no recibe suficientes datos.                                                                                    |
| [**\_cambio de estado de EC \_**](ec-state-change.md)                            | El gráfico de filtro ha cambiado de estado.                                                                                       |
| [**Estado de EC \_**](ec-status.md)                                         | Contiene dos cadenas de estado arbitrarias.                                                                                    |
| [**\_finalización del paso de EC \_**](ec-step-complete.md)                          | Un filtro que realiza la ejecución de fotogramas ha escalonado el número especificado de fotogramas.                                            |
| [**CONTROL de secuencia de EC \_ \_ \_ iniciado**](ec-stream-control-started.md)       | Un comando de inicio de control de secuencia ha surtido efecto.                                                                          |
| [**CONTROL de secuencia de EC \_ \_ \_ detenido**](ec-stream-control-stopped.md)       | Un comando de detención del control de secuencias ha surtido efecto.                                                                           |
| [**\_STILLPLAYING de \_ error de secuencia de EC \_**](ec-stream-error-stillplaying.md) | Se ha producido un error en una secuencia. La secuencia todavía se está reproduciendo.                                                           |
| [**ERROR de flujo de EC \_ \_ \_ detenido**](ec-stream-error-stopped.md)           | Se ha detenido un flujo debido a un error.                                                                                 |
| [**código de acceso de EC \_ \_ disponible**](ec-timecode-available.md)                | No se admite.                                                                                                            |
| [**EC no \_ compilado**](ec-unbuilt.md)                                       | Enviar por el control de vídeo cuando se ha anulado un gráfico. No se reenvía a las aplicaciones.                                 |
| [**USERABORT de EC \_**](ec-userabort.md)                                   | El usuario ha terminado la reproducción.                                                                                         |
| [**tamaño de vídeo de EC \_ \_ \_ cambiado**](ec-video-size-changed.md)               | El tamaño de vídeo nativo ha cambiado.                                                                                        |
| [**VIDEOFRAMEREADY de EC \_**](ec-videoframeready.md)                       | Un fotograma de vídeo está listo para mostrarse.                                                                                       |
| [**\_error de \_ reconexión de VMR de EC \_**](ec-vmr-reconnection-failed.md)     | Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico del descodificador de nivel superior.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ set**](ec-vmr-renderdevice-set.md)           | Se envía cuando VMR ha seleccionado su mecanismo de representación.                                                                   |
| [**\_superficie EC \_ VMR \_ volteada**](ec-vmr-surface-flipped.md)             | Se envía cuando el presentador del asignador VMR-7's ha llamado al método Flip de DirectDraw en la superficie que se está presentando.           |
| [**ventana de EC \_ \_ destruida**](ec-window-destroyed.md)                    | El representador de vídeo se ha destruido o quitado del gráfico.                                                               |
| [**\_evento WMT de EC \_**](ec-wmt-event.md)                                  | Enviado por el filtro de lector ASF de WM cuando lee archivos ASF protegidos por la administración de derechos digitales (DRM).                    |
| [**\_evento de \_ Índice \_ WMT de EC**](ec-wmt-index-event.md)                     | Se envía cuando una aplicación utiliza el escritor ASF de WM para indizar Windows Media Video archivos.                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



