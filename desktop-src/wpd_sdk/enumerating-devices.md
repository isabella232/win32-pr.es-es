---
title: Enumeración de dispositivos (WPD)
description: Obtenga información sobre cómo una aplicación enumera los dispositivos mediante la función EnumerateAllDevices, que obtiene un recuento de dispositivos conectados e información específica del dispositivo.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cfe1c1b4dee11383a4c36eaea43974f7e0439ae4ff2370a90e99b1702a8e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083579"
---
# <a name="enumerating-devices-wpd"></a>Enumeración de dispositivos (WPD)

La primera tarea completada por la mayoría de las aplicaciones es la enumeración de los dispositivos conectados al equipo. Esta tarea y la recuperación de información del dispositivo (por ejemplo, fabricante, nombre descriptivo y descripción) son compatibles con la [**interfaz IPortableDeviceManager.**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)

La función EnumerateAllDevices del módulo DeviceEnumeration.cpp contiene código que muestra la recuperación del recuento de dispositivos conectados y, una vez recuperado el recuento, la recuperación de información específica del dispositivo para cada dispositivo conectado.

La función EnumerateAllDevices realiza cuatro tareas principales:

1.  Crea el objeto de administrador de dispositivos portátil.
2.  Recupera un recuento de dispositivos conectados.
3.  Recupera la información del dispositivo (para los dispositivos conectados).
4.  Libera la memoria usada al recuperar la información del dispositivo.

Cada una de estas cuatro tareas se describe con más detalle en las secciones siguientes.

El primer paso del proceso de enumeración de dispositivos es la creación de un objeto de administrador de dispositivos portátil. Para ello, se llama a la función CoCreateInstance y se pasa el identificador de clase (CLSID) para el objeto, se especifica el contexto en el que se ejecutará el código, se especifica un identificador de referencia para la interfaz IPortableDeviceManager y, a continuación, se proporciona una variable de puntero que recibe el puntero de interfaz IPortableDeviceManager.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



Una vez que obtenga un [**puntero de interfaz IPortableDeviceManager,**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) puede empezar a llamar a métodos en esta interfaz. El primer método llamado en la función EnumerateAllDevices [**es IPortableDeviceManager::GetDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) Cuando se llama a este método con el primer argumento establecido en **NULL,** devuelve el recuento de dispositivos conectados.


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



Después de recuperar el recuento de dispositivos conectados, puede usar este valor para recuperar la información del dispositivo para cada dispositivo conectado. Este proceso comienza pasando una matriz de punteros de cadena como primer argumento y un recuento del número de elementos que esta matriz puede contener como segundo argumento (este recuento debe ser al menos igual al número de dispositivos disponibles).

Las cadenas devueltas por este método son los Plug and Play de los dispositivos conectados. Estos nombres, a su vez, se pasan a otros métodos de la interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) para recuperar información específica del dispositivo, como el nombre descriptivo, el nombre del fabricante y la descripción del dispositivo. (Estos nombres también se usan para abrir una conexión al dispositivo cuando una aplicación llama al método [**IPortableDevice::Open).**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



Una vez que haya recuperado la información del dispositivo, deberá liberar la memoria asociada a las cadenas a las que apunta la matriz de punteros de cadena. También tendrá que eliminar esta matriz.


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceManager (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



