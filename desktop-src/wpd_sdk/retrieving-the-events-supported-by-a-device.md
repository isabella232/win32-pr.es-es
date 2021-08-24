---
description: Recuperar los eventos admitidos por un dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recuperar los eventos admitidos por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e0e24b5a4424d03c916ca73fd0192f9b6de0a80b6a2e2e67a129deb832f7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263125"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Recuperar los eventos admitidos por un dispositivo

Algunos controladores de WPD admiten la notificación de eventos. Esto significa que una aplicación puede registrarse con el controlador para recibir una notificación cuando se produce una acción específica. Por ejemplo, una aplicación puede registrarse para recibir una notificación cuando se agrega o quita un objeto.

Hay diez eventos predefinidos que una aplicación puede supervisar. Se describen en la tabla siguiente.



| Evento                       | Descripción                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades de dispositivo actualizadas | Se produce cuando las funcionalidades del dispositivo han cambiado.                                                                                      |
| Dispositivo quitado              | Se produce cuando el dispositivo está desconectado.                                                                                                   |
| Restablecimiento del dispositivo                | Se produce cuando se ha restablecido el dispositivo.                                                                                                 |
| Objeto agregado                | Se produce después de que un nuevo objeto esté disponible en el dispositivo.                                                                             |
| Objeto quitado              | Se produce después de quitar un objeto del dispositivo.                                                                               |
| Transferencia de objetos solicitada   | Indica que se ha realizado una solicitud para transferir un objeto.                                                                          |
| Objeto actualizado              | Se produce después de actualizar un objeto o sus secundarios. (A continuación, los clientes conectados deben actualizar su vista del objeto especificado). |
| Storage en curso  | Se produce cuando se está formatendo el almacenamiento del dispositivo.                                                                                     |



 

Para obtener una lista de las constantes asociadas a estos eventos, vea el tema [Constantes de](event-constants.md) evento.

La función ListSupportedEvents del módulo DeviceCapabilities.cpp muestra la recuperación de eventos compatibles con un dispositivo determinado.

La aplicación puede recuperar los identificadores de los eventos admitidos por un dispositivo mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**IPortableDeviceCapabilities (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Proporciona acceso a los métodos de recuperación de eventos admitidos. |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para enumerar y almacenar datos de categoría funcional.     |



 

La primera tarea que realiza la aplicación de ejemplo es la recuperación de un objeto [**IPortableDeviceCapabilities,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) que se usa para recuperar los eventos admitidos por el dispositivo determinado.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



Los eventos admitidos se recuperan llamando al [**método IPortableDeviceCapabilities::GetSupportedEvents.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) Este método recupera una colección de identificadores de eventos para el dispositivo determinado y los almacena en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) al que apunta el argumento pEvents.


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



El siguiente paso consiste en recuperar el recuento de eventos admitidos para que la aplicación pueda recorrer en iteración el objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) y recuperar el identificador de cada uno.


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de evento**](event-constants.md)
</dt> <dt>

[**IPortableDevice (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



