---
description: Este programa muestra cómo puede compilar una aplicación que captura eventos InkCollector solo con C++. Este programa crea un objeto InkCollector de forma co-enable de la ventana. Muestra un cuadro de mensaje cada vez que se recibe un evento Stroke.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Ejemplo de receptores de eventos de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360026"
---
# <a name="c-event-sinks-sample"></a>Ejemplo de receptores de eventos de C++

Este programa muestra cómo puede compilar una aplicación que captura eventos InkCollector solo con C++. Este programa crea un objeto [**InkCollector**](inkcollector-class.md) de forma co-enable de la ventana. Muestra un cuadro de mensaje cada vez que se [**recibe un**](inkcollector-stroke.md) evento Stroke.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Definir un contenedor para eventos del recopilador de entrada de lápiz

La clase controla el paso de eventos de recopilador de entrada de lápiz desde `InkCollectorEvents` el recopilador de entrada de lápiz al usuario de esta clase. El `AdviseInkCollector` método configura la conexión entre el objeto [**InkCollector**](inkcollector-class.md) y esta clase. El método convierte la notificación de eventos `Invoke` [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en una llamada a una función virtual que el usuario de esta clase puede invalidar para procesar un evento determinado.

> [!Note]  
> Debe hacer más que invalidar la función virtual para que un controlador de eventos obtenga ese evento. Para todos los eventos, menos los predeterminados, debe llamar al método [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) del recopilador de entrada manuscrita para garantizar la obtención de un evento. En segundo lugar, este objeto se serializa a sí mismo como subproceso libre, por lo que todos los controladores de eventos implementados también deben ser subprocesos libres. De particular importancia es usar Windows API, lo que puede provocar un cambio a otro subproceso, ya que no se garantiza que el controlador de eventos se ejecute en el mismo subproceso que la ventana conectada con el recopilador de entrada de lápiz.

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



El `Init` método llama a [CoCreateFreeThreadedMarsthread para](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) configurar un serializador de subprocesos libre.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



El `AdviseInkCollector` método configura la conexión entre el objeto [**InkCollector**](inkcollector-class.md) y esta clase. En primer lugar, recupera un punto de conexión al recopilador de entrada de lápiz. A continuación, recupera un puntero a `IInkCollectorEvents` para que pueda establecer una conexión de asesoramiento al control.


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



El `UnadviseInkCollector` método libera las conexiones que el objeto tiene con el control .


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Definir un controlador de eventos del recopilador de entrada de lápiz

La clase CMyInkEvents invalida el comportamiento predeterminado del controlador de eventos [**Stroke**](inkcollector-stroke.md) de la clase InkCollectorEvents. El método Stroke muestra un cuadro de mensaje cuando [**InkCollector**](inkcollector-class.md) recibe un **evento Stroke.**


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a>Definición de un contenedor del recopilador de entrada de lápiz

El método Init de la clase CMyInkCollector declara e inicializa un objeto CMyInkEvents. A continuación, crea [**un objeto InkCollector**](inkcollector-class.md) y asocia el recopilador de entrada de lápiz y el controlador de eventos. Por último, **InkCollector** se adjunta a la ventana y se habilita.


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Acceso a las interfaces de tablet PC y a las clases contenedoras

En primer lugar, incluya los encabezados de las interfaces de automatización de Tablet PC. Se instalan con Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Development Kit <entity type="reg"/> 1.7.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



A continuación, incluya los encabezados para las clases contenedoras y se definió el controlador de eventos [**InkCollector.**](inkcollector-class.md)


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Llamar a las clases contenedoras

Cuando se crea la ventana, el procedimiento Ventana crea un contenedor del recopilador de entrada de lápiz e inicializa el contenedor. Cuando se destruye la ventana, el procedimiento Ventana elimina el contenedor del recopilador de entrada de lápiz. El contenedor del recopilador de entrada de lápiz controla la creación y eliminación de su controlador de eventos asociado.


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
