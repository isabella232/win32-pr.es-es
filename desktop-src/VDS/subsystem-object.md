---
description: Subsystem (objeto)
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Subsystem (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562904"
---
# <a name="subsystem-object"></a><span data-ttu-id="d9f8b-103">Subsystem (objeto)</span><span class="sxs-lookup"><span data-stu-id="d9f8b-103">Subsystem Object</span></span>

<span data-ttu-id="d9f8b-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9f8b-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d9f8b-105">Un objeto de subsistema modela un subsistema de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="d9f8b-106">Un subsistema es un alojamiento RAID o una tarjeta RAID PCI.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="d9f8b-107">Un solo equipo host se puede conectar a cualquier número de subsistemas.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="d9f8b-108">Cada subsistema lo administra exactamente un proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="d9f8b-109">En una configuración de SAN, la clase de subsistema representa un contenedor de almacenamiento de SAN.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="d9f8b-110">Un subsistema puede contener cualquier número de controladores y unidades, y puede mostrar (sin máscara) cualquier número de LUN en el equipo en el que se ejecuta el proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="d9f8b-111">Los subsistemas de un extremo superior pueden desenmascarar los LUN en otros equipos de la red.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="d9f8b-112">Cada unidad de disco dentro de un subsistema está conectada a un bus y ocupa una ranura en el bus.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="d9f8b-113">Cada controlador de un subsistema tiene uno o más puertos de controlador.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="d9f8b-114">En la ilustración siguiente se muestran los dispositivos físicos contenidos en un subsistema (no se muestran los LUN) y las relaciones entre ellos.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Diagrama que muestra un subsistema que empieza por "puertos" a la izquierda, pasando a "controladores" y, a continuación, un "bus" con "ranuras" que conducen a "unidades" individuales.](images/vdssubsystem.png)

<span data-ttu-id="d9f8b-116">Las aplicaciones de VDS usan el método [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar los subsistemas que pertenecen a un proveedor de hardware específico.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="d9f8b-117">Los llamadores pueden obtener un puntero a un subsistema específico seleccionando el objeto de subsistema deseado de la enumeración devuelta por el método **QuerySubSystems** .</span><span class="sxs-lookup"><span data-stu-id="d9f8b-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="d9f8b-118">Con un objeto de subsistema, puede establecer el estado del subsistema, crear Lun, reemplazar unidades y consultar controladores, unidades y LUN.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="d9f8b-119">Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de subsistema incluyen el estado del subsistema, el estado y las marcas. un recuento de los controladores, ranuras y buses; y un valor de prioridad de recompilación.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="d9f8b-120">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d9f8b-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="d9f8b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9f8b-121">Type</span></span>                                                                                      | <span data-ttu-id="d9f8b-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9f8b-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f8b-123">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="d9f8b-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="d9f8b-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="d9f8b-125">Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0</span><span class="sxs-lookup"><span data-stu-id="d9f8b-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="d9f8b-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) y [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="d9f8b-127">Interfaces que puede exponer este objeto</span><span class="sxs-lookup"><span data-stu-id="d9f8b-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="d9f8b-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) y [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="d9f8b-129">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="d9f8b-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="d9f8b-130">[**VDS \_ \_ \_ Marca de subsistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) y [**\_ \_ \_ Estado del subsistema de VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="d9f8b-131">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="d9f8b-131">Associated structures</span></span>                                                                     | <span data-ttu-id="d9f8b-132">[**VDS \_ \_Subsistema \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) y [**la \_ \_ \_ notificación del subsistema VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span><span class="sxs-lookup"><span data-stu-id="d9f8b-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d9f8b-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9f8b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9f8b-134">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="d9f8b-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="d9f8b-135">**IVdsHwProvider::QuerySubSystems**</span><span class="sxs-lookup"><span data-stu-id="d9f8b-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
