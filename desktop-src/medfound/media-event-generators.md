---
description: Generadores de eventos multimedia
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Generadores de eventos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579928"
---
# <a name="media-event-generators"></a>Generadores de eventos multimedia

Media Foundation proporciona una manera coherente de que los objetos envíen eventos. Un objeto puede usar eventos para indicar la finalización de un método asincrónico o para notificar a la aplicación un cambio en el estado del objeto.

Si un objeto envía eventos, expone la [**interfaz IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Cada vez que el objeto envía un nuevo evento, el evento se coloca en una cola. La aplicación puede solicitar el siguiente evento de la cola llamando a uno de los métodos siguientes:

-   [**IMFMediaEventGenerator::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

El [**método GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) es sincrónico. Si un evento ya está en la cola, el método devuelve inmediatamente. Si no hay ningún evento en la cola, el método produce un error inmediatamente o se bloquea hasta que se pone en cola el siguiente evento, en función de la marca que pase a **GetEvent**.

El [**método BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) es asincrónico, por lo que nunca se bloquea. Este método toma un puntero a la interfaz [**IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) que la aplicación debe implementar. Cuando se invoca la devolución de llamada, la aplicación llama [**a IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obtener el evento de la cola. Para obtener más información sobre **LA DEVOLUCIÓN DE LLAMADA AASYNC,** vea [Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md).

Los eventos se representan mediante la [**interfaz IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) Esta interfaz tiene los métodos siguientes:

-   [**GetType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)recupera el tipo de evento. El tipo de evento indica lo que ha ocurrido para desencadenar el evento.

-   [**GetStatus:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)recupera un valor **HRESULT,** que indica si la operación que desencadenó el evento se ha realizado correctamente. Si se produce un error en una operación de forma asincrónica, **GetStatus** devuelve un código de error.

-   [**GetValue:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)recupera un **ELEMENTO PROPVARIANT** que contiene datos de eventos. Los datos del evento dependen del tipo de evento. Algunos eventos no tienen datos.

-   [**GetExtendedType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)recupera un **GUID**. Este método se aplica al [evento MEExtendedType](meextendedtype.md)y proporciona una manera de definir eventos personalizados.

La [**interfaz IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) también hereda la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Algunos eventos llevan información adicional como atributos.

Para obtener una lista de tipos de eventos y sus datos y atributos asociados, [vea Media Foundation Events](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implementación de IMFMediaEventGenerator

Si va a escribir un componente de complemento para Media Foundation, como un origen multimedia personalizado o un receptor multimedia, es posible que tenga que implementar [**ELERMEDIAEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator). Para facilitar esto, Media Foundation proporciona un objeto auxiliar que implementa una cola de eventos. Cree la cola de eventos llamando a [**la función MFCreateEventQueue.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) La cola de eventos expone la [**interfaz IMFMediaEventQueue.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) En la implementación del objeto de los métodos **IMFMediaEventGenerator,** llame al método correspondiente en la cola de eventos.

El objeto de cola de eventos es seguro para subprocesos. No mantenga nunca el mismo objeto de sección crítica al llamar [**a GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) y [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), porque **GetEvent** podría bloquear indefinidamente la espera de [**QueueEvent.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent) Si mantiene la misma sección crítica para ambos métodos, provocará un interbloqueo.

Antes de liberar la cola de eventos, llame [**a IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) para liberar los recursos que contiene el objeto.

Cuando el objeto necesite generar un evento, llame a uno de los métodos siguientes en la cola de eventos:

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Estos métodos ponen un nuevo evento en la cola y señalan a cualquier llamador que esté esperando el siguiente evento.

En el código siguiente se muestra una clase que implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) mediante este objeto auxiliar. Esta clase define un método **shutdown** público que apaga la cola de eventos y libera el puntero de la cola de eventos. Este comportamiento sería típico para los orígenes de medios y los receptores de medios, que siempre tienen un **método Shutdown.**


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)
</dt> </dl>

 

 



