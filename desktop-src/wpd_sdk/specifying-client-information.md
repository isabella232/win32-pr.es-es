---
description: Especificar información de cliente
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Especificar información de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278316"
---
# <a name="specifying-client-information"></a><span data-ttu-id="c9f42-103">Especificar información de cliente</span><span class="sxs-lookup"><span data-stu-id="c9f42-103">Specifying Client Information</span></span>

<span data-ttu-id="c9f42-104">Algunos controladores de dispositivos usan la información de cliente proporcionada en el segundo argumento para optimizar el rendimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9f42-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="c9f42-105">Como mínimo, la aplicación debe proporcionar una cadena que contenga su nombre, un número de versión principal, un número de versión secundaria y un número de revisión.</span><span class="sxs-lookup"><span data-stu-id="c9f42-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="c9f42-106">Estos son los campos proporcionados por la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c9f42-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="c9f42-107">La `GetClientInformation` función de la aplicación de ejemplo crea y rellena una interfaz **IPortableDeviceValues** con la información del cliente.</span><span class="sxs-lookup"><span data-stu-id="c9f42-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="c9f42-108">Esta función tiene dos partes principales.</span><span class="sxs-lookup"><span data-stu-id="c9f42-108">This function has two primary parts.</span></span> <span data-ttu-id="c9f42-109">La primera parte crea una instancia de un objeto de valores de dispositivo portable mediante una llamada a la función CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="c9f42-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="c9f42-110">La segunda parte establece la información del cliente en el objeto de valores de dispositivo portable.</span><span class="sxs-lookup"><span data-stu-id="c9f42-110">The second part sets the client information in the portable device-values object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="c9f42-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9f42-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f42-112">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="c9f42-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="c9f42-113">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c9f42-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c9f42-114">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="c9f42-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



