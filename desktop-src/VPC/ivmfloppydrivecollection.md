---
title: Interfaz IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Define una colección de unidades de disquete en la máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Interfaz IVMFloppyDriveCollection Virtual PC
- Interfaz IVMFloppyDriveCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422603"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="3153b-105">Interfaz IVMFloppyDriveCollection</span><span class="sxs-lookup"><span data-stu-id="3153b-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="3153b-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3153b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3153b-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3153b-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3153b-108">Define una colección de unidades de disquete en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3153b-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="3153b-109">Para obtener un objeto **IVMFloppyDriveCollection** , use la propiedad [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="3153b-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="3153b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3153b-110">Members</span></span>

<span data-ttu-id="3153b-111">La interfaz **IVMFloppyDriveCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3153b-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3153b-112">**IVMFloppyDriveCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3153b-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="3153b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3153b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3153b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3153b-114">Properties</span></span>

<span data-ttu-id="3153b-115">La interfaz **IVMFloppyDriveCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3153b-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="3153b-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3153b-116">Property</span></span>                                                          | <span data-ttu-id="3153b-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="3153b-117">Access type</span></span>          | <span data-ttu-id="3153b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3153b-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="3153b-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3153b-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="3153b-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3153b-120">Read-only</span></span><br/> | <span data-ttu-id="3153b-121">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="3153b-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="3153b-122">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="3153b-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="3153b-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3153b-123">Read-only</span></span><br/> | <span data-ttu-id="3153b-124">El número de unidades de disquete de esta colección.</span><span class="sxs-lookup"><span data-stu-id="3153b-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="3153b-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3153b-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="3153b-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3153b-126">Read-only</span></span><br/> | <span data-ttu-id="3153b-127">Objeto de unidad de disquete que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3153b-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3153b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3153b-128">Requirements</span></span>



| <span data-ttu-id="3153b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3153b-129">Requirement</span></span> | <span data-ttu-id="3153b-130">Value</span><span class="sxs-lookup"><span data-stu-id="3153b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3153b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3153b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3153b-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3153b-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3153b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3153b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3153b-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3153b-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3153b-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3153b-135">End of client support</span></span><br/>    | <span data-ttu-id="3153b-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3153b-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3153b-137">Producto</span><span class="sxs-lookup"><span data-stu-id="3153b-137">Product</span></span><br/>                  | <span data-ttu-id="3153b-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3153b-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3153b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3153b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3153b-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3153b-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3153b-141">IID</span><span class="sxs-lookup"><span data-stu-id="3153b-141">IID</span></span><br/>                      | <span data-ttu-id="3153b-142">IID \_ IVMFloppyDriveCollection se define como 8ba70a25-F698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="3153b-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="3153b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3153b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3153b-144">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="3153b-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="3153b-145">**IVMVirtualMachine::FloppyDrives**</span><span class="sxs-lookup"><span data-stu-id="3153b-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

