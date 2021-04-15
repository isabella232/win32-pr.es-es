---
description: Recuperación de los eventos admitidos por un dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recuperación de los eventos admitidos por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547027"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="c3319-103">Recuperación de los eventos admitidos por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="c3319-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="c3319-104">Algunos controladores de WPD admiten la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="c3319-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="c3319-105">Esto significa que una aplicación puede registrarse con el controlador para recibir una notificación cuando se produce una acción específica.</span><span class="sxs-lookup"><span data-stu-id="c3319-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="c3319-106">Por ejemplo, una aplicación puede registrarse para recibir una notificación cuando se agrega o se quita un objeto.</span><span class="sxs-lookup"><span data-stu-id="c3319-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="c3319-107">Hay diez eventos predefinidos que una aplicación puede supervisar.</span><span class="sxs-lookup"><span data-stu-id="c3319-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="c3319-108">Se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3319-108">They are described in the following table.</span></span>



| <span data-ttu-id="c3319-109">Evento</span><span class="sxs-lookup"><span data-stu-id="c3319-109">Event</span></span>                       | <span data-ttu-id="c3319-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3319-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3319-111">Funcionalidades de dispositivo actualizadas</span><span class="sxs-lookup"><span data-stu-id="c3319-111">Device capabilities updated</span></span> | <span data-ttu-id="c3319-112">Se produce cuando han cambiado las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3319-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="c3319-113">Dispositivo quitado</span><span class="sxs-lookup"><span data-stu-id="c3319-113">Device removed</span></span>              | <span data-ttu-id="c3319-114">Se produce cuando el dispositivo está desconectado.</span><span class="sxs-lookup"><span data-stu-id="c3319-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="c3319-115">Restablecimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="c3319-115">Device reset</span></span>                | <span data-ttu-id="c3319-116">Se produce cuando se ha restablecido el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3319-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="c3319-117">Objeto agregado</span><span class="sxs-lookup"><span data-stu-id="c3319-117">Object added</span></span>                | <span data-ttu-id="c3319-118">Se produce después de que un nuevo objeto esté disponible en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3319-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="c3319-119">Objeto quitado</span><span class="sxs-lookup"><span data-stu-id="c3319-119">Object removed</span></span>              | <span data-ttu-id="c3319-120">Se produce después de quitar un objeto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3319-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="c3319-121">Transferencia de objeto solicitada</span><span class="sxs-lookup"><span data-stu-id="c3319-121">Object transfer requested</span></span>   | <span data-ttu-id="c3319-122">Indica que se ha realizado una solicitud para transferir un objeto.</span><span class="sxs-lookup"><span data-stu-id="c3319-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="c3319-123">Objeto actualizado</span><span class="sxs-lookup"><span data-stu-id="c3319-123">Object updated</span></span>              | <span data-ttu-id="c3319-124">Se produce después de la actualización de un objeto o de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c3319-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="c3319-125">(Los clientes conectados deben actualizar la vista del objeto dado).</span><span class="sxs-lookup"><span data-stu-id="c3319-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="c3319-126">Formato de almacenamiento en curso</span><span class="sxs-lookup"><span data-stu-id="c3319-126">Storage format in progress</span></span>  | <span data-ttu-id="c3319-127">Se produce cuando se está formateando el almacenamiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3319-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="c3319-128">Para obtener una lista de las constantes asociadas a estos eventos, vea el tema [constantes de evento](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="c3319-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="c3319-129">La función ListSupportedEvents del módulo DeviceCapabilities. cpp muestra la recuperación de eventos admitidos por un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="c3319-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="c3319-130">La aplicación puede recuperar los identificadores de los eventos admitidos por un dispositivo mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3319-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="c3319-131">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c3319-131">Interface</span></span>                                                                                      | <span data-ttu-id="c3319-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3319-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="c3319-133">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3319-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="c3319-134">Proporciona acceso a los métodos de recuperación de eventos admitidos.</span><span class="sxs-lookup"><span data-stu-id="c3319-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="c3319-135">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c3319-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="c3319-136">Se utiliza para enumerar y almacenar datos de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="c3319-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="c3319-137">La primera tarea que se lleva a cabo mediante la aplicación de ejemplo es la recuperación de un objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que se usa para recuperar los eventos admitidos por el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c3319-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


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



<span data-ttu-id="c3319-138">Los eventos admitidos se recuperan llamando al método [**IPortableDeviceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="c3319-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="c3319-139">Este método recupera una colección de identificadores de eventos para el dispositivo determinado y los almacena en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) al que apunta el argumento pEvents.</span><span class="sxs-lookup"><span data-stu-id="c3319-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


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



<span data-ttu-id="c3319-140">El siguiente paso consiste en recuperar el recuento de eventos admitidos para que la aplicación pueda recorrer en iteración el objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) y recuperar el identificador de cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="c3319-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c3319-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3319-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3319-142">**Constantes de evento**</span><span class="sxs-lookup"><span data-stu-id="c3319-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="c3319-143">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="c3319-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="c3319-144">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3319-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="c3319-145">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c3319-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="c3319-146">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="c3319-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



