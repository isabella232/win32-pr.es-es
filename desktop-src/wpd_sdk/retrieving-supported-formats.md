---
description: Recuperación de formatos de servicio admitidos
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recuperación de formatos de servicio admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73618f3450255ad470545ac472ad9f71238621e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572057"
---
# <a name="retrieving-supported-service-formats"></a>Recuperación de formatos de servicio admitidos

La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los formatos admitidos por un servicio Contacts determinado llamando a métodos de las interfaces de la tabla siguiente.



| Interfaz | Descripción   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Se usa para recuperar la **interfaz IPortableDeviceServiceCapabilities** para acceder a los eventos admitidos. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Proporciona acceso a los eventos y atributos de evento admitidos.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene la lista de formatos admitidos.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene los atributos de un formato determinado.                                                           |



 

Cuando el usuario elige la opción "3" en la línea de comandos, la aplicación invoca el método **ListSupportedFormats** que se encuentra en el módulo ServiceCapabilities.cpp.

Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.

En WPD, un formato se describe mediante atributos que especifican el nombre y (opcionalmente) el tipo MIME de un formato determinado. Estos atributos se definen en el archivo de encabezadoPortableDevice.h. Para obtener una descripción de los atributos admitidos, consulte el [tema Atributos.](attributes.md)

En el caso de la aplicación de ejemplo, si WpdServiceSampleDriver es el único dispositivo instalado, el controlador devuelve dos formatos admitidos para su servicio Contact: "AbstractContactFormat" y "VCard2Format". Estos formatos corresponden a los atributos **WPD \_ OBJECT FORMAT ABSTRACT \_ \_ \_ CONTACT** y **WPD OBJECT FORMAT \_ \_ \_ VCARD2** que se encuentran en PortableDevice.h.

Dos métodos del módulo ServiceCapabilities.cpp admiten la recuperación de formatos admitidos para el servicio Contacts: **ListSupportedFormats** y **DisplayFormat.** El primero recupera el identificador GUID para cada formato admitido. Este último convierte este GUID en una cadena fácil de usar.

El **método ListSupportedFormats** invoca el método [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una [**interfaz IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Con esta interfaz, recupera los formatos admitidos llamando al método [**IPortableDeviceServiceCapabilities::GetSupportedFormats.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) El **método GetSupportedFormats** recupera el GUID para cada formato admitido por el servicio y copia ese GUID en un [**objeto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

El código siguiente usa el **método ListSupportedFormats.**


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



Una vez que el método **ListSupportedFormats** recupera el GUID para cada formato admitido por el servicio dado, invoca el método **DisplayFormat** para mostrar el nombre descriptivo del script para cada formato; por ejemplo, "VCard2".

El **método DisplayFormat** invoca el método [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) para recuperar una colección de atributos para el GUID de formato especificado. A continuación, llama al método [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) y solicita que el controlador devuelva un nombre descriptivo de script para el formato especificado.

En el código siguiente se usa **el método DisplayFormat.**


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



