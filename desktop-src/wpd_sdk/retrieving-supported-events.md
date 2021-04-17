---
description: Recuperación de eventos de servicio admitidos
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Recuperación de eventos de servicio admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716776"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="c5c76-103">Recuperación de eventos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="c5c76-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="c5c76-104">La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los eventos admitidos por un servicio de contactos determinado llamando a métodos en las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="c5c76-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c76-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c5c76-105">Interface</span></span>                                                                            | <span data-ttu-id="c5c76-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5c76-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="c5c76-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="c5c76-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="c5c76-108">Se usa para recuperar la interfaz **IPortableDeviceServiceCapabilities** para tener acceso a los eventos admitidos.</span><span class="sxs-lookup"><span data-stu-id="c5c76-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="c5c76-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c5c76-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="c5c76-110">Proporciona acceso a los eventos y atributos de evento admitidos.</span><span class="sxs-lookup"><span data-stu-id="c5c76-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="c5c76-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c5c76-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="c5c76-112">Contiene la lista de eventos admitidos.</span><span class="sxs-lookup"><span data-stu-id="c5c76-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="c5c76-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c5c76-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="c5c76-114">Contiene los atributos de un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="c5c76-115">Cuando el usuario elige la opción "4" en la línea de comandos, la aplicación invoca el método **ListSupportedEvents** que se encuentra en el módulo ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="c5c76-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="c5c76-116">Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio de contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="c5c76-117">En WPD, un evento se describe mediante el nombre, las opciones y los parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5c76-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="c5c76-118">El nombre del evento es una cadena descriptiva para scripts, por ejemplo, "MyCustomEvent".</span><span class="sxs-lookup"><span data-stu-id="c5c76-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="c5c76-119">Las opciones de evento indican si un evento determinado se difunde a todos los clientes y si ese evento es compatible con la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="c5c76-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="c5c76-120">Los atributos de parámetro de evento incluyen PROPERTYKEY y VARTYPE de un parámetro determinado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="c5c76-121">Cuatro métodos en el módulo ServiceCapabilities. cpp admiten la recuperación de eventos admitidos para el servicio de contactos dado: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** y **DisplayEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="c5c76-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="c5c76-122">El método **ListSupportedEvents** recupera un recuento de eventos admitidos y el identificador GUID para cada evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="c5c76-123">El método **DisplayEvent** muestra el nombre del evento o el GUID y, a continuación, llama a **DisplayEventOptions** y **DisplayEventParameters** para mostrar los datos relacionados con el evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="c5c76-124">El método **ListSupportedEvents** invoca el método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="c5c76-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="c5c76-125">Mediante esta interfaz, recupera los eventos admitidos llamando al método [**IPortableDeviceServiceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="c5c76-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="c5c76-126">El método **GetSupportedEvents** recupera los GUID para cada evento admitido por el servicio y copia esos GUID en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c5c76-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="c5c76-127">En el código siguiente se muestra cómo recuperar eventos de servicio admitidos.</span><span class="sxs-lookup"><span data-stu-id="c5c76-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pEvents->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have an event.  It is assumed that
                // events are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="c5c76-128">Después de que el método **ListSupportedEvents** recupera los GUID que representan cada evento admitido por el servicio determinado, invoca el método **DisplayEvent** para recuperar los datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="c5c76-129">Estos datos incluyen el nombre del evento, sus opciones (difusión o reproducción automática), GUID de parámetros, tipos de parámetros, etc.</span><span class="sxs-lookup"><span data-stu-id="c5c76-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="c5c76-130">El método **DisplayEvent** invoca el método [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) para recuperar una colección de atributos para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="c5c76-131">A continuación, llama al método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) y solicita que el controlador devuelva un nombre descriptivo para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="c5c76-132">A continuación, **DisplayEvent** llama a [**IPortableDeviceValues:: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) para recuperar las opciones de evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="c5c76-133">Por último, DisplayEvent llama a [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar la lista de parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="c5c76-134">Pasa los datos devueltos por estos métodos a las funciones auxiliares **DisplayEventOptions** y **DisplayEventParameters** , que representan las opciones y la información de parámetros para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="c5c76-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="c5c76-135">En el código siguiente se usa el método **DisplayEvent** .</span><span class="sxs-lookup"><span data-stu-id="c5c76-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="c5c76-136">La función auxiliar **DisplayEventOptions** recibe un objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contiene los datos de la opción del evento.</span><span class="sxs-lookup"><span data-stu-id="c5c76-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="c5c76-137">A continuación, llama al método [**IPortableDeviceValues:: GetBoolValue**](iportabledevicevalues-getboolvalue.md) para recuperar los datos de opciones.</span><span class="sxs-lookup"><span data-stu-id="c5c76-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="c5c76-138">Con estos datos, representa una cadena que indica si se admiten las opciones de difusión y reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="c5c76-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="c5c76-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5c76-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c76-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="c5c76-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="c5c76-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="c5c76-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="c5c76-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c5c76-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="c5c76-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c5c76-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c5c76-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="c5c76-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



