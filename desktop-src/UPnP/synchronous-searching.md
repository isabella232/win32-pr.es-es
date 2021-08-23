---
title: Búsqueda sincrónica
description: El objeto Device Finder permite realizar búsquedas sincrónicas y asincrónicas. Las búsquedas sincrónicas se completan y devuelven el control a la aplicación que realiza la llamada solo después de encontrar todos los dispositivos disponibles.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f852957bed4bb73d9b31d0e26e099eb545b804953718d8cfd4e3cb44ea5f6c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999505"
---
# <a name="synchronous-searching"></a>Búsqueda sincrónica

El objeto Device Finder permite realizar búsquedas sincrónicas y asincrónicas. Las búsquedas sincrónicas se completan y devuelven el control a la aplicación que realiza la llamada solo después de encontrar todos los dispositivos disponibles. Para realizar una búsqueda sincrónica, use uno de los métodos de búsqueda sincrónicos de la [**interfaz IUPnPDeviceDevice.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)

> [!Note]  
> Las búsquedas sincrónicas tardarán al menos nueve segundos en devolverse. El retraso se debe a que el mensaje de búsqueda UDP inicial se debe enviar varias veces. Esta duplicación tiene en cuenta la falta de responsabilidad del protocolo de red subyacente. Las búsquedas sincrónicas son las más recomendadas para las interfaces de línea de comandos. No se recomiendan para interfaces gráficas de usuario.

 

El [**método IUPnPDeviceDevice::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) busca por tipo de dispositivo o servicio. Este método toma un URI de tipo como parámetro de entrada y devuelve una colección de objetos Device. Un objeto Device representa un dispositivo individual.

En los ejemplos siguientes se muestra cómo realizar una búsqueda sincrónica de dispositivos en VBScript. Cada script usa [**IUPnPDeviceDevice::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), al que se llama con el uri de tipo (identificador de servicio) para el tipo de dispositivo del reproductor multimedia, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*. El método devuelve una colección de objetos Device que corresponde a los dispositivos del reproductor multimedia que se encontraron. Para obtener información sobre cómo extraer objetos de dispositivo individuales de una colección, vea [Recopilaciones de dispositivos devueltas por búsquedas sincrónicas.](device-collections-returned-by-synchronous-searches.md)

## <a name="search-for-devices-by-type-in-vbscript"></a>Buscar dispositivos por tipo en VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Buscar dispositivo por tipo en C++

En el ejemplo siguiente se muestra una búsqueda sincrónica de dispositivos del reproductor multimedia con C++. La función toma un puntero a la [**interfaz IUPnPDeviceDeviceDevice Como**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) entrada y devuelve el puntero de interfaz [**IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)

En primer lugar, el ejemplo asigna un **BSTR** para representar el URI del tipo de dispositivo y, a continuación, lo pasa al método [**IUPnPDeviceDevice::FindByType.**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) También pasa la dirección de un puntero [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local en el búfer en el que el método almacena la colección de dispositivos encontrados. Si la llamada a la función se realiza correctamente, devuelve el puntero a esta colección.


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



 

 




