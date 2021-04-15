---
title: Interfaz IVMUSBDevice (VPCCOMInterfaces. h)
description: Define la interfaz para un dispositivo USB conectado al host. Puede conectar el dispositivo USB a una máquina virtual para usar el dispositivo dentro de la máquina virtual.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Interfaz IVMUSBDevice Virtual PC
- Interfaz IVMUSBDevice Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695950"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="a2fe7-106">Interfaz IVMUSBDevice</span><span class="sxs-lookup"><span data-stu-id="a2fe7-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="a2fe7-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2fe7-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2fe7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2fe7-109">Define la interfaz para un dispositivo USB conectado al host.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="a2fe7-110">Puede conectar el dispositivo USB a una máquina virtual para usar el dispositivo dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="a2fe7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2fe7-111">Members</span></span>

<span data-ttu-id="a2fe7-112">La interfaz **IVMUSBDevice** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a2fe7-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a2fe7-113">**IVMUSBDevice** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a2fe7-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="a2fe7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2fe7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2fe7-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2fe7-115">Properties</span></span>

<span data-ttu-id="a2fe7-116">La interfaz **IVMUSBDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="a2fe7-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2fe7-117">Property</span></span>                                                                 | <span data-ttu-id="a2fe7-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a2fe7-118">Access type</span></span>          | <span data-ttu-id="a2fe7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2fe7-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="a2fe7-120">**AttachedToVM**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="a2fe7-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-121">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-122">El nombre de la máquina virtual a la que está conectado el dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="a2fe7-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="a2fe7-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-124">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-125">La clase de dispositivo del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="a2fe7-126">**DeviceString**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="a2fe7-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-127">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-128">Nombre del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="a2fe7-129">**HubID**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="a2fe7-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-130">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-131">Identificador del concentrador en el que está conectado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="a2fe7-132">**ManufacturerString**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="a2fe7-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-133">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-134">Nombre del fabricante del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="a2fe7-135">**Port**</span><span class="sxs-lookup"><span data-stu-id="a2fe7-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="a2fe7-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2fe7-136">Read-only</span></span><br/> | <span data-ttu-id="a2fe7-137">El identificador del puerto en el que está conectado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2fe7-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="a2fe7-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2fe7-138">Requirements</span></span>



| <span data-ttu-id="a2fe7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2fe7-139">Requirement</span></span> | <span data-ttu-id="a2fe7-140">Value</span><span class="sxs-lookup"><span data-stu-id="a2fe7-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fe7-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2fe7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fe7-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2fe7-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2fe7-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2fe7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fe7-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a2fe7-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2fe7-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a2fe7-145">End of client support</span></span><br/>    | <span data-ttu-id="a2fe7-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2fe7-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2fe7-147">Producto</span><span class="sxs-lookup"><span data-stu-id="a2fe7-147">Product</span></span><br/>                  | <span data-ttu-id="a2fe7-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2fe7-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2fe7-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2fe7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fe7-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fe7-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2fe7-151">IID</span><span class="sxs-lookup"><span data-stu-id="a2fe7-151">IID</span></span><br/>                      | <span data-ttu-id="a2fe7-152">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="a2fe7-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

