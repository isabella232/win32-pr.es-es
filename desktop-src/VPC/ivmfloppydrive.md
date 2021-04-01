---
title: Interfaz IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controla una unidad de disquete dentro de una máquina virtual.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Interfaz IVMFloppyDrive Virtual PC
- Interfaz IVMFloppyDrive Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996945"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="04632-105">Interfaz IVMFloppyDrive</span><span class="sxs-lookup"><span data-stu-id="04632-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="04632-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04632-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04632-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04632-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04632-108">Controla una unidad de disquete dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04632-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="04632-109">**IVMFloppyDrive** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="04632-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="04632-110">Puede recuperar un objeto **IVMFloppyDrive** del objeto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="04632-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="04632-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="04632-111">Members</span></span>

<span data-ttu-id="04632-112">La interfaz **IVMFloppyDrive** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="04632-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="04632-113">**IVMFloppyDrive** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="04632-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="04632-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="04632-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="04632-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04632-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04632-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="04632-116">Methods</span></span>

<span data-ttu-id="04632-117">La interfaz **IVMFloppyDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="04632-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="04632-118">Método</span><span class="sxs-lookup"><span data-stu-id="04632-118">Method</span></span>                                                      | <span data-ttu-id="04632-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="04632-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04632-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="04632-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="04632-121">Conecta una unidad física del host a la unidad de disquete en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04632-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="04632-122">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="04632-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="04632-123">Adjunta una imagen de disquete en el host a la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="04632-124">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="04632-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="04632-125">Libera una unidad física del host de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="04632-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="04632-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="04632-127">Libera una imagen de disquete en el host de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="04632-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04632-128">Properties</span></span>

<span data-ttu-id="04632-129">La interfaz **IVMFloppyDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="04632-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="04632-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04632-130">Property</span></span>                                                             | <span data-ttu-id="04632-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="04632-131">Access type</span></span>          | <span data-ttu-id="04632-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="04632-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04632-133">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="04632-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="04632-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="04632-134">Read-only</span></span><br/> | <span data-ttu-id="04632-135">El tipo de medio conectado a la unidad de disquete en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04632-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="04632-136">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="04632-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="04632-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="04632-137">Read-only</span></span><br/> | <span data-ttu-id="04632-138">Índice de base cero del controlador al que está conectada esta unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="04632-139">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="04632-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="04632-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="04632-140">Read-only</span></span><br/> | <span data-ttu-id="04632-141">La letra de la unidad host a la que está conectada la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="04632-142">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="04632-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="04632-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="04632-143">Read-only</span></span><br/> | <span data-ttu-id="04632-144">La ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="04632-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="04632-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04632-145">Requirements</span></span>



| <span data-ttu-id="04632-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="04632-146">Requirement</span></span> | <span data-ttu-id="04632-147">Value</span><span class="sxs-lookup"><span data-stu-id="04632-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04632-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04632-148">Minimum supported client</span></span><br/> | <span data-ttu-id="04632-149">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="04632-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04632-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04632-150">Minimum supported server</span></span><br/> | <span data-ttu-id="04632-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="04632-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04632-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="04632-152">End of client support</span></span><br/>    | <span data-ttu-id="04632-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04632-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04632-154">Producto</span><span class="sxs-lookup"><span data-stu-id="04632-154">Product</span></span><br/>                  | <span data-ttu-id="04632-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04632-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04632-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04632-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="04632-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="04632-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="04632-158">IID</span><span class="sxs-lookup"><span data-stu-id="04632-158">IID</span></span><br/>                      | <span data-ttu-id="04632-159">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="04632-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

