---
description: La característica de particiones de COM+ incluye una memoria caché de partición. Esta memoria caché almacena las asignaciones de usuario a partición y está diseñado para evitar el acceso repetitivo Active Directory.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configuración de la memoria caché de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705377"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="e8e25-104">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="e8e25-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="e8e25-105">La característica de particiones de COM+ incluye una memoria caché de partición.</span><span class="sxs-lookup"><span data-stu-id="e8e25-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="e8e25-106">Esta memoria caché almacena las asignaciones de usuario a partición y está diseñado para evitar el acceso repetitivo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8e25-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="e8e25-107">Cambiar el tamaño de la memoria caché</span><span class="sxs-lookup"><span data-stu-id="e8e25-107">Changing Cache Size</span></span>

<span data-ttu-id="e8e25-108">La memoria caché de particiones consta de tres tablas, cuyo tamaño se puede modificar para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e8e25-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="e8e25-109">Estas tablas constan del número de entradas de SID en la memoria caché, el número de entradas de uo en la memoria caché y el número de entradas de partición en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="e8e25-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="e8e25-110">Para cambiar estos tamaños de tabla, los administradores pueden modificar los valores de una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="e8e25-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="e8e25-111">La clave del registro y sus valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8e25-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="e8e25-112">**HKLM \\ software \\ Microsoft \\ COM3 \\ PartitionCache**</span><span class="sxs-lookup"><span data-stu-id="e8e25-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="e8e25-113">Valores clave</span><span class="sxs-lookup"><span data-stu-id="e8e25-113">Key values</span></span>                         | <span data-ttu-id="e8e25-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8e25-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e25-115">**NumSidEntries**</span><span class="sxs-lookup"><span data-stu-id="e8e25-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="e8e25-116">Contiene el \_ valor de REG DWORD para el número de entradas de SID en la memoria caché (valor predeterminado = 512).</span><span class="sxs-lookup"><span data-stu-id="e8e25-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="e8e25-117">Este valor debe establecerse en un valor mayor que el número de identidades únicas en las que se atenderá una máquina en la ventana de tiempo de invalidación de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="e8e25-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e8e25-118">**NumNameEntries**</span><span class="sxs-lookup"><span data-stu-id="e8e25-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="e8e25-119">Contiene el \_ valor de REG DWORD para el número de entradas de nombre de unidad organizativa en la memoria caché (valor predeterminado = 64).</span><span class="sxs-lookup"><span data-stu-id="e8e25-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="e8e25-120">Este valor debe establecerse en un valor mayor que el número de nombres de Uo únicos en los que se atenderá un equipo en la ventana de tiempo de invalidación de caché.</span><span class="sxs-lookup"><span data-stu-id="e8e25-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="e8e25-121">**NumPartitionEntries**</span><span class="sxs-lookup"><span data-stu-id="e8e25-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="e8e25-122">Contiene el \_ valor de REG DWORD para el número de entradas de partición en la memoria caché (valor predeterminado = 1024).</span><span class="sxs-lookup"><span data-stu-id="e8e25-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="e8e25-123">En la ventana de tiempo de invalidación de caché, el valor DWORD se debe establecer en un número mayor que el número de particiones únicas en las que se atenderá un equipo.</span><span class="sxs-lookup"><span data-stu-id="e8e25-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="e8e25-124">Esto se debe a que el contexto de un componente puede incluir un identificador de partición para una partición que no reside en ese equipo.</span><span class="sxs-lookup"><span data-stu-id="e8e25-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="e8e25-125">**EntryExpiration**</span><span class="sxs-lookup"><span data-stu-id="e8e25-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="e8e25-126">Contiene el \_ valor de REG DWORD para el recuento de pasos (cada TIC = ~ 7 minutos) hasta que una entrada de caché deja de ser válida (valor predeterminado = 4 (~ 28 minutos)).</span><span class="sxs-lookup"><span data-stu-id="e8e25-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="e8e25-127">Vaciar la memoria caché</span><span class="sxs-lookup"><span data-stu-id="e8e25-127">Flushing the Cache</span></span>

<span data-ttu-id="e8e25-128">Dado que COM+ almacena en caché la partición predeterminada para los usuarios, es posible que desee llamar a este método después de cambiar la partición predeterminada para un usuario en el Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8e25-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="e8e25-129">Los administradores pueden hacerlo mediante programación llamando al método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="e8e25-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8e25-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8e25-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e25-131">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="e8e25-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="e8e25-132">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="e8e25-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="e8e25-133">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="e8e25-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="e8e25-134">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8e25-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="e8e25-135">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="e8e25-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




