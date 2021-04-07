---
title: Describir dispositivos
description: Hay dos maneras de obtener objetos de dispositivo.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903724"
---
# <a name="describing-devices"></a><span data-ttu-id="3d293-103">Describir dispositivos</span><span class="sxs-lookup"><span data-stu-id="3d293-103">Describing Devices</span></span>

<span data-ttu-id="3d293-104">Hay dos maneras de obtener objetos de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="3d293-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="3d293-105">Uso de la interfaz [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="3d293-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="3d293-106">La interfaz **IUPnPDescriptionDocument** es la única interfaz segura para el scripting.</span><span class="sxs-lookup"><span data-stu-id="3d293-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="3d293-107">Uso de la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para obtener una interfaz [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="3d293-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="3d293-108">Ambos métodos devuelven colecciones de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d293-108">Both methods return Devices collections.</span></span> <span data-ttu-id="3d293-109">Las aplicaciones usan los métodos de dispositivo para recuperar propiedades acerca de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d293-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="3d293-110">Las aplicaciones pueden recuperar los siguientes tipos de información:</span><span class="sxs-lookup"><span data-stu-id="3d293-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="3d293-111">Información de la jerarquía de dispositivos, incluidos los dispositivos raíz, los dispositivos primarios y los dispositivos secundarios.</span><span class="sxs-lookup"><span data-stu-id="3d293-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="3d293-112">Propiedades de dispositivo, incluidas UDNs, identificadores uniformes de recursos (URI) y nombres legibles por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3d293-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="3d293-113">Información del fabricante, incluidos los nombres y las páginas web relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3d293-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="3d293-114">Información del modelo, incluidos el nombre, el número, el UPC, los números de serie y las descripciones de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d293-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="3d293-115">Mostrar información, incluida la dirección URL para controlar el dispositivo y las direcciones URL desde las que se descargan los iconos.</span><span class="sxs-lookup"><span data-stu-id="3d293-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="3d293-116">Servicios proporcionados por un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="3d293-116">Services provided by a particular device.</span></span>

<span data-ttu-id="3d293-117">Las aplicaciones también obtienen la dirección URL del documento de Descripción del dispositivo mediante la interfaz [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) .</span><span class="sxs-lookup"><span data-stu-id="3d293-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="3d293-118">A continuación, la aplicación carga el documento de Descripción y trabaja con las propiedades del dispositivo y del servicio que no se exponen mediante la interfaz [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) .</span><span class="sxs-lookup"><span data-stu-id="3d293-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="3d293-119">Esta interfaz no se puede usar en scripting porque no es la interfaz predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3d293-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="3d293-120">Ejemplo de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3d293-120">Visual Basic Example</span></span>

<span data-ttu-id="3d293-121">En el ejemplo de código siguiente se muestra el uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="3d293-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="3d293-122">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="3d293-122">C++ Example</span></span>

<span data-ttu-id="3d293-123">En el ejemplo de código siguiente se muestra el uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="3d293-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




