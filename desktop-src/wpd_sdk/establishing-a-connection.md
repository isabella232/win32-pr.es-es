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
# <a name="establishing-a-connection"></a><span data-ttu-id="3f2db-103">Establecer una conexión</span><span class="sxs-lookup"><span data-stu-id="3f2db-103">Establishing a Connection</span></span>

<span data-ttu-id="3f2db-104">Una vez que el usuario selecciona un dispositivo, la función ChooseDevice llama a su vez al método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) para establecer una conexión entre la aplicación y el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f2db-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="3f2db-105">El método IPortableDevice:: Open toma dos argumentos:</span><span class="sxs-lookup"><span data-stu-id="3f2db-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="3f2db-106">Puntero a una cadena terminada en null que especifica el nombre Plug and Play del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f2db-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="3f2db-107">(Esta cadena se recupera llamando al método [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ).</span><span class="sxs-lookup"><span data-stu-id="3f2db-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="3f2db-108">Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) que especifica la información de cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f2db-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


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



<span data-ttu-id="3f2db-109">En Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) admite dos CLSID para **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3f2db-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="3f2db-110">**CLSID \_ de PortableDevice** devuelve un puntero **IPortableDevice** que no agrega el contador de referencias de subprocesamiento libre; **CLSID \_ de PortableDeviceFTM** es un nuevo CLSID que devuelve un puntero **IPortableDevice** que agrega el contador de referencias de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="3f2db-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="3f2db-111">Ambos punteros admiten la misma funcionalidad en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3f2db-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="3f2db-112">Las aplicaciones que residen en apartamentos de un solo subproceso deben usar **CLSID \_ PortableDeviceFTM** , ya que esto elimina la sobrecarga que supone la serialización del puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3f2db-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="3f2db-113">**CLSID \_ de PortableDevice** sigue siendo compatible con las aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="3f2db-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f2db-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f2db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f2db-115">**Selección de un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="3f2db-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



