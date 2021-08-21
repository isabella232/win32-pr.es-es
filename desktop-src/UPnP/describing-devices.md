---
title: Descripción de dispositivos
description: Hay dos maneras de obtener objetos de dispositivo.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e40e7f3a8d4a535771c0a670b482122d78dd7c011d6f766608270fa577e5dbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118847386"
---
# <a name="describing-devices"></a>Descripción de dispositivos

Hay dos maneras de obtener objetos de dispositivo:

-   Uso de [**la interfaz IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) La **interfaz IUPnPDescriptionDocument** es la única interfaz segura para scripting.
-   Uso de [**la interfaz IUPnPDeviceDeviceDevice Para**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) obtener una interfaz [**IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)

Ambos métodos devuelven recopilaciones de dispositivos. A continuación, las aplicaciones usan los métodos device para recuperar propiedades sobre los dispositivos.

Las aplicaciones pueden recuperar los siguientes tipos de información:

-   Información de jerarquía de dispositivos, incluidos los dispositivos raíz, los dispositivos primarios y los dispositivos secundarios.
-   Propiedades del dispositivo, incluidas las UDN, los identificadores uniformes de recursos (URI) y los nombres legibles por el usuario.
-   Información del fabricante, incluidos los nombres y las páginas web relacionadas.
-   Información del modelo, incluidos el nombre, el número, el UPC, los números de serie y las descripciones del dispositivo.
-   Muestra información, incluida la dirección URL para controlar el dispositivo y las direcciones URL desde las que se descargan los iconos.
-   Servicios proporcionados por un dispositivo determinado.

Las aplicaciones también obtienen la dirección URL del documento de descripción del dispositivo mediante la [**interfaz IUPnPDeviceDocumentAccess.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) A continuación, la aplicación carga el documento de descripción y trabaja con propiedades de dispositivo y servicio que no están expuestas por la [**interfaz IUPnPDevice.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) Esta interfaz no se puede usar en el scripting, porque no es la interfaz predeterminada.

## <a name="visual-basic-example"></a>Visual Basic Ejemplo

El código de ejemplo siguiente muestra el uso de [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



## <a name="c-example"></a>Ejemplo de C++

El código de ejemplo siguiente muestra el uso de [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



 

 




