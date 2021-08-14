---
description: La clase CBaseRenderer es una clase base para implementar filtros de representador.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: CBaseRenderer (clase, Renbase.h)
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
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954814"
---
# <a name="cbaserenderer-class"></a>CBaseRenderer (clase)

![Jerarquía de clases de cbaserenderer](images/rbase02.png)

La `CBaseRenderer` clase es una clase base para implementar filtros de representador. Admite un pin de entrada, implementado por la [**clase CRendererInputPin.**](crendererinputpin.md) Para usar esta clase, declare una clase derivada que herede `CBaseRenderer` . Como mínimo, la clase derivada debe implementar los métodos siguientes, que se declaran como virtuales puros en la clase base:

-   [**CBaseRenderer::CheckMediaType:**](cbaserenderer-checkmediatype.md)acepta o rechaza los tipos de medios propuestos. El filtro llama a este método durante el proceso de conexión de pin.
-   [**CBaseRenderer::D oRenderSample:**](cbaserenderer-dorendersample.md)representa un ejemplo. El filtro llama a este método para cada ejemplo que recibe mientras se ejecuta.

La clase base controla los cambios de estado y los problemas de sincronización. También programa ejemplos para su representación, aunque no implementa ninguna medida de control de calidad. La clase base también declara varios métodos de "controlador". Estos son métodos a los que llama el filtro en puntos específicos del proceso de streaming. No hacen nada en la clase base, pero la clase derivada puede invalidarlas. En la tabla siguiente, aparecen bajo el encabezado Métodos públicos: Controladores.

El [**controlador CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) merece una mención especial. El filtro llama a este método si recibe un ejemplo mientras el filtro está en pausa. Esto puede ocurrir si el gráfico cambia de detenido a en pausa, o si se busca el gráfico mientras está en pausa. Los representadores de vídeo suelen usar el ejemplo para mostrar un fotograma todavía. Cuando el filtro cambia de en pausa a en ejecución, envía el mismo ejemplo al método [**CBaseRenderer::D oRenderSample,**](cbaserenderer-dorendersample.md) como el primer ejemplo de la secuencia.

La `CBaseRenderer` clase expone las interfaces **IMediaSeeking** e **IMediaPosition** a través del [**objeto CRendererPosPassThru.**](crendererpospassthru.md) Pasa todas las solicitudes de búsqueda al siguiente filtro ascendente.

## <a name="scheduling"></a>Scheduling

Cuando el filtro ascendente llama al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin de entrada para entregar un ejemplo, el pin pasa esta llamada al método [**CBaseRenderer::Receive**](cbaserenderer-receive.md) del filtro. El filtro quita el ejemplo, lo representa inmediatamente o lo programa para su representación.

Si el ejemplo no tiene marcas de tiempo o si no hay ningún reloj de referencia disponible, el filtro representa la muestra inmediatamente. De lo contrario, el filtro llama [**al método CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) para determinar qué hacer. De forma predeterminada, el ejemplo se programa en función de sus marcas de tiempo. La clase derivada puede invalidar **ShouldDrawSampleNow para** admitir el control de calidad.

Para programar un ejemplo, el filtro llama al método [**IReferenceClock::AdviseTime,**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) que crea una solicitud de asesoramiento. A [**continuación,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) el método Receive se bloquea hasta la hora programada o hasta que el filtro cambia de estado. El bloqueo impide que el filtro ascendente entregue más muestras hasta que se represente la muestra actual.

Cuando el filtro ascendente llama al método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) para indicar el final de la secuencia, el filtro envía un evento [**\_ EC COMPLETE**](ec-complete.md) al administrador de gráficos de filtros. El filtro espera la hora de detenerse del ejemplo actual antes de enviar el evento.



