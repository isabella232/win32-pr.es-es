---
title: Cómo implementar controladores de eventos
description: Este tema contiene código de ejemplo que muestra cómo implementar interfaces que permiten a los clientes recibir y controlar eventos de automatización de la interfaz de usuario de Microsoft.
ms.assetid: 6b6549b8-795b-45a8-8fef-59842cc990e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159e95e739ae73f1c37d99ae065032fd680f0720
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357572"
---
# <a name="how-to-implement-event-handlers"></a><span data-ttu-id="50648-103">Cómo implementar controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="50648-103">How to Implement Event Handlers</span></span>

<span data-ttu-id="50648-104">Este tema contiene código de ejemplo que muestra cómo implementar interfaces que permiten a los clientes recibir y controlar eventos de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="50648-104">This topic contains example code that shows how to implement interfaces that enable clients to receive and handle Microsoft UI Automation events.</span></span> <span data-ttu-id="50648-105">Se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="50648-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="50648-106">Controlar eventos generales de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="50648-106">Handling General UI Automation Events</span></span>](#handling-general-ui-automation-events)
-   [<span data-ttu-id="50648-107">Controlar eventos de Focus-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-107">Handling Focus-Changed Events</span></span>](#handling-focus-changed-events)
-   [<span data-ttu-id="50648-108">Controlar eventos de Property-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-108">Handling Property-Changed Events</span></span>](#handling-property-changed-events)
-   [<span data-ttu-id="50648-109">Controlar eventos de Structure-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-109">Handling Structure-Changed Events</span></span>](#handling-structure-changed-events)
-   [<span data-ttu-id="50648-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50648-110">Related topics</span></span>](#related-topics)

## <a name="handling-general-ui-automation-events"></a><span data-ttu-id="50648-111">Controlar eventos generales de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="50648-111">Handling General UI Automation Events</span></span>

<span data-ttu-id="50648-112">El ejemplo de código siguiente es una aplicación de consola de Microsoft Windows que implementa un controlador de eventos de automatización de la interfaz de usuario para eventos generales de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="50648-112">The following code example is a Microsoft Windows console application that implements a UI Automation event handler for general UI Automation events.</span></span> <span data-ttu-id="50648-113">Este ejemplo controla los eventos de creación y destrucción de la información sobre herramientas y otras ventanas.</span><span class="sxs-lookup"><span data-stu-id="50648-113">This example handles creation and destruction events for tooltips and other windows.</span></span>


```C++
// Defines an event handler for general UI Automation events. It listens for
// tooltip and window creation and destruction events. 
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    // Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    // IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown)) 
            *ppInterface=static_cast<IUIAutomationEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationEventHandler)) 
            *ppInterface=static_cast<IUIAutomationEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationEventHandler methods
    HRESULT STDMETHODCALLTYPE HandleAutomationEvent(IUIAutomationElement * pSender, EVENTID eventID)
    {
        _eventCount++;
        switch (eventID) 
        {
            case UIA_ToolTipOpenedEventId:
                wprintf(L">> Event ToolTipOpened Received! (count: %d)\n", _eventCount);
                break;
            case UIA_ToolTipClosedEventId:
                wprintf(L">> Event ToolTipClosed Received! (count: %d)\n", _eventCount);
                break;
            case UIA_Window_WindowOpenedEventId:
                wprintf(L">> Event WindowOpened Received! (count: %d)\n", _eventCount);
                break;
            case UIA_Window_WindowClosedEventId:
                wprintf(L">> Event WindowClosed Received! (count: %d)\n", _eventCount);
                break;
            default:
                wprintf(L">> Event (%d) Received! (count: %d)\n", eventID, _eventCount);
                break;
        }
        return S_OK;
    }
};

int main(int argc, char* argv[])
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);
    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL,CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if(FAILED(hr) || pAutomation==NULL) 
    {
        ret = 1;
        goto cleanup;
    }
    // Use root element for listening to window and tooltip creation and destruction.
    hr = pAutomation->GetRootElement(&pTargetElement);
    if (FAILED(hr) || pTargetElement==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handlers.\n");
    hr = pAutomation->AddAutomationEventHandler(UIA_ToolTipOpenedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_ToolTipClosedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_Window_WindowOpenedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_Window_WindowClosedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handlers and exit\n");
    getchar();

    wprintf(L"-Removing Event Handlers.\n");

cleanup:
    // Remove event handlers, release resources, and terminate
    if (pAutomation != NULL) 
    {
        hr = pAutomation->RemoveAllEventHandlers();
        if (FAILED(hr))
            ret = 1;
        pAutomation->Release();
    }

    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-focus-changed-events"></a><span data-ttu-id="50648-114">Controlar eventos de Focus-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-114">Handling Focus-Changed Events</span></span>

<span data-ttu-id="50648-115">El ejemplo de código siguiente es una aplicación de consola de Windows que implementa un controlador para los eventos de cambio de foco.</span><span class="sxs-lookup"><span data-stu-id="50648-115">The following code example is a Windows console application that implements a handler for focus-changed events.</span></span>


```C++
// Defines an event handler for focus changed events and starts
// listening to them.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationFocusChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    //Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    //IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface = static_cast<IUIAutomationFocusChangedEventHandler*>(this);
        else if(riid == __uuidof(IUIAutomationFocusChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationFocusChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationFocusChangedEventHandler methods.
    HRESULT STDMETHODCALLTYPE HandleFocusChangedEvent(IUIAutomationElement * pSender) 
    {
        _eventCount++;
        wprintf(L">> FocusChangedEvent Received! (count: %d)\n", _eventCount);
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);
    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL,CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation == NULL)
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL)
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handlers.\n");
    hr = pAutomation->AddFocusChangedEventHandler(NULL, (IUIAutomationFocusChangedEventHandler*) pEHTemp); 
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handlers.\n");
    hr = pAutomation->RemoveFocusChangedEventHandler((IUIAutomationFocusChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-property-changed-events"></a><span data-ttu-id="50648-116">Controlar eventos de Property-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-116">Handling Property-Changed Events</span></span>

<span data-ttu-id="50648-117">El ejemplo de código siguiente es una aplicación de consola de Windows que implementa un controlador para los eventos de cambio de propiedad.</span><span class="sxs-lookup"><span data-stu-id="50648-117">The following code example is a Windows console application that implements a handler for property-changed events.</span></span>


```C++
// Defines an event handler for property-changed events, and listens for
// ToggleState property changes on the element specifies by the user.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationPropertyChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    //Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    //IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface=static_cast<IUIAutomationPropertyChangedEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationPropertyChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationPropertyChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationPropertyChangedEventHandler methods.
    HRESULT STDMETHODCALLTYPE HandlePropertyChangedEvent(IUIAutomationElement* pSender, PROPERTYID propertyID, VARIANT newValue) 
    {
        _eventCount++;
        if (propertyID == UIA_ToggleToggleStatePropertyId) 
            wprintf(L">> Property ToggleState changed! ");
        else 
            wprintf(L">> Property (%d) changed! ", propertyID);

        if (newValue.vt == VT_I4) 
            wprintf(L"(0x%0.8x) ", newValue.lVal);

        wprintf(L"(count: %d)\n", _eventCount);
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);

    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Use the mouse to point to the element you want to listen from.\n");
    Sleep(3000);

    // Make this application dots-per-inch (DPI) aware.
    SetProcessDPIAware();

    // Get mouse cursor position and get element from point.
    POINT pt;
    GetPhysicalCursorPos(&pt);
    hr = pAutomation->ElementFromPoint(pt, &pTargetElement);
    if (FAILED(hr) || pTargetElement==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    PROPERTYID pPIDProperties[] = { UIA_ToggleToggleStatePropertyId };

    wprintf(L"-Adding Event Handler.\n");
    hr = pAutomation->AddPropertyChangedEventHandlerNativeArray(pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationPropertyChangedEventHandler*) pEHTemp, pPIDProperties, sizeof(pPIDProperties) / sizeof(pPIDProperties[0]));
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handler.\n");
    hr = pAutomation->RemovePropertyChangedEventHandler(pTargetElement, (IUIAutomationPropertyChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-structure-changed-events"></a><span data-ttu-id="50648-118">Controlar eventos de Structure-Changed</span><span class="sxs-lookup"><span data-stu-id="50648-118">Handling Structure-Changed Events</span></span>

<span data-ttu-id="50648-119">El ejemplo de código siguiente es una aplicación de consola de Windows que implementa un controlador para los eventos de cambio de estructura.</span><span class="sxs-lookup"><span data-stu-id="50648-119">The following code example is a Windows console application that implements a handler for structure-changed events.</span></span>


```C++
// Defines an event handler for structure-changed events, and 
// listens for them on the element specifies by the user.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationStructureChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    // Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    // IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface=static_cast<IUIAutomationStructureChangedEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationStructureChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationStructureChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationStructureChangedEventHandler methods
    HRESULT STDMETHODCALLTYPE HandleStructureChangedEvent(IUIAutomationElement* pSender, StructureChangeType changeType, SAFEARRAY* pRuntimeID) {
        _eventCount++;
        switch (changeType) 
        {
            case StructureChangeType_ChildAdded:
                wprintf(L">> Structure Changed: ChildAdded! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildRemoved:
                wprintf(L">> Structure Changed: ChildRemoved! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenInvalidated:
                wprintf(L">> Structure Changed: ChildrenInvalidated! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenBulkAdded:
                wprintf(L">> Structure Changed: ChildrenBulkAdded! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenBulkRemoved:
                wprintf(L">> Structure Changed: ChildrenBulkRemoved! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenReordered:
                wprintf(L">> Structure Changed: ChildrenReordered! (count: %d)\n", _eventCount);
                break;
        }
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);

    IUIAutomation* pAutomation=NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Use the mouse to point to the element you want to listen from.\n");
    Sleep(3000);

    // Make this application dots-per-inch (DPI) aware.
    SetProcessDPIAware();

    // Get mouse cursor position and get element from point.
    POINT pt;
    GetPhysicalCursorPos(&pt);
    hr = pAutomation->ElementFromPoint(pt, &pTargetElement);
    if (FAILED(hr) || pTargetElement == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handler.\n");
    hr = pAutomation->AddStructureChangedEventHandler(pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationStructureChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handler.\n");
    hr = pAutomation->RemoveStructureChangedEventHandler(pTargetElement, (IUIAutomationStructureChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="50648-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50648-120">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50648-121">**Vista**</span><span class="sxs-lookup"><span data-stu-id="50648-121">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50648-122">Suscribirse a eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="50648-122">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="50648-123">Temas de procedimientos para clientes de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="50648-123">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




