---
description: Objetos de proveedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de proveedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913953"
---
# <a name="software-provider-objects"></a><span data-ttu-id="b1a83-103">Objetos de proveedor de software</span><span class="sxs-lookup"><span data-stu-id="b1a83-103">Software Provider Objects</span></span>

<span data-ttu-id="b1a83-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b1a83-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="b1a83-105">Los objetos de proveedor de software modelan dispositivos físicos, como discos IDE y CD-ROM, y elementos virtuales como paquetes, volúmenes y complejos de volumen.</span><span class="sxs-lookup"><span data-stu-id="b1a83-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="b1a83-106">En la ilustración siguiente se muestra la relación entre el objeto de proveedor y el conjunto de objetos de proveedor de software, así como la relación entre los distintos objetos de proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="b1a83-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Diagrama que muestra la relación entre un ' proveedor ' y objetos de proveedor de software, como ' Pack ' y ' volumen '.](images/vdsswobjects.png)

<span data-ttu-id="b1a83-108">Un objeto de proveedor puede contener cero o más paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1a83-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="b1a83-109">Un objeto de paquete puede contener cero o más volúmenes y discos.</span><span class="sxs-lookup"><span data-stu-id="b1a83-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="b1a83-110">Un volumen consta de al menos un Plex de volumen y cada Plex de volumen se puede asignar a uno o varios discos, dependiendo del tipo de Plex.</span><span class="sxs-lookup"><span data-stu-id="b1a83-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="b1a83-111">VDS administra los discos sin asignar directamente, sin un contenedor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1a83-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="b1a83-112">En los temas restantes de esta sección se describen los objetos de paquete, disco, volumen y volumen.</span><span class="sxs-lookup"><span data-stu-id="b1a83-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1a83-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1a83-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a83-114">Modelo de objetos de VDS</span><span class="sxs-lookup"><span data-stu-id="b1a83-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