| Variables miembro protegidas                                                   | Descripción                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Marca que indica si se debe detener la representación y rechazar más ejemplos.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Marca que indica si se alcanzó el final de la secuencia.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Marca que indica si el filtro ha publicado el evento EC \_ COMPLETE.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Marca que indica si el filtro está procesando una **llamada Receive.**                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Marca que habilita o deshabilita los eventos de repintado.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Marca que indica si el filtro está transmitiendo datos.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Identificador del evento de temporizador que programa la representación.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Identificador de evento de temporizador, para programar notificaciones \_ EC COMPLETE.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Evento que se señala cuando se completa una transición de estado.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Bloqueo de estado de filtro.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Bloqueo para proteger la creación de objetos dentro del filtro.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Puntero a la patilla de entrada del filtro.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Puntero al ejemplo de medios actual.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Objeto auxiliar para pasar comandos seek ascendentes.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Puntero al objeto que recibe mensajes de control de calidad.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Bloqueo de streaming.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Evento que se usa para programar la representación.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Tiempo de detenerse en el ejemplo actual.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Evento que se usa para liberar el subproceso de streaming.                                                                                             |
| Métodos públicos                                                               | Descripción                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Cancela el evento de temporizador que programa la representación. Virtual.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Método constructor.                                                                                                                     |
| [**~CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Método destructor.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera los punteros de interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro. Virtual. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Recupera un pin. Virtual.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera el número de pines. Virtual.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera las marcas de tiempo de un ejemplo. Virtual.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Publica un [**evento EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md) en el administrador de gráficos de filtro.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Se prepara para representar un ejemplo. Virtual.                                                                                                   |
| [**Recibir**](cbaserenderer-receive.md)                                     | Recibe el siguiente ejemplo multimedia de la secuencia. Virtual.                                                                                  |
| [**Render**](cbaserenderer-render.md)                                       | Representa un ejemplo. Virtual.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Programa un ejemplo para su representación. Virtual.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifica al filtro ascendente del identificador de la ventana de vídeo.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Envía un evento de repintado al administrador de gráficos de filtro.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Se llama cuando se establece el tipo de medio del pin. Virtual.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Borra el identificador de temporizador utilizado para programar la representación.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Contiene o libera el subproceso de streaming. Virtual.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Espera a que se [**complete el método CBaseRenderer::Receive.**](cbaserenderer-receive.md)                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Espera el tiempo de presentación del ejemplo actual. Virtual.                                                                              |
| Métodos públicos: métodos de accessor                                             | Descripción                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Libera el ejemplo actual. Virtual.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Recupera el ejemplo actual. Virtual.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Recupera el estado del filtro.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Recupera el evento que programa la representación.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Determina si el filtro tiene un ejemplo. Virtual.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Consulta si se recibió la notificación de fin de flujo.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Consulta si el evento EC \_ COMPLETE se ha entregado al administrador de gráficos de filtros.                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | Consulta si el filtro está transmitiendo datos.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Establece una marca que indica si se debe detener la representación y rechazar más ejemplos.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Habilita o deshabilita los eventos de repintado.                                                                                                     |
| Métodos públicos: State-Change métodos                                         | Descripción                                                                                                                             |
| [**Activo**](cbaserenderer-active.md)                                       | Se llama cuando el estado cambia a en pausa o en ejecución. Virtual.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Comienza una operación de vaciado. Virtual.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Libera el pin de entrada de una conexión. Virtual.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Consulta si se ha completado una transición de estado.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Completa la conexión del pin de entrada a otro pin. Virtual.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Determina si se ha completado una transición al estado en pausa. Virtual.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Finaliza una operación de vaciado. Virtual.                                                                                                        |
| [**Inactivo**](cbaserenderer-inactive.md)                                   | Se llama cuando el estado cambia a detenido. Virtual.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Indica que aún no se ha completado una transición de estado.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Indica que se ha completado una transición de estado.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Inicia el streaming cuando el filtro cambia a un estado de ejecución. Virtual.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Detiene el streaming cuando el filtro sale del estado en ejecución. Virtual.                                                             |
| Métodos públicos: métodos de fin de flujo                                        | Descripción                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifica al filtro que el pin de entrada recibió una notificación de fin de flujo. Virtual.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Publica un [**evento EC \_ COMPLETE**](ec-complete.md) en el administrador de gráficos de filtros.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Restablece las marcas de fin de flujo.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Cancela el temporizador que programa las notificaciones EC \_ COMPLETE. Virtual.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Si se alcanzó el final del flujo, programa un evento EC \_ COMPLETE para el administrador de gráficos de filtro. Virtual.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Método de devolución de llamada para el evento de temporizador de fin de secuencia.                                                                                      |
| Métodos públicos: controladores                                                     | Descripción                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Se llama cuando el filtro recibe un ejemplo mientras está en pausa. Virtual.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Se llama después de representar un ejemplo. Virtual.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Se llama cuando la representación está a punto de iniciarse. Virtual.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Se llama cuando el filtro comienza la transmisión por secuencias. Virtual.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Se llama cuando el filtro deja de transmitir. Virtual.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Se llama cuando se realiza el filtro esperando el tiempo de presentación de una muestra. Virtual.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Se llama cuando el filtro comienza a esperar el tiempo de presentación de una muestra. Virtual.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Se llama antes de que el filtro represente un ejemplo. Virtual.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina cómo se programa un ejemplo para su representación. Virtual.                                                                            |
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
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




