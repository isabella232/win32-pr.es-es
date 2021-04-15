---
title: Interfaz IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Define la colección de conexiones de disco duro dentro de la máquina virtual. Para obtener un objeto IVMHardDiskConnectionCollection, use la propiedad HardDiskConnections de IVMVirtualMachine.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Interfaz IVMHardDiskConnectionCollection Virtual PC
- Interfaz IVMHardDiskConnectionCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488926"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="473df-106">Interfaz IVMHardDiskConnectionCollection</span><span class="sxs-lookup"><span data-stu-id="473df-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="473df-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="473df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="473df-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="473df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="473df-109">Define la colección de conexiones de disco duro dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="473df-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="473df-110">Para obtener un objeto **IVMHardDiskConnectionCollection** , use la propiedad [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="473df-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="473df-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="473df-111">Members</span></span>

<span data-ttu-id="473df-112">La interfaz **IVMHardDiskConnectionCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="473df-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="473df-113">**IVMHardDiskConnectionCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="473df-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="473df-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="473df-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="473df-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="473df-115">Properties</span></span>

<span data-ttu-id="473df-116">La interfaz **IVMHardDiskConnectionCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="473df-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="473df-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="473df-117">Property</span></span>                                                                 | <span data-ttu-id="473df-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="473df-118">Access type</span></span>          | <span data-ttu-id="473df-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="473df-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="473df-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="473df-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="473df-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473df-121">Read-only</span></span><br/> | <span data-ttu-id="473df-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="473df-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="473df-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="473df-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="473df-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473df-124">Read-only</span></span><br/> | <span data-ttu-id="473df-125">El número de conexiones de disco duro en esta colección.</span><span class="sxs-lookup"><span data-stu-id="473df-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="473df-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="473df-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="473df-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473df-127">Read-only</span></span><br/> | <span data-ttu-id="473df-128">Objeto de conexión del disco duro que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="473df-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="473df-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="473df-129">Requirements</span></span>



| <span data-ttu-id="473df-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="473df-130">Requirement</span></span> | <span data-ttu-id="473df-131">Value</span><span class="sxs-lookup"><span data-stu-id="473df-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473df-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="473df-132">Minimum supported client</span></span><br/> | <span data-ttu-id="473df-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="473df-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="473df-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="473df-134">Minimum supported server</span></span><br/> | <span data-ttu-id="473df-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="473df-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="473df-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="473df-136">End of client support</span></span><br/>    | <span data-ttu-id="473df-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="473df-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="473df-138">Producto</span><span class="sxs-lookup"><span data-stu-id="473df-138">Product</span></span><br/>                  | <span data-ttu-id="473df-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="473df-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="473df-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="473df-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="473df-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="473df-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="473df-142">IID</span><span class="sxs-lookup"><span data-stu-id="473df-142">IID</span></span><br/>                      | <span data-ttu-id="473df-143">IID \_ IVMHardDiskconnectionCollection se define como b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="473df-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="473df-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="473df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473df-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="473df-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="473df-146">**IVMVirtualMachine::HardDiskConnections**</span><span class="sxs-lookup"><span data-stu-id="473df-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

