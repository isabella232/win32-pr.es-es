---
title: Interfaz IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Define la colección de unidades de CD y DVD de la máquina virtual. Para obtener un objeto IVMDVDDriveCollection, use la propiedad DVDROMDrives de IVMVirtualMachine.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Interfaz IVMDVDDriveCollection Virtual PC
- Interfaz IVMDVDDriveCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651404"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="96f1a-106">Interfaz IVMDVDDriveCollection</span><span class="sxs-lookup"><span data-stu-id="96f1a-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="96f1a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96f1a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96f1a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96f1a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96f1a-109">Define la colección de unidades de CD y DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="96f1a-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="96f1a-110">Para obtener un objeto **IVMDVDDriveCollection** , use la propiedad [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="96f1a-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="96f1a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="96f1a-111">Members</span></span>

<span data-ttu-id="96f1a-112">La interfaz **IVMDVDDriveCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="96f1a-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="96f1a-113">**IVMDVDDriveCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96f1a-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="96f1a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96f1a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96f1a-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96f1a-115">Properties</span></span>

<span data-ttu-id="96f1a-116">La interfaz **IVMDVDDriveCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96f1a-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="96f1a-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96f1a-117">Property</span></span>                                                       | <span data-ttu-id="96f1a-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="96f1a-118">Access type</span></span>          | <span data-ttu-id="96f1a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="96f1a-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="96f1a-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="96f1a-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="96f1a-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96f1a-121">Read-only</span></span><br/> | <span data-ttu-id="96f1a-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="96f1a-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="96f1a-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="96f1a-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="96f1a-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96f1a-124">Read-only</span></span><br/> | <span data-ttu-id="96f1a-125">El número de unidades de CD y DVD de esta colección.</span><span class="sxs-lookup"><span data-stu-id="96f1a-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="96f1a-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96f1a-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="96f1a-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96f1a-127">Read-only</span></span><br/> | <span data-ttu-id="96f1a-128">Objeto de unidad de CD o DVD que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="96f1a-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96f1a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96f1a-129">Requirements</span></span>



| <span data-ttu-id="96f1a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f1a-130">Requirement</span></span> | <span data-ttu-id="96f1a-131">Value</span><span class="sxs-lookup"><span data-stu-id="96f1a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f1a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96f1a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="96f1a-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="96f1a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96f1a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96f1a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="96f1a-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="96f1a-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96f1a-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="96f1a-136">End of client support</span></span><br/>    | <span data-ttu-id="96f1a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96f1a-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96f1a-138">Producto</span><span class="sxs-lookup"><span data-stu-id="96f1a-138">Product</span></span><br/>                  | <span data-ttu-id="96f1a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96f1a-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96f1a-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96f1a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f1a-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f1a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96f1a-142">IID</span><span class="sxs-lookup"><span data-stu-id="96f1a-142">IID</span></span><br/>                      | <span data-ttu-id="96f1a-143">IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="96f1a-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="96f1a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="96f1a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f1a-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="96f1a-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="96f1a-146">**IVMVirtualMachine::D VDROMDrives**</span><span class="sxs-lookup"><span data-stu-id="96f1a-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

