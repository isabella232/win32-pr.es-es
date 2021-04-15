---
title: Búsqueda sincrónica
description: El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas. Las búsquedas sincrónicas se completan y devuelven el control a la aplicación que realiza la llamada solo después de encontrar todos los dispositivos disponibles.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695428"
---
# <a name="synchronous-searching"></a><span data-ttu-id="d21f8-104">Búsqueda sincrónica</span><span class="sxs-lookup"><span data-stu-id="d21f8-104">Synchronous Searching</span></span>

<span data-ttu-id="d21f8-105">El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="d21f8-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="d21f8-106">Las búsquedas sincrónicas se completan y devuelven el control a la aplicación que realiza la llamada solo después de encontrar todos los dispositivos disponibles.</span><span class="sxs-lookup"><span data-stu-id="d21f8-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="d21f8-107">Para realizar una búsqueda sincrónica, use uno de los métodos de búsqueda sincrónicos de la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .</span><span class="sxs-lookup"><span data-stu-id="d21f8-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="d21f8-108">Las búsquedas sincrónicas tardan al menos nueve segundos en devolverse.</span><span class="sxs-lookup"><span data-stu-id="d21f8-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="d21f8-109">El retraso se debe a que el mensaje de búsqueda UDP inicial se debe enviar varias veces.</span><span class="sxs-lookup"><span data-stu-id="d21f8-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="d21f8-110">Esta duplicación tiene en cuenta la no confiabilidad del Protocolo de red subyacente.</span><span class="sxs-lookup"><span data-stu-id="d21f8-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="d21f8-111">Las búsquedas sincrónicas son más adecuadas para las interfaces de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d21f8-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="d21f8-112">No se recomiendan para las interfaces de usuario gráficas.</span><span class="sxs-lookup"><span data-stu-id="d21f8-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="d21f8-113">El método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) busca por dispositivo o tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="d21f8-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="d21f8-114">Este método toma un URI de tipo como parámetro de entrada y devuelve una colección de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d21f8-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="d21f8-115">Un objeto de dispositivo representa un dispositivo individual.</span><span class="sxs-lookup"><span data-stu-id="d21f8-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="d21f8-116">En los siguientes ejemplos se muestra cómo realizar una búsqueda sincrónica de dispositivos en VBScript.</span><span class="sxs-lookup"><span data-stu-id="d21f8-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="d21f8-117">Cada script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), llamado con el URI de tipo (identificador de servicio) para el tipo de dispositivo del reproductor de media, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*.</span><span class="sxs-lookup"><span data-stu-id="d21f8-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="d21f8-118">El método devuelve una colección de objetos de dispositivo que corresponde a los dispositivos del reproductor de media que se encontraron.</span><span class="sxs-lookup"><span data-stu-id="d21f8-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="d21f8-119">Para obtener información sobre cómo extraer objetos de dispositivo individuales de una colección, consulte [colecciones de dispositivos devueltas por búsquedas sincrónicas](device-collections-returned-by-synchronous-searches.md).</span><span class="sxs-lookup"><span data-stu-id="d21f8-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="d21f8-120">Buscar dispositivos por tipo en VBScript</span><span class="sxs-lookup"><span data-stu-id="d21f8-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="d21f8-121">Buscar dispositivo por tipo en C++</span><span class="sxs-lookup"><span data-stu-id="d21f8-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="d21f8-122">En el ejemplo siguiente se muestra una búsqueda sincrónica de dispositivos del reproductor de media con C++.</span><span class="sxs-lookup"><span data-stu-id="d21f8-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="d21f8-123">La función toma un puntero a la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) como entrada y devuelve el puntero de la interfaz [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="d21f8-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="d21f8-124">En primer lugar, el ejemplo asigna un **BSTR** para representar el URI de tipo de dispositivo y, a continuación, lo pasa al método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) .</span><span class="sxs-lookup"><span data-stu-id="d21f8-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="d21f8-125">También pasa la dirección de un puntero [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local en el búfer en el que el método almacena la colección de dispositivos encontrados.</span><span class="sxs-lookup"><span data-stu-id="d21f8-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="d21f8-126">Si la llamada de función se realiza correctamente, devuelve el puntero a esta colección.</span><span class="sxs-lookup"><span data-stu-id="d21f8-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




