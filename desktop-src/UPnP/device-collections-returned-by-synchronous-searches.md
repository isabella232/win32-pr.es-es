---
title: Recopilaciones de dispositivos devueltas por búsquedas sincrónicas
description: Las colecciones de dispositivos son objetos que contienen uno o varios objetos Device. Una colección de dispositivos expone la interfaz IUPnPDevices que proporciona métodos y propiedades para recorrer la colección y extraer objetos de dispositivo individuales.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94901dd2f3988327c32d7c21799ff4db7647e76fd987247e903501bd8937851a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755531"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Recopilaciones de dispositivos devueltas por búsquedas sincrónicas

Las colecciones de dispositivos son objetos que contienen uno o varios objetos Device. Una colección de dispositivos expone la [**interfaz IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) que proporciona métodos y propiedades para recorrer la colección y extraer objetos de dispositivo individuales.

## <a name="vbscript-example"></a>Ejemplo de VBScript

Las aplicaciones de VBScript pueden tener acceso a los objetos de la colección de dos maneras. En primer lugar, pueden recorrer los elementos secuencialmente mediante un para ... Cada... bucle next, como se muestra en el ejemplo siguiente:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



En este ejemplo, se supone que la variable devices se ha inicializado con el resultado de una búsqueda anterior. El bucle recorre los objetos Device de la colección y asigna a la variable deviceObj el valor de cada objeto Device a su vez. El cuerpo del bucle puede contener código que procesa el objeto Device.

## <a name="c-example"></a>Ejemplo de C++

En el ejemplo siguiente se muestra el código de C++ necesario para tener acceso a los objetos de una colección de objetos de dispositivo. La función mostrada, **TraverseCollection**, recibe un puntero a la [**interfaz IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) como parámetro de entrada. El método [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) u otros métodos **Find** podrían devolver este puntero de interfaz del objeto Device Finder.


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



El primer paso consiste en solicitar un nuevo enumerador para la colección mediante la [**\_ propiedad NewEnum.**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) Esto devuelve un enumerador como la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) El código de ejemplo invoca [**a IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener la [**interfaz IEnumVARIANT.**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) A continuación, el código de ejemplo establece el enumerador en el principio de la colección invocando el [**método IEnumVARIANT::Reset.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) Por último, el código de ejemplo invoca el [**método IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para recorrer la colección. Los objetos de dispositivo de la colección se encuentran dentro de **estructuras VARIANT.** Estas estructuras contienen punteros a [**interfaces IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en los objetos del dispositivo. Para obtener la [**interfaz IUPnPDevice,**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) el código de ejemplo invoca **QueryInterface** en la **interfaz IDispatch.**

 

 