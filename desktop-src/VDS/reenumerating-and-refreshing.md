---
description: Reenumerar y actualizar
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerar y actualizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697261"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="b87c2-103">Reenumerar y actualizar</span><span class="sxs-lookup"><span data-stu-id="b87c2-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="b87c2-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b87c2-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="b87c2-105">La operación de reenumeración detecta los dispositivos recién conectados y recién desconectados.</span><span class="sxs-lookup"><span data-stu-id="b87c2-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="b87c2-106">La operación de actualización actualiza la información de configuración de los dispositivos existentes.</span><span class="sxs-lookup"><span data-stu-id="b87c2-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="b87c2-107">**Para reenumerar objetos de proveedor de software**</span><span class="sxs-lookup"><span data-stu-id="b87c2-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="b87c2-108">Llame al método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="b87c2-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="b87c2-109">Este método detecta todos los discos y unidades de CD-ROM recién conectados y desconectados, y garantiza que todos los discos tienen el propietario adecuado.</span><span class="sxs-lookup"><span data-stu-id="b87c2-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="b87c2-110">VDS posee discos sin procesar o discos con errores. el proveedor básico posee los discos básicos; y el proveedor dinámico posee discos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b87c2-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="b87c2-111">Esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="b87c2-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="b87c2-112">**Para reenumerar y actualizar objetos de proveedor de software**</span><span class="sxs-lookup"><span data-stu-id="b87c2-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="b87c2-113">Llame al método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) y, después, llame al método [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) .</span><span class="sxs-lookup"><span data-stu-id="b87c2-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="b87c2-114">Además de detectar discos y unidades de CD-ROM recién conectados y desconectados, esta combinación de métodos actualiza toda la información de disco, volumen y Plex en la memoria caché de VDS para los discos que no se han conectado o desconectado recientemente.</span><span class="sxs-lookup"><span data-stu-id="b87c2-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="b87c2-115">Llame solo a **Actualizar** para actualizar la información de propiedades de los objetos existentes en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b87c2-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="b87c2-116">Esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="b87c2-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="b87c2-117">Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación.</span><span class="sxs-lookup"><span data-stu-id="b87c2-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="b87c2-118">Además, llamar a **Refresh** en respuesta a una notificación de VDS podría provocar que se envíe un bucle interminable de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b87c2-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="b87c2-119">Por estos motivos, solo se debe llamar a **Refresh** cuando parezca que la memoria caché no se está actualizando correctamente.</span><span class="sxs-lookup"><span data-stu-id="b87c2-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="b87c2-120">**Para reenumerar los subsistemas de hardware**</span><span class="sxs-lookup"><span data-stu-id="b87c2-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="b87c2-121">Llame al método [**IVdsHwProvider:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="b87c2-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="b87c2-122">En función del proveedor, esta operación puede implicar el envío de paquetes de red y la espera de tiempos de espera, el reexamen de buses SCSI y la espera de tiempos de espera, etc.</span><span class="sxs-lookup"><span data-stu-id="b87c2-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="b87c2-123">**Para reenumerar objetos de subsistema de hardware**</span><span class="sxs-lookup"><span data-stu-id="b87c2-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="b87c2-124">Llame al método [**IVdsSubSystem:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) para inventariar los objetos (normalmente unidades) del subsistema.</span><span class="sxs-lookup"><span data-stu-id="b87c2-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="b87c2-125">En función del subsistema, esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="b87c2-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="b87c2-126">**Para actualizar subsistemas de hardware y objetos de subsistema**</span><span class="sxs-lookup"><span data-stu-id="b87c2-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="b87c2-127">Llame al método [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) para actualizar la memoria caché de VDS de la información sobre los subsistemas existentes administrados por los proveedores de hardware de Vds.</span><span class="sxs-lookup"><span data-stu-id="b87c2-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="b87c2-128">Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación.</span><span class="sxs-lookup"><span data-stu-id="b87c2-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="b87c2-129">Además, llamar a [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) en respuesta a una notificación de VDS podría provocar que se envíe un bucle interminable de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b87c2-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="b87c2-130">Por estos motivos, solo se debe llamar a **Refresh** cuando parezca que la memoria caché no se está actualizando correctamente.</span><span class="sxs-lookup"><span data-stu-id="b87c2-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b87c2-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b87c2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b87c2-132">Uso de VDS</span><span class="sxs-lookup"><span data-stu-id="b87c2-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="b87c2-133">**IVdsService:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="b87c2-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="b87c2-134">**IVdsService:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="b87c2-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="b87c2-135">**IVdsHwProvider:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="b87c2-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="b87c2-136">**IVdsSubSystem:: reenumerar**</span><span class="sxs-lookup"><span data-stu-id="b87c2-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="b87c2-137">**IVdsHwProvider:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="b87c2-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
