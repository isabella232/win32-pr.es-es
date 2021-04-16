---
description: Un objeto de bloque de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Objeto de bloque de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678421"
---
# <a name="storage-pool-object"></a><span data-ttu-id="a4b45-103">Objeto de bloque de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="a4b45-103">Storage Pool Object</span></span>

<span data-ttu-id="a4b45-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a4b45-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="a4b45-105">Un objeto de bloque de almacenamiento modela un grupo de almacenamiento en un subsistema de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a4b45-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="a4b45-106">Un grupo de almacenamiento contiene extensiones de unidad de una o varias unidades administradas por el mismo proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="a4b45-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="a4b45-107">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a4b45-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="a4b45-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4b45-108">Type</span></span>                                              | <span data-ttu-id="a4b45-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a4b45-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b45-110">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="a4b45-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="a4b45-111">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="a4b45-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a4b45-112">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="a4b45-112">Associated enumerations</span></span>                           | <span data-ttu-id="a4b45-113">[**VDS \_ \_Tipo de RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ Estado del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)y [**\_ \_ \_ tipo de grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="a4b45-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="a4b45-114">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="a4b45-114">Associated structures</span></span>                             | <span data-ttu-id="a4b45-115">[**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ atributos de grupo de VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ atributos personalizados del grupo de VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extensión de unidad del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)y [**\_ \_ \_ Prop del grupo de almacenamiento de VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="a4b45-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
