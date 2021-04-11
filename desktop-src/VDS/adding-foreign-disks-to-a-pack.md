---
description: Adición de discos externos a un paquete
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Adición de discos externos a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361455"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="f3513-103">Adición de discos externos a un paquete</span><span class="sxs-lookup"><span data-stu-id="f3513-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="f3513-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3513-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f3513-105">Normalmente, un disco externo es un disco dinámico que se asigna en un equipo y se mueve físicamente a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="f3513-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="f3513-106">Sin embargo, cualquier disco que pertenezca a un paquete que no sea el paquete en línea se considera un disco externo que pertenece a un paquete de disco externo.</span><span class="sxs-lookup"><span data-stu-id="f3513-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="f3513-107">Un paquete externo tiene la **marca \_ \_ Foreign PKF de VDS** establecida en el miembro **ulFlags** de la estructura de [**\_ \_ propiedades del paquete VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) .</span><span class="sxs-lookup"><span data-stu-id="f3513-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="f3513-108">Los paquetes externos siempre están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f3513-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="f3513-109">En el procedimiento siguiente se describe cómo importar uno o varios discos externos.</span><span class="sxs-lookup"><span data-stu-id="f3513-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="f3513-110">**Para importar uno o varios discos externos**</span><span class="sxs-lookup"><span data-stu-id="f3513-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="f3513-111">Mueva los discos al nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="f3513-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="f3513-112">En el nuevo equipo, use el método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) para instalar los discos externos.</span><span class="sxs-lookup"><span data-stu-id="f3513-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="f3513-113">Seleccione el paquete en línea para que sea el paquete de destino que recibe los discos externos.</span><span class="sxs-lookup"><span data-stu-id="f3513-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="f3513-114">Si no existe ningún paquete en línea, use el método [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un nuevo paquete vacío.</span><span class="sxs-lookup"><span data-stu-id="f3513-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="f3513-115">Use el método [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) para importar los discos al nuevo paquete dinámico.</span><span class="sxs-lookup"><span data-stu-id="f3513-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="f3513-116">Use el método [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) para enumerar los packs y [**IVdsPack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) para determinar qué paquete es ahora el paquete en línea.</span><span class="sxs-lookup"><span data-stu-id="f3513-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="f3513-117">Si crea un nuevo paquete de destino vacío, los discos externos no se migran realmente a ese paquete.</span><span class="sxs-lookup"><span data-stu-id="f3513-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="f3513-118">En su lugar, el paquete externo se marca como en línea, la marca **\_ \_ externa de VDS PKF** para el paquete está desactivada (por lo que el paquete ya no es externo) y se descarta el paquete de destino que creó.</span><span class="sxs-lookup"><span data-stu-id="f3513-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="f3513-119">Use el método [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar a un paquete discos sin asignar (discos no reclamados por un proveedor).</span><span class="sxs-lookup"><span data-stu-id="f3513-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="f3513-120">Un disco sin asignar no puede ser externo.</span><span class="sxs-lookup"><span data-stu-id="f3513-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3513-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3513-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3513-122">Uso de VDS</span><span class="sxs-lookup"><span data-stu-id="f3513-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="f3513-123">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="f3513-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="f3513-124">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="f3513-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="f3513-125">**IVdsPack::MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="f3513-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="f3513-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="f3513-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
