---
title: Obtener objetos de servicio
description: Los objetos de dispositivo exponen una propiedad denominada Servicios que devuelve una colección de objetos de servicio que contiene un objeto de servicio para cada servicio exportado por el dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b7fca24bfc79a9458cfb964af28edba813a90ef17924a68fd0d1689e047884c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999575"
---
# <a name="obtaining-service-objects"></a>Obtener objetos de servicio

Los objetos de dispositivo exponen una propiedad denominada [**Servicios**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) que devuelve una colección de objetos de servicio que contiene un objeto de servicio para cada servicio exportado por el dispositivo. Las aplicaciones pueden recorrer esta colección secuencialmente o solicitar un servicio determinado mediante su identificador de servicio.

## <a name="vbscript-example"></a>Ejemplo de VBScript

El ejemplo siguiente es código VBScript que extrae objetos service para dos de los servicios exportados por un dispositivo.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



La primera línea extrae la colección de servicios del objeto Device consultando la [**propiedad**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) Services. Las dos líneas siguientes obtienen los dos objetos service deseados de la colección especificando sus propios valores de servicio. La colección de servicios también se puede recorrer secuencialmente mediante un **para cada ... bucle** next.

## <a name="c-example"></a>Ejemplo de C++

En el ejemplo siguiente se muestra el código de C++ necesario para obtener objetos service de un dispositivo. En primer lugar, el código de ejemplo consulta la propiedad [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) en la interfaz que se pasó a la función. Esto devuelve una colección de servicios mediante la [**interfaz IUPnPServices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) Para obtener objetos de servicio individuales, use el [**método Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) y especifique los iDs de servicio solicitados. Para recorrer la colección secuencialmente, use los métodos [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT::Skip.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) Este ejemplo es similar al ejemplo que se usa para recorrer la [**colección IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 