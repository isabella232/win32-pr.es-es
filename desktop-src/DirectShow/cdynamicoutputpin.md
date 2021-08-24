---
description: La clase CDynamicOutputPin implementa un pin de salida que admite reconexiones dinámicas y cambios de formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: CDynamicOutputPin (clase, Amfilter.h)
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
ms.openlocfilehash: 6e0b8903f83c372aa85bd1c41fb12ce9065798d79dc4dbd940df926a395f8bc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871805"
---
# <a name="cdynamicoutputpin-class"></a>CDynamicOutputPin (clase)

La `CDynamicOutputPin` clase implementa un pin de salida que admite reconexiones dinámicas y cambios de formato.

Esta clase se deriva de la [**clase CBaseOutputPin**](cbaseoutputpin.md) e implementa la [**interfaz IPinFlowControl.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Admite varias operaciones que son importantes para la creación dinámica de grafos:

-   Reconexión dinámica: el pin puede desconectarse y volver a conectarse mientras el filtro sigue activo (en pausa o en ejecución).
-   Cambio de formato dinámico: el pin puede negociar un nuevo tipo de medio mientras el filtro sigue activo, sin volver a conectarse.
-   Flow control: el filtro propietario (o una aplicación) puede bloquear el flujo de datos desde el pin sin detener el filtro.

Para obtener más información, vea [Dynamic Graph Building](dynamic-graph-building.md).

El pin tiene tres estados posibles: bloqueado, desbloqueado y pendiente. En el *estado pendiente,* el pin está esperando a que se complete alguna operación en otro subproceso, antes de que el pin pase al estado bloqueado. Mientras el pin está bloqueado, el filtro no puede entregar datos a través del pin ni cambiar la conexión del pin.

Para coordinar entre varios subprocesos, el filtro propietario debe seguir ciertas reglas. (Para obtener más información sobre los subprocesos en el gráfico de filtros, vea [Subprocesos y secciones críticas).](threads-and-critical-sections.md) En primer lugar, el subproceso de streaming siempre debe llamar al método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a cualquiera de los métodos siguientes:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Después, debe llamar al [**método CDynamicOutputPin::StopUsingOutputPin.**](cdynamicoutputpin-stopusingoutputpin.md)

En segundo lugar, el subproceso de aplicación no debe llamar a ninguno de los métodos de la lista anterior. En tercer lugar, el subproceso de streaming no debe llamar a los métodos de clase que bloquean o desbloquean el pin. Estos métodos son: [**CDynamicOutputPin::Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin::SynchronousBlockOutputPin,**](cdynamicoutputpin-synchronousblockoutputpin.md) [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)y [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Estas reglas garantizan que el subproceso de aplicación no puede bloquear el pin mientras el subproceso de streaming lo usa, y viceversa. Después de que el subproceso de streaming haya llamado **a StartUsingOutputPin,** el pin no se bloqueará hasta que el subproceso de streaming llame a **StopUsingOutputPin**. Por el contrario, si el pin está bloqueado, **StartUsingOutputPin** espera hasta que se desbloquea el pin.

Para evitar el abandono de llamar a **StopUsingOutputPin,** puede usar la [**clase CAutoUsingOutputPin.**](cautousingoutputpin-cautousingoutputpin.md) Llama a **StopUsingOutputPin** automáticamente cuando sale del ámbito.

Cuando el filtro propietario une o deja el gráfico de filtro (en su método [**IBaseFilter::JoinFilterGraph),**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) debe llamar al método [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) del pin.



| Variables de miembro protegido                                                                      | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Sección crítica que protege el estado de bloqueo.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento que se señala cuando el pin no está bloqueado.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento que se señala cuando el pin se bloquea correctamente o el usuario cancela un bloque pendiente.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | Estado de bloqueo.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Identificador del subproceso que llamó por última vez al [**método IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en este pin. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Número de subprocesos de streaming mediante este pin.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento que se señala cuando el filtro se detiene o el pin vacía los datos.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Puntero a la [**interfaz IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) para realizar reconexiones dinámicas.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Marca que especifica si los ejemplos del asignador del pin son de solo lectura.                                                   |
| Métodos protegidos                                                                               | Descripción                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Bloquea el pin; no devuelve hasta que se bloquea el pin.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Bloquea el pin; puede devolver antes de que se bloquee el pin.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Desbloquea el pin.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Bloquea el pin.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Espera hasta que se señala el evento especificado.                                                                                  |
| Métodos públicos                                                                                  | Descripción                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Método constructor.                                                                                                           |
| [**~CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Método destructor.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Especifica el puntero [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y el evento stop.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Solicita el pin de entrada conectado para iniciar una operación de vaciado.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Solicita el pin de entrada conectado para finalizar una operación de vaciado.                                                                    |
| [**Inactivo**](cdynamicoutputpin-inactive.md)                                                  | Notifica al pin que el filtro se ha detenido.                                                                                 |
| [**Activo**](cdynamicoutputpin-active.md)                                                      | Notifica al pin que el filtro ahora está activo.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Completa una conexión a un pin de entrada. Virtual.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Obtiene acceso al pin para una operación de streaming. Virtual.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Libera el acceso al pin después de una operación de streaming. Virtual.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina si algún subproceso está realizando una operación de streaming en el pin. Virtual.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Cambia dinámicamente el tipo de medio para la conexión y proporciona información de segmento nuevo.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Cambia dinámicamente el tipo de medio para la conexión.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Realiza una reconexión dinámica con un nuevo tipo de medio.                                                                        |
| Métodos de IPin                                                                                    | Descripción                                                                                                                   |
| [**Desconectar**](cdynamicoutputpin-disconnect.md)                                              | Interrumpe la conexión de pin actual.                                                                                            |
| Métodos IPinFlowControl                                                                         | Descripción                                                                                                                   |
| [**Block**](cdynamicoutputpin-block.md)                                                        | Bloquea o desbloquea el flujo de datos del pin.                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




