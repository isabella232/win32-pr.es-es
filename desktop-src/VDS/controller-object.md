---
description: Controller (objeto)
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571424"
---
# <a name="controller-object"></a><span data-ttu-id="90026-103">Controller (objeto)</span><span class="sxs-lookup"><span data-stu-id="90026-103">Controller Object</span></span>

<span data-ttu-id="90026-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="90026-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="90026-105">Un objeto de controlador modela un controlador en un subsistema.</span><span class="sxs-lookup"><span data-stu-id="90026-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="90026-106">Los subsistemas contienen controladores y cada controlador tiene uno o más puertos de controlador a través de los cuales el equipo host puede escribir y leer en los LUN.</span><span class="sxs-lookup"><span data-stu-id="90026-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="90026-107">Un solo controlador se puede establecer simultáneamente en activo para un LUN e inactivo para otros.</span><span class="sxs-lookup"><span data-stu-id="90026-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="90026-108">Un controlador que está activo para un LUN especificado conlleva la responsabilidad de controlar la entrada y la salida del LUN.</span><span class="sxs-lookup"><span data-stu-id="90026-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="90026-109">En la ilustración siguiente se muestra esta idea.</span><span class="sxs-lookup"><span data-stu-id="90026-109">The following figure illustrates this idea.</span></span>

![Diagrama que muestra un ' controlador ' con un LUN activo a la izquierda y dos LUN activos a la derecha.](images/vdscontroller.png)

<span data-ttu-id="90026-111">**VDS 1,0:** Cada uno de los controladores de un subsistema se establece en activo o inactivo con respecto a cada uno de los LUN que el subsistema Surfaces.</span><span class="sxs-lookup"><span data-stu-id="90026-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="90026-112">Las aplicaciones de VDS usan el método [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) para determinar los controladores que se incluyen en un subsistema específico.</span><span class="sxs-lookup"><span data-stu-id="90026-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="90026-113">Los llamadores pueden obtener un puntero a un controlador específico seleccionando el objeto de controlador deseado de la enumeración devuelta por el método **QueryControllers** .</span><span class="sxs-lookup"><span data-stu-id="90026-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="90026-114">Con un objeto de controlador, un llamador puede establecer el estado del controlador, consultar los LUN asociados, consultar sus puertos de controlador y vaciar e invalidar la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="90026-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="90026-115">Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de controlador incluyen el estado y el estado del controlador, así como un recuento de los puertos.</span><span class="sxs-lookup"><span data-stu-id="90026-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="90026-116">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="90026-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="90026-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="90026-117">Type</span></span>                                                                                              | <span data-ttu-id="90026-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="90026-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90026-119">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="90026-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="90026-120">**IVdsController**</span><span class="sxs-lookup"><span data-stu-id="90026-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="90026-121">Interfaces que siempre expone este objeto en VDS 1,1 y 2,0 Canal de fibra proveedores</span><span class="sxs-lookup"><span data-stu-id="90026-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="90026-122">**IVdsControllerControllerPort**</span><span class="sxs-lookup"><span data-stu-id="90026-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="90026-123">Interfaces que puede exponer este objeto</span><span class="sxs-lookup"><span data-stu-id="90026-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="90026-124">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="90026-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="90026-125">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="90026-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="90026-126">[**VDS \_ \_Estado del controlador**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="90026-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="90026-127">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="90026-127">Associated structures</span></span>                                                                             | <span data-ttu-id="90026-128">[**VDS \_ Notificación \_ de controlador**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) de VDS y de controlador de [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span><span class="sxs-lookup"><span data-stu-id="90026-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="90026-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90026-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90026-130">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="90026-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="90026-131">**IVdsSubSystem::QueryControllers**</span><span class="sxs-lookup"><span data-stu-id="90026-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
