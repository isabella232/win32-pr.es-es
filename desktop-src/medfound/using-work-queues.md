---
description: En este tema se describe cómo usar las colas de trabajos en Microsoft Media Foundation.
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: Uso de colas de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275809"
---
# <a name="using-work-queues"></a>Uso de colas de trabajo

En este tema se describe cómo usar las colas de trabajos en Microsoft Media Foundation.

-   [Uso de colas de trabajo](#using-work-queues)
-   [Cerrando colas de trabajo](#shutting-down-work-queues)
-   [Usar elementos de trabajo programados](#using-scheduled-work-items)
-   [Usar devoluciones de llamada periódicas](#using-periodic-callbacks)
-   [Temas relacionados](#related-topics)

## <a name="using-work-queues"></a>Uso de colas de trabajo

Una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso. Conceptualmente, los elementos de trabajo se colocan en la cola y la cola tiene un subproceso que extrae cada elemento de la cola y lo envía. Los elementos de trabajo se implementan como devoluciones de llamada mediante la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .

Media Foundation crea varias colas de trabajo estándar, denominadas *colas de trabajo de plataforma*. Las aplicaciones también pueden crear sus propias colas de trabajo, denominadas *colas de trabajo privadas*. Para obtener una lista de las colas de trabajo de la plataforma, vea [identificadores de cola de trabajo](work-queue-identifiers.md). Para crear una cola de trabajo privada, llame a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Esta función devuelve un identificador para la nueva cola de trabajo. Para colocar un elemento en la cola, llame a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). En ambos casos, debe especificar una interfaz de devolución de llamada.

-   [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) toma un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , además de un objeto de estado opcional que implementa **IUnknown**. Estos son los mismos parámetros que se usan en métodos asincrónicos, como se describe en el tema [métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md). Internamente, esta función crea un objeto de resultado asincrónico, que se pasa al método de [**invocación**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la devolución de llamada.
-   [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) toma un puntero a la interfaz [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Esta interfaz representa un objeto de resultado asincrónico. Cree este objeto llamando a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) y especificando la interfaz de devolución de llamada y, opcionalmente, un objeto de estado.

En ambos casos, el subproceso de la cola de trabajo llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Use el método **Invoke** para realizar el elemento de trabajo.

Si más de un subproceso o componente comparte la misma cola de trabajo, puede llamar a [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) para bloquear la cola de trabajo, lo que evita que la plataforma la libere. Para cada llamada a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) o **MFLockWorkQueue**, debe llamar a [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) una vez para liberar la cola de trabajo. Por ejemplo, si crea una nueva cola de trabajo y, a continuación, la bloquea una vez, debe llamar a **MFUnlockWorkQueue** dos veces, una vez para la llamada a **MFAllocateWorkQueue** y otra para la llamada a **MFLockWorkQueue**.

El código siguiente muestra cómo crear una nueva cola de trabajo, colocar un elemento de trabajo en la cola y liberar la cola de trabajo.

Consulte [mejoras en la cola de trabajo y el subproceso](media-foundation-work-queue-and-threading-improvements.md) para obtener información adicional sobre las colas de trabajos en Windows 8.


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



En este ejemplo se da por supuesto que *pCallback* es un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de la aplicación. También se supone que la devolución de llamada establece el identificador de evento *hEvent* . El código espera a que se establezca este evento antes de llamar a [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue).

Los subprocesos de la cola de trabajo siempre se crean en el proceso del llamador. En cada cola de trabajo, las devoluciones de llamada se serializan. Si llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) dos veces con la misma cola de trabajo, no se invoca la segunda devolución de llamada hasta que se devuelve la primera devolución de llamada.

## <a name="shutting-down-work-queues"></a>Cerrando colas de trabajo

Antes de llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), libere los recursos que usan los subprocesos de la cola de trabajo. Para sincronizar este proceso, puede bloquear la plataforma Media Foundation, lo que evita que la función **MFShutdown** cierre todos los subprocesos de la cola de trabajo. Si se llama a **MFShutdown** mientras la plataforma está bloqueada, **MFShutdown** espera unos cientos de milisegundos para que la plataforma se desbloquee. Si no se desbloquea dentro de ese tiempo, **MFShutdown** cierra los subprocesos de la cola de trabajo.

La implementación predeterminada de [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) bloquea automáticamente la plataforma Media Foundation cuando se crea el objeto de resultado. Al liberar la interfaz, se desbloquea la plataforma. Por lo tanto, casi nunca necesitará bloquear la plataforma directamente. Pero si escribe su propia implementación personalizada de **IMFAsyncResult**, debe bloquear y desbloquear manualmente la plataforma. Para bloquear la plataforma, llame a [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform). Para desbloquear la plataforma, llame a [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform). Para obtener un ejemplo, vea [objetos de resultado asincrónicos personalizados](custom-asynchronous-result-objects.md).

Después de llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), debe asegurarse de que la plataforma esté desbloqueada en el período de tiempo de espera de 5 segundos. Para ello, libera todos los punteros de [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) y llama a [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) si la plataforma se bloqueó manualmente. Asegúrese de liberar todos los recursos utilizados por los subprocesos de la cola de trabajo o la aplicación podría perder memoria.

Normalmente, si la aplicación se cierra y libera todos los objetos de Media Foundation antes de llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), no tiene que preocuparse por el bloqueo. El mecanismo de bloqueo simplemente permite que los subprocesos de la cola de trabajo salgan correctamente después de llamar a **MFShutdown**.

## <a name="using-scheduled-work-items"></a>Usar elementos de trabajo programados

Puede programar una devolución de llamada para que se produzca después de un período de tiempo establecido mediante una llamada a [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) o [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex).

-   [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) toma un puntero a la devolución de llamada, un objeto de estado opcional y un intervalo de tiempo de espera.
-   [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) toma un puntero a un objeto de resultado asincrónico y un valor de tiempo de espera.

Especifique el tiempo de espera como un valor negativo en milisegundos. Por ejemplo, para programar una devolución de llamada que se va a invocar en 5 segundos, use el valor − 5000. Ambas funciones devuelven un valor de **\_ clave MFWORKITEM** , que puede usar para cancelar la devolución de llamada pasándola a la función [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) .

Los elementos de trabajo programados siempre utilizan la cola de trabajo de la \_ \_ plataforma del temporizador de cola de devolución de llamada MFASYNC \_ .

## <a name="using-periodic-callbacks"></a>Usar devoluciones de llamada periódicas

La función [**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) programa una devolución de llamada que se invocará periódicamente hasta que la cancele. El intervalo de devolución de llamada es fijo. las aplicaciones no pueden cambiarla. Para averiguar el intervalo exacto, llame a [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity). El intervalo está en el orden de 10 milisegundos, por lo que esta función está pensada para situaciones en las que se necesita un "paso" frecuente, como la implementación de un reloj de presentación. Si desea programar una operación para que se produzca con menos frecuencia, use un elemento de trabajo programado, como se describió anteriormente.

A diferencia de las otras devoluciones de llamada descritas en este tema, la devolución de llamada periódica no utiliza la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . En su lugar, utiliza un puntero de función. Para obtener más información, vea [**devolución de llamada MFPERIODICCALLBACK**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).

Para cancelar la devolución de llamada periódica, llame a [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback).

Las devoluciones de llamada periódicas usan la \_ \_ cola de trabajo de \_ plataforma del temporizador de cola de devolución de llamada MFASYNC

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Colas de trabajo](work-queues.md)
</dt> <dt>

[**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[Mejoras en la cola de trabajo y subprocesos](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
