---
description: Este programa muestra cómo puede compilar una aplicación que capture eventos InkCollector usando solo C++. Este programa crea un objeto InkCollector para habilitar la ventana de entrada de lápiz. Muestra un cuadro de mensaje cada vez que se recibe un evento de trazo.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Ejemplo de receptores de eventos de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705398"
---
# <a name="c-event-sinks-sample"></a><span data-ttu-id="0570a-105">Ejemplo de receptores de eventos de C++</span><span class="sxs-lookup"><span data-stu-id="0570a-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="0570a-106">Este programa muestra cómo puede compilar una aplicación que capture eventos InkCollector usando solo C++.</span><span class="sxs-lookup"><span data-stu-id="0570a-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="0570a-107">Este programa crea un objeto [**InkCollector**](inkcollector-class.md) para habilitar la ventana de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="0570a-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="0570a-108">Muestra un cuadro de mensaje cada vez que se recibe un evento de [**trazo**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="0570a-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="0570a-109">Definir un contenedor para eventos del recopilador de tinta</span><span class="sxs-lookup"><span data-stu-id="0570a-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="0570a-110">La `InkCollectorEvents` clase controla el paso de eventos del recopilador de tinta del recopilador de entradas de lápiz al usuario de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0570a-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="0570a-111">El `AdviseInkCollector` método configura la conexión entre el objeto [**InkCollector**](inkcollector-class.md) y esta clase.</span><span class="sxs-lookup"><span data-stu-id="0570a-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="0570a-112">El `Invoke` método convierte la notificación de eventos [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en una llamada a una función virtual que el usuario de esta clase puede reemplazar para procesar un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="0570a-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="0570a-113">Debe hacer más que invalidar la función virtual de un controlador de eventos para obtener ese evento.</span><span class="sxs-lookup"><span data-stu-id="0570a-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="0570a-114">Para todos los eventos, excepto los predeterminados, debe llamar al método [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) del recopilador de tinta para garantizar la obtención de un evento.</span><span class="sxs-lookup"><span data-stu-id="0570a-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="0570a-115">En segundo lugar, este objeto calcula las referencias de subprocesos libres, por lo que todos los controladores de eventos implementados también tienen que tener un subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="0570a-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="0570a-116">De especial importancia se usan las API de Windows, que pueden provocar un cambio a otro subproceso, ya que no se garantiza que el controlador de eventos se ejecute en el mismo subproceso que la ventana conectada con el recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="0570a-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


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



<span data-ttu-id="0570a-117">El `Init` método llama a [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) para configurar un contador de referencias de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="0570a-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="0570a-118">El `AdviseInkCollector` método configura la conexión entre el objeto [**InkCollector**](inkcollector-class.md) y esta clase.</span><span class="sxs-lookup"><span data-stu-id="0570a-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="0570a-119">En primer lugar, recupera un punto de conexión con el recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="0570a-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="0570a-120">A continuación, recupera un puntero a para `IInkCollectorEvents` que pueda establecer una conexión de consulta con el control.</span><span class="sxs-lookup"><span data-stu-id="0570a-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


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



<span data-ttu-id="0570a-121">El `UnadviseInkCollector` método libera las conexiones que el objeto tiene en el control.</span><span class="sxs-lookup"><span data-stu-id="0570a-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="0570a-122">Definir un controlador de eventos del recopilador de tinta</span><span class="sxs-lookup"><span data-stu-id="0570a-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="0570a-123">La clase CMyInkEvents invalida el comportamiento predeterminado del controlador de eventos [**Stroke**](inkcollector-stroke.md) de la clase InkCollectorEvents.</span><span class="sxs-lookup"><span data-stu-id="0570a-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="0570a-124">El método Stroke muestra un cuadro de mensaje cuando [**InkCollector**](inkcollector-class.md) recibe un evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="0570a-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


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



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="0570a-125">Definir un contenedor del recopilador de tinta</span><span class="sxs-lookup"><span data-stu-id="0570a-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="0570a-126">El método init de la clase CMyInkCollector declara e inicializa un objeto CMyInkEvents.</span><span class="sxs-lookup"><span data-stu-id="0570a-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="0570a-127">A continuación, crea un objeto [**InkCollector**](inkcollector-class.md) y asocia el recopilador de entradas de lápiz y el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="0570a-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="0570a-128">Por último, el **InkCollector** se adjunta a la ventana y se habilita.</span><span class="sxs-lookup"><span data-stu-id="0570a-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="0570a-129">Acceder a las interfaces de Tablet PC y a las clases contenedoras</span><span class="sxs-lookup"><span data-stu-id="0570a-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="0570a-130">En primer lugar, incluya los encabezados de las interfaces de automatización de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0570a-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="0570a-131">Se instalan con el kit de desarrollo de Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition 1,7.</span><span class="sxs-lookup"><span data-stu-id="0570a-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="0570a-132">A continuación, incluya los encabezados de las clases contenedoras y se definió el controlador de eventos [**InkCollector**](inkcollector-class.md) .</span><span class="sxs-lookup"><span data-stu-id="0570a-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="0570a-133">Llamar a las clases contenedoras</span><span class="sxs-lookup"><span data-stu-id="0570a-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="0570a-134">Cuando se crea la ventana, el procedimiento de ventana crea un contenedor del recopilador de tinta e inicializa el contenedor.</span><span class="sxs-lookup"><span data-stu-id="0570a-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="0570a-135">Cuando se destruye la ventana, el procedimiento de ventana elimina el contenedor del recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="0570a-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="0570a-136">El contenedor del recopilador de tinta controla la creación y eliminación de su controlador de eventos asociado.</span><span class="sxs-lookup"><span data-stu-id="0570a-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


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



 

 
