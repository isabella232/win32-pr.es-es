---
title: Enumerar dispositivos (WPD)
description: Enumerar dispositivos
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2738398de7f3bfb6aa1ea88175ff30241b4dbb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697805"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="e1e76-103">Enumerar dispositivos (WPD)</span><span class="sxs-lookup"><span data-stu-id="e1e76-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="e1e76-104">La primera tarea completada por la mayoría de las aplicaciones es la enumeración de los dispositivos conectados al equipo.</span><span class="sxs-lookup"><span data-stu-id="e1e76-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="e1e76-105">Esta tarea y la recuperación de información del dispositivo (como fabricante, nombre descriptivo y descripción) se admiten en la interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="e1e76-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="e1e76-106">La función EnumerateAllDevices del módulo DeviceEnumeration. cpp contiene código que muestra la recuperación del recuento de dispositivos conectados y, una vez que se recupera el recuento, la recuperación de información específica del dispositivo para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="e1e76-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="e1e76-107">La función EnumerateAllDevices realiza cuatro tareas principales:</span><span class="sxs-lookup"><span data-stu-id="e1e76-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="e1e76-108">Crea el objeto portable Device Manager.</span><span class="sxs-lookup"><span data-stu-id="e1e76-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="e1e76-109">Recupera un recuento de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="e1e76-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="e1e76-110">Recupera información del dispositivo (para los dispositivos conectados).</span><span class="sxs-lookup"><span data-stu-id="e1e76-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="e1e76-111">Libera la memoria usada al recuperar la información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1e76-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="e1e76-112">Cada una de estas cuatro tareas se describe con más detalle en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="e1e76-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="e1e76-113">El primer paso en el proceso de enumeración de dispositivos es la creación de un objeto portable Device Manager.</span><span class="sxs-lookup"><span data-stu-id="e1e76-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="e1e76-114">Esto se hace llamando a la función CoCreateInstance y pasando el identificador de clase (CLSID) para el objeto, especificando el contexto en el que se ejecutará el código, especificando un identificador de referencia para la interfaz IPortableDeviceManager y proporcionando después una variable de puntero que recibe el puntero de la interfaz IPortableDeviceManager.</span><span class="sxs-lookup"><span data-stu-id="e1e76-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


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



<span data-ttu-id="e1e76-115">Una vez que obtenga un puntero de interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) , puede empezar a llamar a métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="e1e76-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="e1e76-116">El primer método llamado en la función EnumerateAllDevices es [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span><span class="sxs-lookup"><span data-stu-id="e1e76-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="e1e76-117">Cuando se llama a este método con el primer argumento establecido en **null**, devuelve el recuento de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="e1e76-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


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



<span data-ttu-id="e1e76-118">Una vez que haya recuperado el número de dispositivos conectados, puede usar este valor para recuperar la información del dispositivo para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="e1e76-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="e1e76-119">Este proceso comienza pasando una matriz de punteros de cadena como primer argumento y un recuento del número de elementos que esta matriz puede contener como segundo argumento (este recuento debe ser al menos igual que el número de dispositivos disponibles).</span><span class="sxs-lookup"><span data-stu-id="e1e76-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="e1e76-120">Las cadenas devueltas por este método son los nombres de Plug and Play de los dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="e1e76-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="e1e76-121">Estos nombres, a su vez, se pasan a otros métodos de la interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) para recuperar información específica del dispositivo, como el nombre descriptivo, el nombre del fabricante y la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1e76-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="e1e76-122">(Estos nombres también se usan para abrir una conexión al dispositivo cuando una aplicación llama al método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) ).</span><span class="sxs-lookup"><span data-stu-id="e1e76-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


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



<span data-ttu-id="e1e76-123">Una vez que haya recuperado la información del dispositivo, tendrá que liberar la memoria asociada a las cadenas a las que apunta la matriz de punteros de cadena.</span><span class="sxs-lookup"><span data-stu-id="e1e76-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="e1e76-124">También tendrá que eliminar esta matriz.</span><span class="sxs-lookup"><span data-stu-id="e1e76-124">You will also need to delete this array.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e1e76-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1e76-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e76-126">**Interfaz IPortableDeviceManager**</span><span class="sxs-lookup"><span data-stu-id="e1e76-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="e1e76-127">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="e1e76-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



