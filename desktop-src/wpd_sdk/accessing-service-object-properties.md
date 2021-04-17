---
description: Obtener acceso a las propiedades del objeto de servicio
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Obtener acceso a las propiedades del objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696316"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="403c6-103">Obtener acceso a las propiedades del objeto de servicio</span><span class="sxs-lookup"><span data-stu-id="403c6-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="403c6-104">Una aplicación puede leer y escribir propiedades para un solo objeto en un servicio, para varios objetos identificados por identificadores de objeto o para varios objetos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="403c6-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="403c6-105">El tema [recuperar propiedades de objeto](retrieving-content-object-properties.md) describe cómo leer propiedades de un solo objeto en un servicio.</span><span class="sxs-lookup"><span data-stu-id="403c6-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="403c6-106">El tema [Writing Object Properties](writing-content-object-properties.md) describe cómo escribir propiedades para un solo objeto en un servicio.</span><span class="sxs-lookup"><span data-stu-id="403c6-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="403c6-107">Consulte la sección [tareas avanzadas](advanced-tasks.md) para obtener una descripción de la recuperación de propiedades de varios objetos.</span><span class="sxs-lookup"><span data-stu-id="403c6-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="403c6-108">Cuándo usar las definiciones de propiedad de servicio</span><span class="sxs-lookup"><span data-stu-id="403c6-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="403c6-109">Las llamadas API de WPD usadas para recuperar y establecer las propiedades de los objetos de un servicio son las mismas que las llamadas para recuperar las propiedades de los objetos de un dispositivo (Comparar "recuperar propiedades de un solo objeto" para obtener un ejemplo).</span><span class="sxs-lookup"><span data-stu-id="403c6-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="403c6-110">La diferencia clave es que se usa un conjunto diferente de PROPERTYKEYs para consultar las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="403c6-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="403c6-111">En el caso de WpdServiceApiSample, se usan los PROPERTYKEYs de servicio del dispositivo (como el **\_ \_ nombre** de la GenericObj de PKEY); para WpdApiSample, se usan los propertykeys de la WPD (como **\_ \_ el nombre del objeto WPD**).</span><span class="sxs-lookup"><span data-stu-id="403c6-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="403c6-112">Los PROPERTYKEYs de servicio de dispositivo se definen en BridgeDeviceServices. h (incluido en cada archivo de encabezado de servicio) y representan el conjunto común de los PROPERTYKEYS utilizados por las aplicaciones de servicios de dispositivos y la implementación de firmware en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="403c6-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="403c6-113">Esto permite un conjunto coherente de definiciones a lo largo de la pila de dispositivos con una traducción mínima, grupos de PROPERTYKEYs basados en el servicio y permite definir nuevos servicios más fácilmente sin tener que actualizar el esquema de WPD.</span><span class="sxs-lookup"><span data-stu-id="403c6-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="403c6-114">El conjunto de PROPERTYKEYs utilizado dependerá de las necesidades de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="403c6-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="403c6-115">Si la aplicación se comunica con el dispositivo mediante una llamada a [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use los PROPERTYKEYs definidos en PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="403c6-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="403c6-116">Un ejemplo de este tipo de aplicación es WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="403c6-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="403c6-117">Si la aplicación se comunica con los servicios de dispositivo mediante una llamada a [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use los PROPERTYKEYS definidos en BridgeDeviceServices. h.</span><span class="sxs-lookup"><span data-stu-id="403c6-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="403c6-118">Un ejemplo de este tipo de aplicación es WpdServicesApiSample.</span><span class="sxs-lookup"><span data-stu-id="403c6-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="403c6-119">Si está escribiendo una aplicación compleja que necesita admitir un híbrido de los servicios de dispositivo y el dispositivo (esto significa que la aplicación llama a **IPortableDevice:: Open** y **IPortableDeviceService:: Open**), deberá usar las propertykeys de la carga de usuario al usar IPortableDevice y sus interfaces derivadas y las propertykeys de servicio de dispositivo al usar [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) y sus interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="403c6-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="403c6-120">La mayoría de las aplicaciones de WPD deben entrar en la primera o en la segunda categoría.</span><span class="sxs-lookup"><span data-stu-id="403c6-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="403c6-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="403c6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="403c6-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="403c6-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="403c6-123">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="403c6-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="403c6-124">Recuperación de propiedades de objeto</span><span class="sxs-lookup"><span data-stu-id="403c6-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="403c6-125">Escribir propiedades de objeto</span><span class="sxs-lookup"><span data-stu-id="403c6-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="403c6-126">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="403c6-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



