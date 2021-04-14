---
title: Funciones de Sistema de archivos distribuido
description: A continuación se muestran las funciones de Sistema de archivos distribuido (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496577"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="66e3c-103">Funciones de Sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="66e3c-103">Distributed File System Functions</span></span>

<span data-ttu-id="66e3c-104">A continuación se muestran las funciones de Sistema de archivos distribuido (DFS).</span><span class="sxs-lookup"><span data-stu-id="66e3c-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66e3c-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="66e3c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="66e3c-106">NetDfsAdd</span><span class="sxs-lookup"><span data-stu-id="66e3c-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="66e3c-107">Crea un nuevo vínculo de Sistema de archivos distribuido (DFS) o agrega destinos a un vínculo existente en un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-108">NetDfsAddFtRoot</span><span class="sxs-lookup"><span data-stu-id="66e3c-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="66e3c-109">Crea un nuevo espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="66e3c-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="66e3c-110">Si el espacio de nombres ya existe, la función le agrega el destino raíz especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-111">NetDfsAddRootTarget</span><span class="sxs-lookup"><span data-stu-id="66e3c-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="66e3c-112">Crea un espacio de nombres DFS independiente o basado en dominio o agrega un nuevo destino raíz a un espacio de nombres basado en dominio existente.</span><span class="sxs-lookup"><span data-stu-id="66e3c-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-113">NetDfsAddStdRoot</span><span class="sxs-lookup"><span data-stu-id="66e3c-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="66e3c-114">Crea un nuevo espacio de nombres de Sistema de archivos distribuido independiente (DFS).</span><span class="sxs-lookup"><span data-stu-id="66e3c-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-115">NetDfsEnum</span><span class="sxs-lookup"><span data-stu-id="66e3c-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="66e3c-116">Enumera los espacios de nombres de Sistema de archivos distribuido (DFS) hospedados en un servidor o vínculos DFS de un espacio de nombres hospedado por un servidor.</span><span class="sxs-lookup"><span data-stu-id="66e3c-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-117">NetDfsGetClientInfo</span><span class="sxs-lookup"><span data-stu-id="66e3c-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="66e3c-118">Recupera información acerca de una raíz o un vínculo de Sistema de archivos distribuido (DFS) de la memoria caché mantenida por el cliente DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-119">NetDfsGetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="66e3c-120">Recupera el descriptor de seguridad del objeto contenedor de los espacios de nombres DFS basados en dominio en el dominio de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-121">NetDfsGetInfo</span><span class="sxs-lookup"><span data-stu-id="66e3c-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="66e3c-122">Recupera información sobre una raíz o un vínculo de Sistema de archivos distribuido (DFS) especificado en un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-123">NetDfsGetSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="66e3c-124">Recupera el descriptor de seguridad para el objeto raíz del espacio de nombres DFS especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-125">NetDfsGetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="66e3c-126">Recupera el descriptor de seguridad para el objeto contenedor del espacio de nombres DFS independiente especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-127">NetDfsGetSupportedNamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="66e3c-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="66e3c-128">Determina el número de versión de metadatos admitido.</span><span class="sxs-lookup"><span data-stu-id="66e3c-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-129">NetDfsMove</span><span class="sxs-lookup"><span data-stu-id="66e3c-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="66e3c-130">Cambia el nombre de un vínculo DFS o lo mueve.</span><span class="sxs-lookup"><span data-stu-id="66e3c-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-131">NetDfsRemove</span><span class="sxs-lookup"><span data-stu-id="66e3c-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="66e3c-132">Quita un vínculo de Sistema de archivos distribuido (DFS) o un destino de vínculo específico de un vínculo DFS en un espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="66e3c-133">Al quitar un destino de vínculo específico, se quita el vínculo en sí si se quita el último destino de vínculo del vínculo.</span><span class="sxs-lookup"><span data-stu-id="66e3c-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-134">NetDfsRemoveFtRoot</span><span class="sxs-lookup"><span data-stu-id="66e3c-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="66e3c-135">Quita el destino de raíz especificado de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="66e3c-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="66e3c-136">Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="66e3c-137">Se puede eliminar un espacio de nombres DFS sin eliminar primero todos los vínculos que contiene.</span><span class="sxs-lookup"><span data-stu-id="66e3c-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-138">NetDfsRemoveFtRootForced</span><span class="sxs-lookup"><span data-stu-id="66e3c-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="66e3c-139">Quita el destino de raíz especificado de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS), incluso si el servidor de destino raíz está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="66e3c-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="66e3c-140">Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="66e3c-141">Se puede eliminar un espacio de nombres DFS sin eliminar primero todos los vínculos que contiene.</span><span class="sxs-lookup"><span data-stu-id="66e3c-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="66e3c-142">La función [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) no actualiza el registro en el servidor de destino raíz DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="66e3c-143">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="66e3c-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-144">NetDfsRemoveRootTarget</span><span class="sxs-lookup"><span data-stu-id="66e3c-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="66e3c-145">Quita un destino de raíz DFS de un espacio de nombres DFS basado en dominio.</span><span class="sxs-lookup"><span data-stu-id="66e3c-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="66e3c-146">Si el destino raíz es el último destino raíz en el espacio de nombres DFS, esta función quita el espacio de nombres DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="66e3c-147">Esta función también se puede usar para quitar un espacio de nombres DFS independiente.</span><span class="sxs-lookup"><span data-stu-id="66e3c-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-148">NetDfsRemoveStdRoot</span><span class="sxs-lookup"><span data-stu-id="66e3c-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="66e3c-149">Elimina un espacio de nombres de Sistema de archivos distribuido independiente (DFS).</span><span class="sxs-lookup"><span data-stu-id="66e3c-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-150">NetDfsSetClientInfo</span><span class="sxs-lookup"><span data-stu-id="66e3c-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="66e3c-151">Modifica información acerca de una raíz o un vínculo de Sistema de archivos distribuido (DFS) en la caché mantenido por el cliente DFS.</span><span class="sxs-lookup"><span data-stu-id="66e3c-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-152">NetDfsSetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="66e3c-153">Establece el descriptor de seguridad del objeto contenedor de los espacios de nombres DFS basados en dominio en el dominio de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-154">NetDfsSetInfo</span><span class="sxs-lookup"><span data-stu-id="66e3c-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="66e3c-155">Establece o modifica la información sobre una raíz específica del Sistema de archivos distribuido (DFS), el destino de la raíz, el vínculo o el destino del vínculo.</span><span class="sxs-lookup"><span data-stu-id="66e3c-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-156">NetDfsSetSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="66e3c-157">Establece el descriptor de seguridad para el objeto raíz del espacio de nombres DFS especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="66e3c-158">NetDfsSetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="66e3c-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="66e3c-159">Establece el descriptor de seguridad para el objeto contenedor del espacio de nombres DFS independiente especificado.</span><span class="sxs-lookup"><span data-stu-id="66e3c-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="66e3c-160">Tenga en cuenta que una aplicación que invoca cualquiera de las funciones puede hacer que el servidor de espacio de nombres DFS local que atiende a la llamada de función realice una sincronización completa de los metadatos de espacio de nombres relacionados desde el maestro de emulador de PDC para ese dominio.</span><span class="sxs-lookup"><span data-stu-id="66e3c-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="66e3c-161">Esta sincronización completa puede producirse incluso cuando se configura el modo de escalabilidad de raíz para ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="66e3c-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
