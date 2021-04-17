---
description: La clase CDynamicOutputPin implementa un PIN de salida que admite reconexiones dinámicas y cambios de formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Clase CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c6dab41c122456076299df22bf90d886c905cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660871"
---
# <a name="cdynamicoutputpin-class"></a>Clase CDynamicOutputPin

La `CDynamicOutputPin` clase implementa un PIN de salida que admite reconexiones dinámicas y cambios de formato.

Esta clase se deriva de la clase [**CBaseOutputPin**](cbaseoutputpin.md) e implementa la interfaz [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Admite varias operaciones que son importantes para la creación de gráficos dinámicos:

-   Reconexión dinámica: el pin puede desconectarse y volver a conectarse mientras el filtro sigue activo (en pausa o en ejecución).
-   Cambio de formato dinámico: el pin puede negociar un nuevo tipo de medio mientras el filtro sigue activo, sin volver a conectarse.
-   Control de flujo: el filtro propietario (o una aplicación) puede bloquear el flujo de datos desde el código PIN sin detener el filtro.

Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md).

El pin tiene tres Estados posibles: bloqueado, desbloqueado y pendiente. En el estado *pendiente* , el PIN está esperando a que se complete una operación en otro subproceso, antes de que el PIN cambie al estado bloqueado. Mientras el PIN está bloqueado, el filtro no puede enviar datos a través del PIN ni cambiar la conexión del PIN.

Para coordinarse entre varios subprocesos, el filtro propietario debe cumplir ciertas reglas. (Para obtener más información sobre los subprocesos en el gráfico de filtros, vea [subprocesos y secciones críticas](threads-and-critical-sections.md)). En primer lugar, el subproceso de streaming debe llamar siempre al método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a cualquiera de los métodos siguientes:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Después, debe llamar al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .

En segundo lugar, el subproceso de aplicación no debe llamar a ninguno de los métodos de la lista anterior. En tercer lugar, el subproceso de streaming no debe llamar a los métodos de clase que bloquean o desbloquean el código PIN. Estos métodos son: [**CDynamicOutputPin:: Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)y [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Estas reglas garantizan que el subproceso de la aplicación no puede bloquear el PIN mientras el subproceso de streaming lo está usando y viceversa. Después de que el subproceso de streaming haya llamado a **StartUsingOutputPin**, el PIN no se bloqueará hasta que el subproceso de streaming llame a **StopUsingOutputPin**. Por el contrario, si el PIN está bloqueado, **StartUsingOutputPin** espera hasta que se desbloquea el PIN.

Para evitar la llamada a **StopUsingOutputPin**, puede usar la clase [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) . Llama automáticamente a **StopUsingOutputPin** cuando sale del ámbito.

Cuando el filtro propietario combina o leaveds el gráfico de filtro (en su método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) ), debe llamar al método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) del PIN.



| Variables de miembro protegidas                                                                      | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Sección crítica que protege el estado de bloqueo.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento que se señala cuando el PIN no está bloqueado.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento que se señala cuando el PIN se bloquea correctamente o el usuario cancela un bloque pendiente.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | Estado de bloqueo.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | El identificador del subproceso que llamó por última vez al método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en este pin. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Número de subprocesos de streaming con este pin.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento que se señala cuando se detiene el filtro o el PIN vacía los datos.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Puntero a la interfaz [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) para realizar reconexiones dinámicas.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Marca que especifica si los ejemplos del asignador del PIN son de solo lectura.                                                   |
| Métodos protegidos                                                                               | Descripción                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Bloquea el PIN; no devuelve ningún resultado hasta que se bloquea el PIN.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Bloquea el PIN; podría devolver antes de que se bloquee el PIN.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Desbloquea el código PIN.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Bloquea el PIN.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Espera hasta que se señale el evento especificado.                                                                                  |
| Métodos públicos                                                                                  | Descripción                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Método de constructor.                                                                                                           |
| [**~ CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Método de destructor.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Especifica el puntero [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y el evento STOP.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Solicita la clavija de entrada conectada para iniciar una operación de vaciado.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Solicita la clavija de entrada conectada para finalizar una operación de vaciado.                                                                    |
| [**Inactivo**](cdynamicoutputpin-inactive.md)                                                  | Notifica al pin que el filtro se ha detenido.                                                                                 |
| [**Active**](cdynamicoutputpin-active.md)                                                      | Notifica al pin que el filtro está activo ahora.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Completa una conexión a un PIN de entrada. Virtualiza.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Obtiene acceso al pin para una operación de streaming. Virtualiza.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Libera el acceso al pin después de una operación de streaming. Virtualiza.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina si algún subproceso está realizando una operación de transmisión por secuencias en el código PIN. Virtualiza.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Cambia de forma dinámica el tipo de medio para la conexión y proporciona información de nuevo segmento.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Cambia dinámicamente el tipo de medio para la conexión.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Realiza una reconexión dinámica con un nuevo tipo de medio.                                                                        |
| Métodos IPin                                                                                    | Descripción                                                                                                                   |
| [**Desconectar**](cdynamicoutputpin-disconnect.md)                                              | Interrumpe la conexión del PIN actual.                                                                                            |
| Métodos IPinFlowControl                                                                         | Descripción                                                                                                                   |
| [**Block**](cdynamicoutputpin-block.md)                                                        | Bloquea o desbloquea el flujo de datos desde el código PIN.                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




