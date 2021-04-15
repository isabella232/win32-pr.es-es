---
title: Interfaz IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Define la conexión para un disco duro dentro de la máquina virtual.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Interfaz IVMHardDiskConnection Virtual PC
- Interfaz IVMHardDiskConnection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695964"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="cb4a4-105">Interfaz IVMHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="cb4a4-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="cb4a4-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb4a4-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb4a4-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb4a4-108">Define la conexión para un disco duro dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="cb4a4-109">El método [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) devuelve un objeto **IVMHardDiskConnection** .</span><span class="sxs-lookup"><span data-stu-id="cb4a4-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="cb4a4-110">También puede recuperar un objeto **IVMHardDiskConnection** del objeto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="cb4a4-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="cb4a4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb4a4-111">Members</span></span>

<span data-ttu-id="cb4a4-112">La interfaz **IVMHardDiskConnection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="cb4a4-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cb4a4-113">**IVMHardDiskConnection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb4a4-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="cb4a4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb4a4-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb4a4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb4a4-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb4a4-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb4a4-116">Methods</span></span>

<span data-ttu-id="cb4a4-117">La interfaz **IVMHardDiskConnection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="cb4a4-118">Método</span><span class="sxs-lookup"><span data-stu-id="cb4a4-118">Method</span></span>                                                         | <span data-ttu-id="cb4a4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb4a4-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="cb4a4-120">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="cb4a4-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="cb4a4-121">Establece la ubicación del bus al que está conectado este disco duro.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb4a4-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb4a4-122">Properties</span></span>

<span data-ttu-id="cb4a4-123">La interfaz **IVMHardDiskConnection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="cb4a4-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb4a4-124">Property</span></span>                                                              | <span data-ttu-id="cb4a4-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="cb4a4-125">Access type</span></span>          | <span data-ttu-id="cb4a4-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb4a4-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="cb4a4-127">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="cb4a4-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="cb4a4-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a4-128">Read-only</span></span><br/> | <span data-ttu-id="cb4a4-129">Número de bus al que está conectada la imagen de la unidad.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="cb4a4-130">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="cb4a4-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="cb4a4-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a4-131">Read-only</span></span><br/> | <span data-ttu-id="cb4a4-132">El número de dispositivo al que está conectada la imagen de la unidad.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="cb4a4-133">**Detectar**</span><span class="sxs-lookup"><span data-stu-id="cb4a4-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="cb4a4-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a4-134">Read-only</span></span><br/> | <span data-ttu-id="cb4a4-135">Un objeto de disco duro correspondiente a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="cb4a4-136">**UndoHardDisk**</span><span class="sxs-lookup"><span data-stu-id="cb4a4-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="cb4a4-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a4-137">Read-only</span></span><br/> | <span data-ttu-id="cb4a4-138">Un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb4a4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb4a4-139">Requirements</span></span>



| <span data-ttu-id="cb4a4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4a4-140">Requirement</span></span> | <span data-ttu-id="cb4a4-141">Value</span><span class="sxs-lookup"><span data-stu-id="cb4a4-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4a4-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb4a4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4a4-143">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb4a4-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb4a4-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb4a4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4a4-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb4a4-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb4a4-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="cb4a4-146">End of client support</span></span><br/>    | <span data-ttu-id="cb4a4-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb4a4-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb4a4-148">Producto</span><span class="sxs-lookup"><span data-stu-id="cb4a4-148">Product</span></span><br/>                  | <span data-ttu-id="cb4a4-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb4a4-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb4a4-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb4a4-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4a4-151"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4a4-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb4a4-152">IID</span><span class="sxs-lookup"><span data-stu-id="cb4a4-152">IID</span></span><br/>                      | <span data-ttu-id="cb4a4-153">IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="cb4a4-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

