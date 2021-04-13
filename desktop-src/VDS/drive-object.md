---
description: Drive (objeto)
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Drive (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276983"
---
# <a name="drive-object"></a><span data-ttu-id="acb3f-103">Drive (objeto)</span><span class="sxs-lookup"><span data-stu-id="acb3f-103">Drive Object</span></span>

<span data-ttu-id="acb3f-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="acb3f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="acb3f-105">Un objeto de unidad modela una unidad de disco física incluida en un subsistema.</span><span class="sxs-lookup"><span data-stu-id="acb3f-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="acb3f-106">Cada unidad se conecta a un bus, ocupa una ranura y contiene un conjunto de extensiones de unidad.</span><span class="sxs-lookup"><span data-stu-id="acb3f-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="acb3f-107">Cada unidad puede aportar extensiones a cualquier número de LUN.</span><span class="sxs-lookup"><span data-stu-id="acb3f-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="acb3f-108">También se puede designar una unidad como reserva activa.</span><span class="sxs-lookup"><span data-stu-id="acb3f-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="acb3f-109">Use el método [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar las unidades que contiene un subsistema específico.</span><span class="sxs-lookup"><span data-stu-id="acb3f-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="acb3f-110">Los llamadores pueden obtener un puntero a una unidad específica seleccionando el objeto de unidad deseado de la enumeración devuelta por el método **QueryDrives** o invocando el método [**IVdsSubSystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) y pasando el bus y el número de ranura deseados.</span><span class="sxs-lookup"><span data-stu-id="acb3f-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="acb3f-111">Con un objeto de unidad, puede establecer el estado de la unidad y la consulta de las propiedades de la unidad, las extensiones de unidad asociadas y el subsistema que contiene la unidad.</span><span class="sxs-lookup"><span data-stu-id="acb3f-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="acb3f-112">Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de unidad incluyen el estado de la unidad, el estado y las marcas; tamaño en bytes; y un número de bus y ranura.</span><span class="sxs-lookup"><span data-stu-id="acb3f-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="acb3f-113">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="acb3f-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="acb3f-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="acb3f-114">Type</span></span>                                              | <span data-ttu-id="acb3f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="acb3f-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acb3f-116">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="acb3f-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="acb3f-117">**IVdsDrive**</span><span class="sxs-lookup"><span data-stu-id="acb3f-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="acb3f-118">Interfaces que puede exponer este objeto</span><span class="sxs-lookup"><span data-stu-id="acb3f-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="acb3f-119">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="acb3f-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="acb3f-120">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="acb3f-120">Associated enumerations</span></span>                           | <span data-ttu-id="acb3f-121">[**VDS \_ \_Marca de unidad**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ Estado de unidad de VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)y [**\_ \_ extensión de unidad de VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span><span class="sxs-lookup"><span data-stu-id="acb3f-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="acb3f-122">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="acb3f-122">Associated structures</span></span>                             | <span data-ttu-id="acb3f-123">[**VDS \_ GENERAR \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) una [**notificación de \_ unidad \_ de disco**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)y de Prop.</span><span class="sxs-lookup"><span data-stu-id="acb3f-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="acb3f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acb3f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acb3f-125">Objetos de proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="acb3f-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="acb3f-126">**IVdsSubSystem::QueryDrives**</span><span class="sxs-lookup"><span data-stu-id="acb3f-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="acb3f-127">**IVdsSubSystem::GetDrive**</span><span class="sxs-lookup"><span data-stu-id="acb3f-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
