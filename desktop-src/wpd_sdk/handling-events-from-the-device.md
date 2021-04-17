---
description: Control de eventos desde el dispositivo
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: Control de eventos desde el dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707357"
---
# <a name="handling-events-from-the-device"></a><span data-ttu-id="fab00-103">Control de eventos desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="fab00-103">Handling Events from the Device</span></span>

<span data-ttu-id="fab00-104">Otra operación que realiza una aplicación de WPD es el control de los eventos desencadenados por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fab00-104">Another operation accomplished by a WPD application is the handling of events that are fired by the device.</span></span>

<span data-ttu-id="fab00-105">Las operaciones de control de eventos se realizan mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fab00-105">Event handling operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="fab00-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="fab00-106">Interface</span></span>                                                                      | <span data-ttu-id="fab00-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fab00-107">Description</span></span>                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="fab00-108">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="fab00-108">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | <span data-ttu-id="fab00-109">Permite que la aplicación se registre para recibir devoluciones de llamada asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="fab00-109">Lets the application register to receive asynchronous callbacks.</span></span> |
| [<span data-ttu-id="fab00-110">**Interfaz IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="fab00-110">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | <span data-ttu-id="fab00-111">Contiene el controlador de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fab00-111">Contains the application's event handler.</span></span>                        |



 

<span data-ttu-id="fab00-112">La clase CPortableDeviceEventsCallback del módulo DeviceEvents. cpp de la aplicación de ejemplo muestra cómo una aplicación puede implementar [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span><span class="sxs-lookup"><span data-stu-id="fab00-112">The CPortableDeviceEventsCallback class in the sample application's DeviceEvents.cpp module demonstrates how an application can implement [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span></span> <span data-ttu-id="fab00-113">La implementación del método [**onEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) en esta clase escribe los parámetros de cualquier evento en la ventana de la consola de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fab00-113">The implementation of the [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) method in this class writes the parameters for any event to the application's console window.</span></span> <span data-ttu-id="fab00-114">Además del método onEvent, esta clase implementa AddRef y release, que se usan para mantener el recuento de referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="fab00-114">In addition to the OnEvent method, this class implements AddRef and Release, which are used to maintain the object's reference count.</span></span>


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



<span data-ttu-id="fab00-115">La aplicación de ejemplo crea una instancia de la clase CPortableDeviceEventsCallback en su función auxiliar RegisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="fab00-115">The sample application instantiates the CPortableDeviceEventsCallback class in its RegisterForEventNotifications helper function.</span></span> <span data-ttu-id="fab00-116">Esta función crea una instancia del objeto de devolución de llamada mediante el operador new.</span><span class="sxs-lookup"><span data-stu-id="fab00-116">This function creates an instance of the callback object using the new operator.</span></span> <span data-ttu-id="fab00-117">A continuación, llama al método [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) para registrar la devolución de llamada y comenzar a recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="fab00-117">It then calls the [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) method to register the callback and begin receiving events.</span></span>


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



<span data-ttu-id="fab00-118">Una vez que la aplicación de ejemplo está a la recepción de eventos, llama a la función auxiliar UnregisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="fab00-118">Once the sample application is through receiving events, it calls the UnregisterForEventNotifications helper function.</span></span> <span data-ttu-id="fab00-119">Esta función, a su vez, llama al método [**IPortableDevice:: Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) para anular el registro de la devolución de llamada de los eventos de recepción.</span><span class="sxs-lookup"><span data-stu-id="fab00-119">This function, in turn, calls the [**IPortableDevice::Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) method to unregister the callback from receiving events.</span></span>


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a><span data-ttu-id="fab00-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fab00-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab00-121">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="fab00-121">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="fab00-122">**Interfaz IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="fab00-122">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[<span data-ttu-id="fab00-123">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="fab00-123">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



