---
description: Recuperación de eventos de servicio admitidos
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Recuperación de eventos de servicio admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc1df4c8255a4dc2a1297ae99216437ac3b4c9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423475"
---
# <a name="retrieving-supported-service-events"></a>Recuperación de eventos de servicio admitidos

La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los eventos admitidos por un servicio Contacts determinado llamando a métodos en las interfaces siguientes.



| Interfaz                | Descripción    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Se usa para recuperar la **interfaz IPortableDeviceServiceCapabilities** para acceder a los eventos admitidos. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Proporciona acceso a los eventos y atributos de eventos admitidos.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene la lista de eventos admitidos.                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene los atributos de un evento determinado.                                                            |



 

Cuando el usuario elige la opción "4" en la línea de comandos, la aplicación invoca el método **ListSupportedEvents** que se encuentra en el módulo ServiceCapabilities.cpp.

Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.

En WPD, un evento se describe por su nombre, opciones y parámetros. El nombre del evento es una cadena que admite scripts, por ejemplo, "MyCustomEvent". Las opciones de evento indican si un evento determinado se difunde a todos los clientes y si ese evento admite la reproducción automática. Los atributos de parámetro de evento incluyen PROPERTYKEY y VARTYPE de un parámetro determinado.

Cuatro métodos del módulo ServiceCapabilities.cpp admiten la recuperación de eventos admitidos para el servicio Contacts dado: **ListSupportedEvents,** **DisplayEvent,** **DisplayEventOptions** y **DisplayEventParameters.** El **método ListSupportedEvents** recupera un recuento de eventos admitidos y el identificador GUID de cada evento. El **método DisplayEvent** muestra el nombre o GUID del evento y, a continuación, llama a **DisplayEventOptions** y **DisplayEventParameters** para mostrar los datos relacionados con el evento.

El **método ListSupportedEvents** invoca el método [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una [**interfaz IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Con esta interfaz, recupera los eventos admitidos llamando al método [**IPortableDeviceServiceCapabilities::GetSupportedEvents.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) El **método GetSupportedEvents** recupera los GUID de cada evento admitido por el servicio y copia esos GUID en un objeto [**IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

El código siguiente muestra cómo recuperar eventos de servicio admitidos.


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



Una vez que el método **ListSupportedEvents** recupera los GUID que representan cada evento admitido por el servicio dado, invoca el método **DisplayEvent** para recuperar datos específicos del evento. Estos datos incluyen el nombre del evento, sus opciones (difusión o reproducción automática), GUID de parámetros, tipos de parámetros, y así sucesivamente.

El **método DisplayEvent** invoca el método [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) para recuperar una colección de atributos para el evento especificado. A continuación, llama al método [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) y solicita al controlador que devuelva un nombre descriptivo para el evento especificado. A **continuación, DisplayEvent** llama a [**IPortableDeviceValues::GetIPortableDeviceValuesValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) para recuperar las opciones de evento. Por último, DisplayEvent llama a [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue para**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) recuperar la lista de parámetros de evento. Pasa los datos devueltos por estos métodos a las funciones auxiliares **DisplayEventOptions** y **DisplayEventParameters,** que representan las opciones y la información de parámetros para el evento especificado.

El código siguiente usa el **método DisplayEvent.**


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



La función auxiliar **DisplayEventOptions** recibe un [**objeto IPortableDeviceValues**](iportabledevicevalues.md) que contiene los datos de opción del evento. A continuación, llama [**al método IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) para recuperar los datos de opciones. Con estos datos, representa una cadena que indica si se admiten las opciones de difusión y reproducción automática.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



