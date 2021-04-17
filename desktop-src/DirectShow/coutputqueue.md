---
description: La clase COutputQueue implementa una cola para proporcionar ejemplos de medios.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Clase COutputQueue (Outputq. h)
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
ms.openlocfilehash: cd6167402abd36db8f436f6e27b18213642f010b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680380"
---
# <a name="coutputqueue-class"></a>Clase COutputQueue

![coutputqueue](images/oput01.png)

La `COutputQueue` clase implementa una cola para proporcionar ejemplos de medios.

Esta clase permite que un PIN de salida entregue ejemplos de forma asincrónica. Los ejemplos se colocan en una cola y un subproceso de trabajo los entrega al pin de entrada. La cola también puede contener mensajes de control que indican un nuevo segmento, una notificación de final de secuencia o una operación de vaciado.

Para usar esta clase, cree un objeto **COutputQueue** para cada pin de salida del filtro. En el método de constructor, especifique el PIN de entrada conectado a ese pin de salida. Con esta clase, el PIN de salida no llama a los métodos directamente en el PIN de entrada. En su lugar, llama a los métodos correspondientes en `COutputQueue` , como se muestra en la tabla siguiente.



| PIN (método)                                                            | Método COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**OCASIONA**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Aparecen**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Opcionalmente, puede configurar el `COutputQueue` objeto para ofrecer ejemplos de forma sincrónica, sin un subproceso de trabajo. El objeto también puede decidir en tiempo de ejecución si se debe usar un subproceso de trabajo, en función de las características del terminal de entrada. Para obtener más información, vea [**COutputQueue:: COutputQueue**](coutputqueue-coutputqueue.md).



| Variables de miembro protegidas                                   | Descripción                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN de entrada.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Marca que especifica si el objeto proporciona ejemplos en lotes exactos.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Tamaño del lote.                                                                                              |
| [**\_lista m**](coutputqueue-m-list.md)                       | Cola de ejemplo multimedia.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Identificador de un semáforo, utilizado por el subproceso para esperar ejemplos.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Evento que indica cuándo ha finalizado una operación de vaciado.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Identificador del subproceso de trabajo.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Matriz de ejemplos de tamaño [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Número de muestras actualmente por lotes y en espera de procesamiento.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Marca que tiene un valor distinto de cero cuando el subproceso está esperando un ejemplo.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Marca que especifica si el objeto está realizando una operación de vaciado.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Marca que especifica si el subproceso debe finalizar.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Marca para invalidar el procesamiento por lotes.                                                                       |
| [**m \_ .**](coutputqueue-m-hr.md)                           | Valor **HRESULT** que indica si el objeto aceptará ejemplos.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Evento que se señala cuando el objeto quita un ejemplo de la cola.                              |
| Métodos protegidos                                            | Descripción                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Llama al método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) cuando se crea el subproceso. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Recupera ejemplos de la cola y los entrega al pin de entrada.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Determina si el objeto está utilizando un subproceso de trabajo para proporcionar ejemplos.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Pone en cola un mensaje de control o de ejemplo multimedia.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina si los datos en cola son un mensaje de control.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera todas las muestras pendientes.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica al subproceso que la cola contiene datos.                                                        |
| Métodos públicos                                               | Descripción                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Método de constructor.                                                                                      |
| [**~ COutputQueue**](coutputqueue--coutputqueue.md)          | Método de destructor.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Comienza una operación de vaciado.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Finaliza una operación de vaciado.                                                                                  |
| [**OCASIONA**](coutputqueue-eos.md)                              | Entrega una llamada de final de secuencia al pin de entrada.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Entrega cualquier ejemplo pendiente.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Entrega un nuevo segmento al pin de entrada.                                                                 |
| [**Aparecen**](coutputqueue-receive.md)                      | Entrega un ejemplo multimedia al pin de entrada.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Entrega un lote de muestras de medios al pin de entrada.                                                      |
| [**Reset**](coutputqueue-reset.md)                          | Restablece el objeto para que pueda recibir más datos.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina si el objeto está esperando los datos.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Especifica un evento que se señaliza cada vez que el objeto quita un ejemplo de la cola.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




