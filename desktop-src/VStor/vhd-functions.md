---
description: 'Más información acerca de: <span id=vhd.vhd_functions></span> funciones de disco virtual'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funciones de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696419"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="9de71-103"><span id="vhd.vhd_functions"></span>Funciones de disco virtual</span><span class="sxs-lookup"><span data-stu-id="9de71-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="9de71-104">Las siguientes funciones se usan en discos virtuales:</span><span class="sxs-lookup"><span data-stu-id="9de71-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="9de71-105"><span id="in_this_section"></span>En esta sección</span><span class="sxs-lookup"><span data-stu-id="9de71-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9de71-106">Tema</span><span class="sxs-lookup"><span data-stu-id="9de71-106">Topic</span></span></th>
<th><span data-ttu-id="9de71-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9de71-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9de71-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-109">Aplica una instantánea del disco virtual actual para los archivos de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="9de71-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-111">Conecta un elemento primario a un disco virtual abierto con la marca de <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="9de71-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-113">Conecta un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO) buscando un proveedor de VHD adecuado para realizar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9de71-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-115">Interrumpe una operación de reflejo iniciada previamente y establece el reflejo como el disco virtual activo.</span><span class="sxs-lookup"><span data-stu-id="9de71-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-117">Reduce el tamaño de un archivo de almacenamiento de copia de seguridad de disco duro virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="9de71-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-119">Crea un archivo de imagen de disco duro virtual (VHD), ya sea mediante parámetros predeterminados o mediante un disco virtual o un disco físico existente.</span><span class="sxs-lookup"><span data-stu-id="9de71-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-121">Elimina una instantánea de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="9de71-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-123">Elimina los metadatos de un disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-125">Desasocia un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO) localizando un proveedor de discos virtuales adecuado para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="9de71-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-127">Enumera los metadatos asociados a un disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-129">Aumenta el tamaño de un disco duro virtual (VHD) fijo o expansible dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="9de71-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-131">Devuelve las relaciones entre discos duros virtuales (VHD) o un archivo de imagen de CD o DVD (ISO) o los volúmenes contenidos en esos discos y su disco o volumen primarios.</span><span class="sxs-lookup"><span data-stu-id="9de71-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-133">Recupera información sobre un VHD.</span><span class="sxs-lookup"><span data-stu-id="9de71-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-135">Recupera los metadatos especificados del disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-137">Comprueba el progreso de una operación asincrónica del disco duro virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="9de71-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-139">Recupera la ruta de acceso al objeto de dispositivo físico que contiene un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO).</span><span class="sxs-lookup"><span data-stu-id="9de71-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-141">Combina un disco duro virtual (VHD) secundario en una cadena de diferenciación con uno o más discos virtuales primarios de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9de71-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-143">Inicia una operación de reflejo para un disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-145">Modifica el contenido interno de un archivo de disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="9de71-146">Se puede usar para establecer la hoja activa o para corregir las entradas de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="9de71-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-148">Abre un disco duro virtual (VHD) o un CD o un archivo de imagen de DVD (ISO) para su uso.</span><span class="sxs-lookup"><span data-stu-id="9de71-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-150">Recupera información sobre los cambios en las áreas especificadas de un disco duro virtual (VHD) cuyo seguimiento realiza el seguimiento de cambios resistentes (RCT).</span><span class="sxs-lookup"><span data-stu-id="9de71-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-152">Emite una solicitud SCSI insertada directamente en un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-154">Cambia el tamaño de un disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-156">Establece información sobre un disco duro virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="9de71-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9de71-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-158">Establece un elemento de metadatos para un disco virtual.</span><span class="sxs-lookup"><span data-stu-id="9de71-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9de71-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="9de71-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="9de71-160">Crea una instantánea del disco virtual actual para los archivos de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="9de71-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
