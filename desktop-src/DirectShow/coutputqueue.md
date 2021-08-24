---
description: La clase COutputQueue implementa una cola para entregar ejemplos multimedia.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: COutputQueue (clase, Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8911c7261af0bf2e140a551b0146b7764cd541368898e6d3905f5dee2eaa4c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813445"
---
# <a name="coutputqueue-class"></a>COutputQueue (clase)

![coutputqueue](images/oput01.png)

La `COutputQueue` clase implementa una cola para entregar ejemplos multimedia.

Esta clase permite que un pin de salida entregue muestras de forma asincrónica. Los ejemplos se colocan en una cola y un subproceso de trabajo los entrega al pin de entrada. La cola también puede contener mensajes de control que indican un nuevo segmento, una notificación de fin de flujo o una operación de vaciado.

Para usar esta clase, cree un **objeto COutputQueue** para cada pin de salida del filtro. En el método del constructor, especifique el pin de entrada conectado a ese pin de salida. Con esta clase, el pin de salida no llama a los métodos directamente en el pin de entrada. En su lugar, llama a los métodos correspondientes en `COutputQueue` , como se muestra en la tabla siguiente.



| Pin (método)                                                            | COutputQueue (método)                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Eos**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Recibir**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Opcionalmente, puede configurar el objeto `COutputQueue` para entregar ejemplos de forma sincrónica, sin un subproceso de trabajo. El objeto también puede decidir en tiempo de ejecución si se debe usar un subproceso de trabajo, en función de las características del pin de entrada. Para obtener más información, [**vea COutputQueue::COutputQueue**](coutputqueue-coutputqueue.md).



| Variables de miembro protegido                                   | Descripción                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del pin de entrada.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Marca que especifica si el objeto entrega muestras en lotes exactos.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Tamaño del lote.                                                                                              |
| [**m \_ List**](coutputqueue-m-list.md)                       | Cola de ejemplo multimedia.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Controlar un semáforo, utilizado por el subproceso para esperar muestras.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Evento que indica cuándo ha finalizado una operación de vaciado.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Identificador del subproceso de trabajo.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Matriz de ejemplos de tamaño [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Número de muestras actualmente por lotes y en espera de procesamiento.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Marca que tiene un valor distinto de cero cuando el subproceso está esperando un ejemplo.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Marca que especifica si el objeto está realizando una operación de vaciado.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Marca que especifica si el subproceso debe finalizar.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Marca para invalidar el procesamiento por lotes.                                                                       |
| [**m \_ hr**](coutputqueue-m-hr.md)                           | **Valor HRESULT** que indica si el objeto aceptará muestras.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Evento que se señala cada vez que el objeto quita un ejemplo de la cola.                              |
| Métodos protegidos                                            | Descripción                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Llama al [**método COutputQueue::ThreadProc**](coutputqueue-threadproc.md) cuando se crea el subproceso. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Recupera ejemplos de la cola y los entrega al pin de entrada.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Determina si el objeto usa un subproceso de trabajo para entregar ejemplos.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Pone en cola un ejemplo multimedia o un mensaje de control.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina si los datos en cola son un mensaje de control.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera todos los ejemplos pendientes.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica al subproceso que la cola contiene datos.                                                        |
| Métodos públicos                                               | Descripción                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Método constructor.                                                                                      |
| [**~COutputQueue**](coutputqueue--coutputqueue.md)          | Método destructor.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Comienza una operación de vaciado.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Finaliza una operación de vaciado.                                                                                  |
| [**Eos**](coutputqueue-eos.md)                              | Entrega una llamada de fin de flujo al pin de entrada.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Entrega los ejemplos pendientes.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Entrega un nuevo segmento al pin de entrada.                                                                 |
| [**Recibir**](coutputqueue-receive.md)                      | Entrega un ejemplo multimedia al pin de entrada.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Entrega un lote de muestras multimedia al pin de entrada.                                                      |
| [**Restablecer**](coutputqueue-reset.md)                          | Restablece el objeto para que pueda recibir más datos.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina si el objeto está esperando datos.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Especifica un evento que se señala cada vez que el objeto quita un ejemplo de la cola.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




