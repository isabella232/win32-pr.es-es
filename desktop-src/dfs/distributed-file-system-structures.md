---
description: A continuación se muestran las Sistema de archivos distribuido estructuras DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Sistema de archivos distribuido estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496582"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="54b14-103">Sistema de archivos distribuido estructuras</span><span class="sxs-lookup"><span data-stu-id="54b14-103">Distributed File System Structures</span></span>

<span data-ttu-id="54b14-104">A continuación se muestran las estructuras Sistema de archivos distribuido (DFS):</span><span class="sxs-lookup"><span data-stu-id="54b14-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54b14-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="54b14-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="54b14-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="54b14-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="54b14-107">Búfer de entrada utilizado con el código de control de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)</span><span class="sxs-lookup"><span data-stu-id="54b14-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="54b14-108">Estructura de _DFS_INFO_1</span><span class="sxs-lookup"><span data-stu-id="54b14-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="54b14-109">Contiene el nombre de una raíz o vínculo de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-110">Estructura de _DFS_INFO_2</span><span class="sxs-lookup"><span data-stu-id="54b14-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="54b14-111">Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="54b14-112">Esta estructura contiene el nombre, el estado y el número de destinos DFS para la raíz o el vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-113">Estructura de _DFS_INFO_3</span><span class="sxs-lookup"><span data-stu-id="54b14-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="54b14-114">Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="54b14-115">Esta estructura contiene el nombre, el estado, el número de destinos DFS e información sobre cada destino de la raíz o vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-116">Estructura de _DFS_INFO_4</span><span class="sxs-lookup"><span data-stu-id="54b14-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="54b14-117">Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="54b14-118">Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, el número de destinos e información sobre cada destino de la raíz o el vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-119">Estructura de _DFS_INFO_5</span><span class="sxs-lookup"><span data-stu-id="54b14-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="54b14-120">Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="54b14-121">Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, las propiedades de espacio de nombres/raíz/vínculo, el tamaño de los metadatos y el número de destinos para la raíz o el vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-122">Estructura de _DFS_INFO_6</span><span class="sxs-lookup"><span data-stu-id="54b14-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="54b14-123">Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="54b14-124">Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, las propiedades de espacio de nombres/raíz/vínculo, el tamaño de los metadatos, el número de destinos e información sobre cada destino de la raíz o el vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-125">Estructura de _DFS_INFO_7</span><span class="sxs-lookup"><span data-stu-id="54b14-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="54b14-126">Contiene información sobre un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="54b14-127">Esta estructura contiene el **GUID** de la versión de los metadatos para el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="54b14-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-128">Estructura de _DFS_INFO_8</span><span class="sxs-lookup"><span data-stu-id="54b14-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="54b14-129">Contiene el nombre, el estado, el **GUID**, el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS y el descriptor de seguridad del punto de análisis de vínculos para una raíz o vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-130">Estructura de _DFS_INFO_9</span><span class="sxs-lookup"><span data-stu-id="54b14-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="54b14-131">Contiene el nombre, el estado, el **GUID**, el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS, el descriptor de seguridad del punto de reanálisis de vínculos y una lista de destinos DFS para un vínculo o raíz.</span><span class="sxs-lookup"><span data-stu-id="54b14-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-132">Estructura de _DFS_INFO_50</span><span class="sxs-lookup"><span data-stu-id="54b14-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="54b14-133">Contiene la versión de metadatos de DFS y las capacidades de un espacio de nombres DFS existente.</span><span class="sxs-lookup"><span data-stu-id="54b14-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-134">Estructura de _DFS_INFO_100</span><span class="sxs-lookup"><span data-stu-id="54b14-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="54b14-135">Contiene un comentario asociado a una raíz o vínculo de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-136">Estructura de _DFS_INFO_101</span><span class="sxs-lookup"><span data-stu-id="54b14-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="54b14-137">Describe el estado de almacenamiento en una raíz DFS, un vínculo, un destino raíz o un destino de vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-138">Estructura de _DFS_INFO_102</span><span class="sxs-lookup"><span data-stu-id="54b14-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="54b14-139">Contiene un valor de tiempo de espera para asociar a una raíz de Sistema de archivos distribuido (DFS) o un vínculo en una raíz DFS con nombre.</span><span class="sxs-lookup"><span data-stu-id="54b14-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-140">Estructura de _DFS_INFO_103</span><span class="sxs-lookup"><span data-stu-id="54b14-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="54b14-141">Contiene propiedades que establecen comportamientos específicos para una raíz o vínculo DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-142">Estructura de _DFS_INFO_104</span><span class="sxs-lookup"><span data-stu-id="54b14-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="54b14-143">Contiene la prioridad de un destino de raíz DFS o destino de vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-144">Estructura de _DFS_INFO_105</span><span class="sxs-lookup"><span data-stu-id="54b14-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="54b14-145">Contiene información sobre una raíz o vínculo DFS, incluidos los comportamientos de comentario, estado, tiempo de espera y DFS especificados por las marcas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="54b14-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-146">Estructura de _DFS_INFO_106</span><span class="sxs-lookup"><span data-stu-id="54b14-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="54b14-147">Contiene el estado y la prioridad de almacenamiento de un destino de raíz DFS o destino de vínculo.</span><span class="sxs-lookup"><span data-stu-id="54b14-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="54b14-148">Esta estructura solo se usa con la función [**NetDfsSetInfo**](netdfssetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="54b14-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-149">Estructura de _DFS_INFO_107</span><span class="sxs-lookup"><span data-stu-id="54b14-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="54b14-150">Contiene información acerca de una raíz o vínculo DFS, incluidos los comentarios, el estado, el tiempo de espera, las marcas de propiedad y el descriptor de seguridad del punto de reanálisis de vínculos.</span><span class="sxs-lookup"><span data-stu-id="54b14-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-151">Estructura de _DFS_INFO_150</span><span class="sxs-lookup"><span data-stu-id="54b14-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="54b14-152">Contiene el descriptor de seguridad para el punto de reanálisis de un vínculo DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-153">Estructura de _DFS_INFO_200</span><span class="sxs-lookup"><span data-stu-id="54b14-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="54b14-154">Contiene el nombre de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="54b14-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-155">Estructura de _DFS_INFO_300</span><span class="sxs-lookup"><span data-stu-id="54b14-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="54b14-156">Contiene el nombre y el tipo (basado en dominio o independiente) de un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-157">Estructura de _DFS_STORAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="54b14-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="54b14-158">Contiene información acerca de un destino de vínculo o raíz DFS en un espacio de nombres DFS o desde la memoria caché mantenida por el cliente DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-159">Estructura de _DFS_STORAGE_INFO_1</span><span class="sxs-lookup"><span data-stu-id="54b14-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="54b14-160">Contiene información sobre un destino DFS, incluido el nombre del servidor de destino DFS y el nombre del recurso compartido, así como el estado y la prioridad del destino.</span><span class="sxs-lookup"><span data-stu-id="54b14-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-161">Estructura de _DFS_SUPPORTED_NAMESPACE_VERSION_INFO</span><span class="sxs-lookup"><span data-stu-id="54b14-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="54b14-162">Contiene información de versión de un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="54b14-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="54b14-163">Estructura de _DFS_TARGET_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="54b14-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="54b14-164">Contiene la clase de prioridad y el rango de un destino DFS específico.</span><span class="sxs-lookup"><span data-stu-id="54b14-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
