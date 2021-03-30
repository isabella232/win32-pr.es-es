---
title: Interfaz IVMDVDDrive (VPCCOMInterfaces. h)
description: Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual. IVMDVDDrive puede notificar a los clientes sobre eventos mediante la interfaz de salida de IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Interfaz IVMDVDDrive Virtual PC
- Interfaz IVMDVDDrive Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079508"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="bf134-106">Interfaz IVMDVDDrive</span><span class="sxs-lookup"><span data-stu-id="bf134-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="bf134-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf134-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf134-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bf134-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf134-109">Controla una unidad de CD-ROM o DVD-ROM dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf134-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="bf134-110">**IVMDVDDrive** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="bf134-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="bf134-111">Puede Agregar una nueva unidad de CD-ROM o DVD-ROM a una máquina virtual mediante el método [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="bf134-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="bf134-112">Puede quitar una unidad de CD-ROM o DVD-ROM existente de una máquina virtual mediante el método [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="bf134-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="bf134-113">Puede recuperar un objeto **IVMDVDDrive** del objeto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) devuelto desde la propiedad [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="bf134-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="bf134-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf134-114">Members</span></span>

<span data-ttu-id="bf134-115">La interfaz **IVMDVDDrive** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bf134-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bf134-116">**IVMDVDDrive** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf134-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="bf134-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf134-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf134-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf134-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf134-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf134-119">Methods</span></span>

<span data-ttu-id="bf134-120">La interfaz **IVMDVDDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bf134-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="bf134-121">Método</span><span class="sxs-lookup"><span data-stu-id="bf134-121">Method</span></span>                                                   | <span data-ttu-id="bf134-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf134-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf134-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="bf134-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="bf134-124">Conecta una unidad host a la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf134-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="bf134-125">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="bf134-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="bf134-126">Adjunta una imagen ISO a la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf134-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="bf134-127">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="bf134-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="bf134-128">Libera una unidad de host capturada de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="bf134-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="bf134-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="bf134-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="bf134-130">Libera una imagen ISO capturada de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="bf134-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="bf134-131">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="bf134-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="bf134-132">Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf134-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bf134-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf134-133">Properties</span></span>

<span data-ttu-id="bf134-134">La interfaz **IVMDVDDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf134-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="bf134-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf134-135">Property</span></span>                                                          | <span data-ttu-id="bf134-136">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bf134-136">Access type</span></span>          | <span data-ttu-id="bf134-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf134-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="bf134-138">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="bf134-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="bf134-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf134-139">Read-only</span></span><br/> | <span data-ttu-id="bf134-140">El tipo de medio conectado a la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf134-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="bf134-141">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="bf134-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="bf134-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf134-142">Read-only</span></span><br/> | <span data-ttu-id="bf134-143">Número de bus al que está conectado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf134-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="bf134-144">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="bf134-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="bf134-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf134-145">Read-only</span></span><br/> | <span data-ttu-id="bf134-146">El número de dispositivo al que está conectada esta unidad.</span><span class="sxs-lookup"><span data-stu-id="bf134-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="bf134-147">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="bf134-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="bf134-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf134-148">Read-only</span></span><br/> | <span data-ttu-id="bf134-149">La letra de la unidad de host establecida para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf134-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="bf134-150">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="bf134-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="bf134-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf134-151">Read-only</span></span><br/> | <span data-ttu-id="bf134-152">Ruta de acceso completa del archivo de imagen establecido para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf134-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="bf134-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf134-153">Requirements</span></span>



| <span data-ttu-id="bf134-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf134-154">Requirement</span></span> | <span data-ttu-id="bf134-155">Value</span><span class="sxs-lookup"><span data-stu-id="bf134-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf134-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf134-156">Minimum supported client</span></span><br/> | <span data-ttu-id="bf134-157">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf134-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf134-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf134-158">Minimum supported server</span></span><br/> | <span data-ttu-id="bf134-159">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bf134-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf134-160">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bf134-160">End of client support</span></span><br/>    | <span data-ttu-id="bf134-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf134-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf134-162">Producto</span><span class="sxs-lookup"><span data-stu-id="bf134-162">Product</span></span><br/>                  | <span data-ttu-id="bf134-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf134-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf134-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf134-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf134-165"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf134-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf134-166">IID</span><span class="sxs-lookup"><span data-stu-id="bf134-166">IID</span></span><br/>                      | <span data-ttu-id="bf134-167">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="bf134-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

