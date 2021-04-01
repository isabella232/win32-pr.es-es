---
title: Interfaz IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Define la colección de máquinas virtuales dentro de Windows Virtual PC. Para obtener un objeto IVMVirtualMachineCollection, use la propiedad VirtualMachines de IVMVirtualPC.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Interfaz IVMVirtualMachineCollection Virtual PC
- Interfaz IVMVirtualMachineCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150941"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="4bb32-106">Interfaz IVMVirtualMachineCollection</span><span class="sxs-lookup"><span data-stu-id="4bb32-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="4bb32-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4bb32-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4bb32-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4bb32-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4bb32-109">Define la colección de máquinas virtuales dentro de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="4bb32-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="4bb32-110">Para obtener un objeto **IVMVirtualMachineCollection** , use la propiedad [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb32-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="4bb32-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4bb32-111">Members</span></span>

<span data-ttu-id="4bb32-112">La interfaz **IVMVirtualMachineCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4bb32-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4bb32-113">**IVMVirtualMachineCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4bb32-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="4bb32-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bb32-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bb32-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bb32-115">Properties</span></span>

<span data-ttu-id="4bb32-116">La interfaz **IVMVirtualMachineCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4bb32-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="4bb32-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bb32-117">Property</span></span>                                                             | <span data-ttu-id="4bb32-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4bb32-118">Access type</span></span>          | <span data-ttu-id="4bb32-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bb32-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="4bb32-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4bb32-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="4bb32-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bb32-121">Read-only</span></span><br/> | <span data-ttu-id="4bb32-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="4bb32-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="4bb32-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="4bb32-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="4bb32-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bb32-124">Read-only</span></span><br/> | <span data-ttu-id="4bb32-125">El número de máquinas virtuales de esta colección.</span><span class="sxs-lookup"><span data-stu-id="4bb32-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="4bb32-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4bb32-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="4bb32-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bb32-127">Read-only</span></span><br/> | <span data-ttu-id="4bb32-128">Objeto de máquina virtual que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4bb32-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4bb32-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bb32-129">Requirements</span></span>



| <span data-ttu-id="4bb32-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb32-130">Requirement</span></span> | <span data-ttu-id="4bb32-131">Value</span><span class="sxs-lookup"><span data-stu-id="4bb32-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb32-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb32-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb32-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bb32-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4bb32-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb32-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb32-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4bb32-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4bb32-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4bb32-136">End of client support</span></span><br/>    | <span data-ttu-id="4bb32-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bb32-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="4bb32-138">Producto</span><span class="sxs-lookup"><span data-stu-id="4bb32-138">Product</span></span><br/>                  | <span data-ttu-id="4bb32-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4bb32-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="4bb32-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bb32-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bb32-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb32-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="4bb32-142">IID</span><span class="sxs-lookup"><span data-stu-id="4bb32-142">IID</span></span><br/>                      | <span data-ttu-id="4bb32-143">IID \_ IVMVirtualMachineCollection se define como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="4bb32-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bb32-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bb32-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb32-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4bb32-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="4bb32-146">**IVMVirtualPC:: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="4bb32-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

