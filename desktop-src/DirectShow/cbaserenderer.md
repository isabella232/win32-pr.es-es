---
description: La clase CBaseRenderer es una clase base para implementar filtros de representador.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Clase CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e30bae52cf5a7eba642354d002173291cb7d38b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670690"
---
# <a name="cbaserenderer-class"></a>Clase CBaseRenderer

![jerarquía de clases cbaserenderer](images/rbase02.png)

La `CBaseRenderer` clase es una clase base para implementar filtros de representador. Admite un PIN de entrada, implementado por la clase [**CRendererInputPin**](crendererinputpin.md) . Para usar esta clase, declare una clase derivada que herede `CBaseRenderer` . Como mínimo, la clase derivada debe implementar los métodos siguientes, que se declaran como virtuales puras en la clase base:

-   [**CBaseRenderer:: CheckMediaType**](cbaserenderer-checkmediatype.md): acepta o rechaza los tipos de medios propuestos. El filtro llama a este método durante el proceso de conexión del PIN.
-   [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md): representa un ejemplo. El filtro llama a este método para cada ejemplo que recibe durante la ejecución.

La clase base controla los cambios de estado y los problemas de sincronización. También programa ejemplos de representación, aunque no implementa ninguna medida de control de calidad. La clase base también declara varios métodos de "controlador". Son métodos a los que el filtro llama en puntos específicos del proceso de streaming. No hacen nada en la clase base, pero la clase derivada puede invalidarlos. En la tabla siguiente, se enumeran bajo el encabezado métodos públicos: Controladores.

El controlador [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) merece mención especial. El filtro llama a este método si recibe un ejemplo mientras el filtro está en pausa. Esto puede ocurrir si el gráfico cambia de detenido a en pausa, o si se busca en el gráfico mientras está en pausa. Los representadores de vídeo suelen usar el ejemplo para mostrar un marco fijo. Cuando el filtro cambia de pausado a en ejecución, envía el mismo ejemplo al método [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , como el primer ejemplo de la secuencia.

La `CBaseRenderer` clase expone las interfaces **IMediaSeeking** y **IMediaPosition** a través del objeto [**CRendererPosPassThru**](crendererpospassthru.md) . Pasa todas las solicitudes de búsqueda al siguiente filtro ascendente.

## <a name="scheduling"></a>Scheduling

Cuando el filtro de nivel superior llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN de entrada para ofrecer un ejemplo, el PIN pasa esta llamada al método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro. El filtro quita el ejemplo, lo representa inmediatamente o lo programa para su representación.

Si el ejemplo no tiene marcas de tiempo, o si no hay ningún reloj de referencia disponible, el filtro representa el ejemplo inmediatamente. De lo contrario, el filtro llama al método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) para determinar qué hacer. De forma predeterminada, el ejemplo se programa en función de sus marcas de tiempo. La clase derivada puede invalidar **ShouldDrawSampleNow** para admitir el control de calidad.

Para programar un ejemplo, el filtro llama al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , que crea una solicitud de notificación. A continuación, el método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) se bloquea hasta la hora programada o hasta que el filtro cambia el estado. El bloqueo impide que el filtro de nivel superior entregue más muestras hasta que se represente el ejemplo actual.

Cuando el filtro de nivel superior llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) para indicar el final de la secuencia, el filtro envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro. El filtro espera la hora de detención del ejemplo actual antes de enviar el evento.



