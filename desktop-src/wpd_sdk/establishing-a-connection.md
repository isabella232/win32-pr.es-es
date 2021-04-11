---
description: Establecer una conexión
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Establecer una conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083448"
---
# <a name="establishing-a-connection"></a>Establecer una conexión

Una vez que el usuario selecciona un dispositivo, la función ChooseDevice llama a su vez al método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) para establecer una conexión entre la aplicación y el dispositivo. El método IPortableDevice:: Open toma dos argumentos:

-   Puntero a una cadena terminada en null que especifica el nombre Plug and Play del dispositivo. (Esta cadena se recupera llamando al método [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ).
-   Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) que especifica la información de cliente de la aplicación.


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



En Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) admite dos CLSID para **CoCreateInstance**. **CLSID \_ de PortableDevice** devuelve un puntero **IPortableDevice** que no agrega el contador de referencias de subprocesamiento libre; **CLSID \_ de PortableDeviceFTM** es un nuevo CLSID que devuelve un puntero **IPortableDevice** que agrega el contador de referencias de subprocesamiento libre. Ambos punteros admiten la misma funcionalidad en caso contrario.

Las aplicaciones que residen en apartamentos de un solo subproceso deben usar **CLSID \_ PortableDeviceFTM** , ya que esto elimina la sobrecarga que supone la serialización del puntero de interfaz. **CLSID \_ de PortableDevice** sigue siendo compatible con las aplicaciones heredadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Selección de un dispositivo**](selecting-a-device.md)
</dt> </dl>

 

 



