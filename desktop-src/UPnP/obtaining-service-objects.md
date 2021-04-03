---
title: Obtener objetos de servicio
description: Los objetos de dispositivo exponen una propiedad denominada servicios que devuelve una colección de objetos de servicio que contiene un objeto de servicio para cada servicio exportado por el dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904742"
---
# <a name="obtaining-service-objects"></a>Obtener objetos de servicio

Los objetos de dispositivo exponen una propiedad denominada [**servicios**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) que devuelve una colección de objetos de servicio que contiene un objeto de servicio para cada servicio exportado por el dispositivo. Las aplicaciones pueden atravesar esta colección secuencialmente o solicitar un servicio determinado mediante su identificador de servicio.

## <a name="vbscript-example"></a>Ejemplo de VBScript

El ejemplo siguiente es código VBScript que extrae objetos de servicio para dos de los servicios exportados por un dispositivo.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



La primera línea extrae la colección de servicios del objeto de dispositivo consultando la propiedad [**servicios**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) . Las dos líneas siguientes obtienen los dos objetos de servicio deseados de la colección mediante la especificación de sus identificadores de servicio. La colección de servicios también se puede recorrer secuencialmente mediante el uso **de un para cada... siguiente** bucle.

## <a name="c-example"></a>Ejemplo de C++

En el ejemplo siguiente se muestra el código de C++ necesario para obtener objetos de servicio de un dispositivo. En primer lugar, el código de ejemplo consulta la propiedad [**IUPnPDevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) en la interfaz que se pasó a la función. Esto devuelve una colección de servicios mediante la interfaz [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) . Para obtener objetos de servicio individuales, use el método [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) y especifique los identificadores de servicio solicitados. Para atravesar la colección secuencialmente, use los métodos [**IEnumVARIANT:: RESET**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)y [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) . Este ejemplo es similar al ejemplo usado para atravesar la colección [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .


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



 

 