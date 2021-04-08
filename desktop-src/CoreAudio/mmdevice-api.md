---
description: Acerca de la API de MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Acerca de la API de MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807735"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="170cb-103">Acerca de la API de MMDevice</span><span class="sxs-lookup"><span data-stu-id="170cb-103">About MMDevice API</span></span>

<span data-ttu-id="170cb-104">La API de dispositivo multimedia de Windows (MMDevice) permite a los clientes de audio detectar [dispositivos de punto de conexión de audio](audio-endpoint-devices.md), determinar sus capacidades y crear instancias de controlador para esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="170cb-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="170cb-105">El archivo de encabezado Mmdeviceapi. h define las interfaces de la API de MMDevice.</span><span class="sxs-lookup"><span data-stu-id="170cb-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="170cb-106">La API de MMDevice consta de varias interfaces.</span><span class="sxs-lookup"><span data-stu-id="170cb-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="170cb-107">La primera de ellas es la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="170cb-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="170cb-108">Para acceder a las interfaces de la API de MMDevice, un cliente obtiene una referencia a la interfaz **IMMDeviceEnumerator** de un objeto de enumerador de dispositivo mediante una llamada a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , tal como se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="170cb-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="170cb-109">En el fragmento de código anterior, CLSID \_ MMDeviceEnumerator y IID \_ IMMDeviceEnumerator son los valores GUID que se adjuntan como atributos al objeto de la clase **MMDeviceEnumerator** y a la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="170cb-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="170cb-110">La llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pasa estos valores por referencia.</span><span class="sxs-lookup"><span data-stu-id="170cb-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="170cb-111">`hr`La variable es de tipo **HRESULT** y `pEnumerator` la variable es un puntero a la interfaz **IMMDeviceEnumerator** de un objeto de enumerador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170cb-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="170cb-112">**IMMDeviceEnumerator** proporciona métodos para enumerar los dispositivos de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="170cb-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="170cb-113">Para obtener información sobre el operador **\_ \_ uuidof** , la función **CoCreateInstance** y las constantes \_ *XXX* de CLSCTX, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="170cb-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="170cb-114">A través de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , el cliente puede obtener referencias a las otras interfaces de la API de MMDevice.</span><span class="sxs-lookup"><span data-stu-id="170cb-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="170cb-115">La API de MMDevice implementa las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="170cb-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="170cb-116">Interfaz</span><span class="sxs-lookup"><span data-stu-id="170cb-116">Interface</span></span>                                          | <span data-ttu-id="170cb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="170cb-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="170cb-118">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="170cb-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="170cb-119">Representa un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="170cb-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="170cb-120">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="170cb-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="170cb-121">Representa una colección de dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="170cb-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="170cb-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="170cb-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="170cb-123">Proporciona métodos para enumerar los dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="170cb-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="170cb-124">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="170cb-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="170cb-125">Representa un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="170cb-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="170cb-126">Además, los clientes de la API de MMDevice que requieran notificación de cambios de estado en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.</span><span class="sxs-lookup"><span data-stu-id="170cb-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="170cb-127">Interfaz</span><span class="sxs-lookup"><span data-stu-id="170cb-127">Interface</span></span>                                              | <span data-ttu-id="170cb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="170cb-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="170cb-129">**IMMNotificationClient**</span><span class="sxs-lookup"><span data-stu-id="170cb-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="170cb-130">Proporciona notificaciones cuando se agrega o se quita un dispositivo de punto de conexión de audio, cuando cambia el estado o las propiedades de un dispositivo, o cuando se produce un cambio en el rol predeterminado que se asigna a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170cb-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="170cb-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="170cb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="170cb-132">Dispositivos de punto de conexión de audio</span><span class="sxs-lookup"><span data-stu-id="170cb-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="170cb-133">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="170cb-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
