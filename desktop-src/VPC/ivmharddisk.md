---
title: Interfaz IVMHardDisk (VPCCOMInterfaces. h)
description: Proporciona acceso a una imagen de disco duro. Se puede tener acceso a ella a través de la propiedad IVMHardDiskConnection disco duro o el método IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Interfaz IVMHardDisk Virtual PC
- Interfaz IVMHardDisk Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488932"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="60023-106">Interfaz IVMHardDisk</span><span class="sxs-lookup"><span data-stu-id="60023-106">IVMHardDisk interface</span></span>

<span data-ttu-id="60023-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="60023-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="60023-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="60023-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="60023-109">Proporciona acceso a una imagen de disco duro.</span><span class="sxs-lookup"><span data-stu-id="60023-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="60023-110">Se puede tener acceso a ella a través de la propiedad [**IVMHardDiskConnection:: disco duro**](ivmharddiskconnection-harddisk.md) o el método [**IVMVirtualPC:: GetHardDisk**](ivmvirtualpc-getharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="60023-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="60023-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="60023-111">Members</span></span>

<span data-ttu-id="60023-112">La interfaz **IVMHardDisk** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="60023-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="60023-113">**IVMHardDisk** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60023-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="60023-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="60023-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="60023-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60023-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60023-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="60023-116">Methods</span></span>

<span data-ttu-id="60023-117">La interfaz **IVMHardDisk** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="60023-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="60023-118">Método</span><span class="sxs-lookup"><span data-stu-id="60023-118">Method</span></span>                                 | <span data-ttu-id="60023-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="60023-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60023-120">**Compacto**</span><span class="sxs-lookup"><span data-stu-id="60023-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="60023-121">Compacta una imagen de disco duro virtual de expansión dinámica.</span><span class="sxs-lookup"><span data-stu-id="60023-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="60023-122">**Convert**</span><span class="sxs-lookup"><span data-stu-id="60023-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="60023-123">Convierte cualquier disco duro virtual en un disco duro virtual de expansión dinámica o en un disco duro virtual de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="60023-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="60023-124">**Sin**</span><span class="sxs-lookup"><span data-stu-id="60023-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="60023-125">Combina un disco duro virtual de diferenciación con su imagen de disco principal.</span><span class="sxs-lookup"><span data-stu-id="60023-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="60023-126">**Fusionar mediante combinación**</span><span class="sxs-lookup"><span data-stu-id="60023-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="60023-127">Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta el disco duro virtual primario raíz incluido) en un nuevo archivo de disco duro.</span><span class="sxs-lookup"><span data-stu-id="60023-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="60023-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60023-128">Properties</span></span>

<span data-ttu-id="60023-129">La interfaz **IVMHardDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60023-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="60023-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60023-130">Property</span></span>                                                              | <span data-ttu-id="60023-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="60023-131">Access type</span></span>           | <span data-ttu-id="60023-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="60023-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60023-133">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="60023-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="60023-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="60023-134">Read-only</span></span><br/>  | <span data-ttu-id="60023-135">El nombre de la ruta de acceso completa del archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="60023-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="60023-136">**HostFreeDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="60023-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="60023-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="60023-137">Read-only</span></span><br/>  | <span data-ttu-id="60023-138">La cantidad de espacio en disco restante disponible en el host para el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="60023-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="60023-139">**Parent**</span><span class="sxs-lookup"><span data-stu-id="60023-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="60023-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="60023-140">Read/write</span></span><br/> | <span data-ttu-id="60023-141">El elemento primario del disco duro virtual de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="60023-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="60023-142">**SizeInGuest**</span><span class="sxs-lookup"><span data-stu-id="60023-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="60023-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="60023-143">Read-only</span></span><br/>  | <span data-ttu-id="60023-144">El tamaño del disco duro virtual en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="60023-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="60023-145">**SizeOnHost**</span><span class="sxs-lookup"><span data-stu-id="60023-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="60023-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="60023-146">Read-only</span></span><br/>  | <span data-ttu-id="60023-147">El tamaño del archivo de disco duro virtual en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="60023-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="60023-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="60023-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="60023-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="60023-149">Read-only</span></span><br/>  | <span data-ttu-id="60023-150">El tipo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="60023-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="60023-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60023-151">Requirements</span></span>



| <span data-ttu-id="60023-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="60023-152">Requirement</span></span> | <span data-ttu-id="60023-153">Value</span><span class="sxs-lookup"><span data-stu-id="60023-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="60023-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60023-154">Minimum supported client</span></span><br/> | <span data-ttu-id="60023-155">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="60023-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60023-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60023-156">Minimum supported server</span></span><br/> | <span data-ttu-id="60023-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60023-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="60023-158">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="60023-158">End of client support</span></span><br/>    | <span data-ttu-id="60023-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="60023-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="60023-160">Producto</span><span class="sxs-lookup"><span data-stu-id="60023-160">Product</span></span><br/>                  | <span data-ttu-id="60023-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="60023-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="60023-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60023-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="60023-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="60023-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="60023-164">IID</span><span class="sxs-lookup"><span data-stu-id="60023-164">IID</span></span><br/>                      | <span data-ttu-id="60023-165">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="60023-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

