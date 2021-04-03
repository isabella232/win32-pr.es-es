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
# <a name="obtaining-service-objects"></a><span data-ttu-id="bfa62-103">Obtener objetos de servicio</span><span class="sxs-lookup"><span data-stu-id="bfa62-103">Obtaining Service Objects</span></span>

<span data-ttu-id="bfa62-104">Los objetos de dispositivo exponen una propiedad denominada [**servicios**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) que devuelve una colección de objetos de servicio que contiene un objeto de servicio para cada servicio exportado por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfa62-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="bfa62-105">Las aplicaciones pueden atravesar esta colección secuencialmente o solicitar un servicio determinado mediante su identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="bfa62-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="bfa62-106">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="bfa62-106">VBScript Example</span></span>

<span data-ttu-id="bfa62-107">El ejemplo siguiente es código VBScript que extrae objetos de servicio para dos de los servicios exportados por un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfa62-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="bfa62-108">La primera línea extrae la colección de servicios del objeto de dispositivo consultando la propiedad [**servicios**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) .</span><span class="sxs-lookup"><span data-stu-id="bfa62-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="bfa62-109">Las dos líneas siguientes obtienen los dos objetos de servicio deseados de la colección mediante la especificación de sus identificadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="bfa62-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="bfa62-110">La colección de servicios también se puede recorrer secuencialmente mediante el uso **de un para cada... siguiente** bucle.</span><span class="sxs-lookup"><span data-stu-id="bfa62-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="bfa62-111">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="bfa62-111">C++ Example</span></span>

<span data-ttu-id="bfa62-112">En el ejemplo siguiente se muestra el código de C++ necesario para obtener objetos de servicio de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfa62-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="bfa62-113">En primer lugar, el código de ejemplo consulta la propiedad [**IUPnPDevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) en la interfaz que se pasó a la función.</span><span class="sxs-lookup"><span data-stu-id="bfa62-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="bfa62-114">Esto devuelve una colección de servicios mediante la interfaz [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) .</span><span class="sxs-lookup"><span data-stu-id="bfa62-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="bfa62-115">Para obtener objetos de servicio individuales, use el método [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) y especifique los identificadores de servicio solicitados.</span><span class="sxs-lookup"><span data-stu-id="bfa62-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="bfa62-116">Para atravesar la colección secuencialmente, use los métodos [**IEnumVARIANT:: RESET**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)y [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="bfa62-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="bfa62-117">Este ejemplo es similar al ejemplo usado para atravesar la colección [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="bfa62-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


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



 

 