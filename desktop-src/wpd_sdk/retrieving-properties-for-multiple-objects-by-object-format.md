---
description: Recuperar propiedades de varios objetos por formato de objeto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recuperar propiedades de varios objetos por formato de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497848"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="b2af8-103">Recuperar propiedades de varios objetos por formato de objeto</span><span class="sxs-lookup"><span data-stu-id="b2af8-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="b2af8-104">Además de una recuperación masiva de las propiedades de una colección de identificadores de objeto, una aplicación también puede realizar una recuperación masiva de propiedades para todos los objetos de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="b2af8-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="b2af8-105">Como en el ejemplo anterior, la recuperación masiva para un tipo determinado requiere que el controlador de dispositivo admita recuperaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="b2af8-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="b2af8-106">La aplicación puede realizar una recuperación masiva con las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b2af8-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="b2af8-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b2af8-107">Interface</span></span>                                                                                      | <span data-ttu-id="b2af8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2af8-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="b2af8-109">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b2af8-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="b2af8-110">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="b2af8-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="b2af8-111">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="b2af8-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="b2af8-112">Se utiliza para identificar las propiedades que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b2af8-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="b2af8-113">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b2af8-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="b2af8-114">Se utiliza para determinar si un controlador determinado admite operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="b2af8-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="b2af8-115">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b2af8-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="b2af8-116">Admite la operación de recuperación masiva.</span><span class="sxs-lookup"><span data-stu-id="b2af8-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="b2af8-117">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b2af8-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b2af8-118">Se utiliza para almacenar los identificadores de objeto para la operación masiva.</span><span class="sxs-lookup"><span data-stu-id="b2af8-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="b2af8-119">La función ReadContentPropertiesBulkFilteringFormat del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de recuperación masiva para objetos de un tipo o formato determinado.</span><span class="sxs-lookup"><span data-stu-id="b2af8-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="b2af8-120">El código que se encuentra en la función ReadContentPropertiesBulkFilteringFormat es casi idéntico al código que se encuentra en la función ReadContentPropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="b2af8-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="b2af8-121">(Vea el tema [recuperar propiedades de varios objetos](retrieving-properties-for-multiple-objects.md) para obtener una descripción completa de esta función).</span><span class="sxs-lookup"><span data-stu-id="b2af8-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="b2af8-122">La diferencia principal se produce cuando la operación se pone en cola.</span><span class="sxs-lookup"><span data-stu-id="b2af8-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="b2af8-123">Al filtrar por tipo o formato, se llama al método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) en lugar del método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="b2af8-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="b2af8-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2af8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2af8-125">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="b2af8-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b2af8-126">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b2af8-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="b2af8-127">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="b2af8-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="b2af8-128">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b2af8-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="b2af8-129">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b2af8-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="b2af8-130">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b2af8-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="b2af8-131">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="b2af8-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



