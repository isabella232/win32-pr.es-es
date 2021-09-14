---
description: Establecer una conexión
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Establecer una conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251415"
---
# <a name="establishing-a-connection"></a>Establecer una conexión

Una vez que el usuario selecciona un dispositivo, la función ChooseDevice, a su vez, llama al método [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) para establecer una conexión entre la aplicación y el dispositivo. El método IPortableDevice::Open toma dos argumentos:

-   Puntero a una cadena terminada en NULL que especifica Plug and Play nombre del dispositivo. (Esta cadena se recupera mediante una llamada al [**método IPortableDeviceManager::GetDevices).**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)
-   Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) que especifica información de cliente para la aplicación.


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



Para Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) admite dos CLID para **CoCreateInstance.** **CLSID \_ PortableDevice** devuelve un **puntero IPortableDevice** que no agrega el serializador de subproceso libre; **CLSID \_ PortableDeviceFTM es** un nuevo CLSID que devuelve un puntero **IPortableDevice** que agrega el serializador de subproceso libre. De lo contrario, ambos punteros admiten la misma funcionalidad.

Las aplicaciones que se usan en un solo subproceso deben usar **CLSID \_ PortableDeviceFTM,** ya que esto elimina la sobrecarga de la serialización de punteros de interfaz. **CLSID \_ PortableDevice** sigue siendo compatible con las aplicaciones heredadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Selección de un dispositivo**](selecting-a-device.md)
</dt> </dl>

 

 