| Variables de miembro protegidas                                                   | Descripción                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Marca que indica si se debe detener la representación y rechazar más ejemplos.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Marca que indica si se ha alcanzado el final de la secuencia.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Marca que indica si el filtro ha publicado el \_ evento de finalización de EC.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Marca que indica si el filtro está procesando una llamada de **recepción** .                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Marca que habilita o deshabilita los eventos Repaint.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Marca que indica si el filtro es un flujo de datos.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Identificador del evento de temporizador que programa la representación.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Temporizador: identificador de evento, para programar \_ notificaciones completas de EC.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Evento que se señala cuando se completa una transición de estado.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Bloqueo de estado de filtro.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Bloqueo para proteger la creación de objetos dentro del filtro.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Puntero al pin de entrada del filtro.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Puntero al ejemplo multimedia actual.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Objeto auxiliar para pasar comandos de búsqueda ascendentes.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Puntero al objeto que recibe los mensajes de control de calidad.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Bloqueo de streaming.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Evento utilizado para programar la representación.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Hora de detención en el ejemplo actual.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Evento que se usa para liberar el subproceso de streaming.                                                                                             |
| Métodos públicos                                                               | Descripción                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Cancela el evento de temporizador que programa la representación. Virtualiza.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Método de constructor.                                                                                                                     |
| [**~ CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Método de destructor.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera los punteros de interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro. Virtualiza. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Recupera un código PIN. Virtualiza.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera el número de clavijas. Virtualiza.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera las marcas de tiempo de un ejemplo. Virtualiza.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Envía un evento de visualización de la [**\_ \_ vista EC**](ec-display-changed.md) al administrador de gráficos de filtro.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Prepara para representar un ejemplo. Virtualiza.                                                                                                   |
| [**Aparecen**](cbaserenderer-receive.md)                                     | Recibe el siguiente ejemplo multimedia en la secuencia. Virtualiza.                                                                                  |
| [**Representar**](cbaserenderer-render.md)                                       | Representa un ejemplo. Virtualiza.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Programa un ejemplo para la representación. Virtualiza.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifica al filtro de nivel superior el identificador de la ventana de vídeo.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Envía un evento Repaint al administrador de gráficos de filtro.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Se le llama cuando se establece el tipo de medio del PIN. Virtualiza.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Borra el identificador del temporizador que se usa para programar la representación.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Contiene o libera el subproceso de streaming. Virtualiza.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Espera a que se complete el método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Espera el tiempo de presentación del ejemplo actual. Virtualiza.                                                                              |
| Métodos públicos: métodos de descriptor de acceso                                             | Descripción                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Libera el ejemplo actual. Virtualiza.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Recupera el ejemplo actual. Virtualiza.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Recupera el estado del filtro.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Recupera el evento que programa la representación.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Determina si el filtro tiene un ejemplo. Virtualiza.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Consulta si se ha recibido la notificación de final de secuencia.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Consulta si el evento de finalización de EC se ha \_ entregado al administrador de gráficos de filtro.                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | Consulta si el filtro es un flujo de datos.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Establece una marca que indica si se debe detener la representación y rechazar más ejemplos.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Habilita o deshabilita los eventos Repaint.                                                                                                     |
| Métodos públicos: métodos de State-Change                                         | Descripción                                                                                                                             |
| [**Activo**](cbaserenderer-active.md)                                       | Se llama cuando el estado cambia a en pausa o en ejecución. Virtualiza.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Comienza una operación de vaciado. Virtualiza.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Libera el PIN de entrada de una conexión. Virtualiza.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Consulta si se ha completado una transición de estado.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Completa la conexión del PIN de entrada con otro PIN. Virtualiza.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Determina si se ha completado una transición al estado en pausa. Virtualiza.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Finaliza una operación de vaciado. Virtualiza.                                                                                                        |
| [**Inactivo**](cbaserenderer-inactive.md)                                   | Se llama cuando el estado cambia a detenido. Virtualiza.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Indica que aún no se ha completado una transición de estado.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Indica que se ha completado una transición de estado.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Inicia el streaming cuando el filtro cambia a un estado de ejecución. Virtualiza.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Detiene el streaming cuando el filtro sale del estado de ejecución. Virtualiza.                                                             |
| Métodos públicos: métodos de final de secuencia                                        | Descripción                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifica al filtro que el PIN de entrada recibió una notificación de final de secuencia. Virtualiza.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Publica un evento de [**\_ finalización de EC**](ec-complete.md) en el administrador de gráficos de filtro.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Restablece las marcas de fin de secuencia.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Cancela el temporizador que programa las \_ notificaciones completas de EC. Virtualiza.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Si se ha alcanzado el final de la secuencia, programa un \_ evento EC complete para el administrador de gráficos de filtro. Virtualiza.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Método de devolución de llamada para el evento de temporizador de final de secuencia.                                                                                      |
| Métodos públicos: Controladores                                                     | Descripción                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Se llama cuando el filtro recibe un ejemplo mientras está en pausa. Virtualiza.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Se llama después de representar un ejemplo. Virtualiza.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Se llama cuando la representación está a punto de iniciarse. Virtualiza.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Se llama cuando el filtro comienza el streaming. Virtualiza.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Se llama cuando el filtro detiene el streaming. Virtualiza.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Se llama cuando el filtro se realiza en espera de un tiempo de presentación de un ejemplo. Virtualiza.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Se llama cuando el filtro empieza a esperar el tiempo de presentación de un ejemplo. Virtualiza.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Se llama antes de que el filtro represente un ejemplo. Virtualiza.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina cómo se programa un ejemplo para su representación. Virtualiza.                                                                            |
| Métodos virtuales puros                                                         | Descripción                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Determina si el filtro acepta un tipo de medio específico.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Representa un ejemplo.                                                                                                                       |
| Métodos IMediaFilter                                                         | Descripción                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Recupera el estado del filtro (en ejecución, detenido o en pausa).                                                                             |
| [**Pausar**](cbaserenderer-pause.md)                                         | Pausa el filtro.                                                                                                                      |
| [**Ejecutar**](cbaserenderer-run.md)                                             | Ejecuta el filtro.                                                                                                                        |
| [**Stop**](cbaserenderer-stop.md)                                           | Detiene el filtro.                                                                                                                       |
| Métodos IBaseFilter                                                          | Descripción                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Recupera el pin con el identificador especificado.                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




