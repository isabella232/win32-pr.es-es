---
title: Interfaz IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Define la colección de dispositivos USB conectados al sistema host. Para obtener un objeto IVMUSBDeviceCollection, use la propiedad USBDeviceCollection de IVMVirtualPC.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Interfaz IVMUSBDeviceCollection Virtual PC
- Interfaz IVMUSBDeviceCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695930"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="1bec0-106">Interfaz IVMUSBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="1bec0-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="1bec0-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1bec0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1bec0-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1bec0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1bec0-109">Define la colección de dispositivos USB conectados al sistema host.</span><span class="sxs-lookup"><span data-stu-id="1bec0-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="1bec0-110">Para obtener un objeto **IVMUSBDeviceCollection** , use la propiedad [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1bec0-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="1bec0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1bec0-111">Members</span></span>

<span data-ttu-id="1bec0-112">La interfaz **IVMUSBDeviceCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1bec0-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1bec0-113">**IVMUSBDeviceCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1bec0-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="1bec0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bec0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bec0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bec0-115">Properties</span></span>

<span data-ttu-id="1bec0-116">La interfaz **IVMUSBDeviceCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1bec0-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="1bec0-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1bec0-117">Property</span></span>                                                        | <span data-ttu-id="1bec0-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1bec0-118">Access type</span></span>          | <span data-ttu-id="1bec0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bec0-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bec0-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1bec0-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="1bec0-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bec0-121">Read-only</span></span><br/> | <span data-ttu-id="1bec0-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="1bec0-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="1bec0-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="1bec0-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="1bec0-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bec0-124">Read-only</span></span><br/> | <span data-ttu-id="1bec0-125">El número de dispositivos USB en esta recopilación.</span><span class="sxs-lookup"><span data-stu-id="1bec0-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="1bec0-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1bec0-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="1bec0-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bec0-127">Read-only</span></span><br/> | <span data-ttu-id="1bec0-128">Objeto de dispositivo USB que corresponde al índice especificado (basado en 1).</span><span class="sxs-lookup"><span data-stu-id="1bec0-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bec0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bec0-129">Requirements</span></span>



| <span data-ttu-id="1bec0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bec0-130">Requirement</span></span> | <span data-ttu-id="1bec0-131">Value</span><span class="sxs-lookup"><span data-stu-id="1bec0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bec0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bec0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1bec0-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1bec0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bec0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bec0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1bec0-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1bec0-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1bec0-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1bec0-136">End of client support</span></span><br/>    | <span data-ttu-id="1bec0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1bec0-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1bec0-138">Producto</span><span class="sxs-lookup"><span data-stu-id="1bec0-138">Product</span></span><br/>                  | <span data-ttu-id="1bec0-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1bec0-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1bec0-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bec0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bec0-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bec0-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1bec0-142">IID</span><span class="sxs-lookup"><span data-stu-id="1bec0-142">IID</span></span><br/>                      | <span data-ttu-id="1bec0-143">IID \_ IVMUSBDeviceCollection se define como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="1bec0-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="1bec0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bec0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bec0-145">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="1bec0-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="1bec0-146">**IVMVirtualPC::USBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="1bec0-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

