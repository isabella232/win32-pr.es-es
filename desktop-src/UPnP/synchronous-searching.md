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
# <a name="synchronous-searching"></a>Búsqueda sincrónica

El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas. Las búsquedas sincrónicas se completan y devuelven el control a la aplicación que realiza la llamada solo después de encontrar todos los dispositivos disponibles. Para realizar una búsqueda sincrónica, use uno de los métodos de búsqueda sincrónicos de la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .

> [!Note]  
> Las búsquedas sincrónicas tardan al menos nueve segundos en devolverse. El retraso se debe a que el mensaje de búsqueda UDP inicial se debe enviar varias veces. Esta duplicación tiene en cuenta la no confiabilidad del Protocolo de red subyacente. Las búsquedas sincrónicas son más adecuadas para las interfaces de línea de comandos. No se recomiendan para las interfaces de usuario gráficas.

 

El método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) busca por dispositivo o tipo de servicio. Este método toma un URI de tipo como parámetro de entrada y devuelve una colección de objetos de dispositivo. Un objeto de dispositivo representa un dispositivo individual.

En los siguientes ejemplos se muestra cómo realizar una búsqueda sincrónica de dispositivos en VBScript. Cada script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), llamado con el URI de tipo (identificador de servicio) para el tipo de dispositivo del reproductor de media, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*. El método devuelve una colección de objetos de dispositivo que corresponde a los dispositivos del reproductor de media que se encontraron. Para obtener información sobre cómo extraer objetos de dispositivo individuales de una colección, consulte [colecciones de dispositivos devueltas por búsquedas sincrónicas](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Buscar dispositivos por tipo en VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Buscar dispositivo por tipo en C++

En el ejemplo siguiente se muestra una búsqueda sincrónica de dispositivos del reproductor de media con C++. La función toma un puntero a la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) como entrada y devuelve el puntero de la interfaz [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

En primer lugar, el ejemplo asigna un **BSTR** para representar el URI de tipo de dispositivo y, a continuación, lo pasa al método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) . También pasa la dirección de un puntero [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local en el búfer en el que el método almacena la colección de dispositivos encontrados. Si la llamada de función se realiza correctamente, devuelve el puntero a esta colección.


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



 

 




