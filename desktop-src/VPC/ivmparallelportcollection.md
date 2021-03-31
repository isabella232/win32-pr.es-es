---
title: Interfaz IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Define la colección de puertos paralelos dentro de la máquina virtual. Para obtener un objeto IVMParallelPortCollection, use la propiedad ParallelPorts de IVMVirtualMachine.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Interfaz IVMParallelPortCollection Virtual PC
- Interfaz IVMParallelPortCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151076"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="b28b6-106">Interfaz IVMParallelPortCollection</span><span class="sxs-lookup"><span data-stu-id="b28b6-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="b28b6-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b28b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b28b6-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b28b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b28b6-109">Define la colección de puertos paralelos dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b28b6-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="b28b6-110">Para obtener un objeto **IVMParallelPortCollection** , use la propiedad [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="b28b6-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="b28b6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b28b6-111">Members</span></span>

<span data-ttu-id="b28b6-112">La interfaz **IVMParallelPortCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b28b6-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b28b6-113">**IVMParallelPortCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b28b6-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b28b6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b28b6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b28b6-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b28b6-115">Properties</span></span>

<span data-ttu-id="b28b6-116">La interfaz **IVMParallelPortCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b28b6-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="b28b6-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b28b6-117">Property</span></span>                                                           | <span data-ttu-id="b28b6-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b28b6-118">Access type</span></span>          | <span data-ttu-id="b28b6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b28b6-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="b28b6-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b28b6-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="b28b6-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b28b6-121">Read-only</span></span><br/> | <span data-ttu-id="b28b6-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="b28b6-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="b28b6-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="b28b6-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="b28b6-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b28b6-124">Read-only</span></span><br/> | <span data-ttu-id="b28b6-125">Número de puertos paralelos de esta colección.</span><span class="sxs-lookup"><span data-stu-id="b28b6-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="b28b6-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b28b6-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="b28b6-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b28b6-127">Read-only</span></span><br/> | <span data-ttu-id="b28b6-128">Objeto de puerto paralelo que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b28b6-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b28b6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b28b6-129">Requirements</span></span>



| <span data-ttu-id="b28b6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28b6-130">Requirement</span></span> | <span data-ttu-id="b28b6-131">Value</span><span class="sxs-lookup"><span data-stu-id="b28b6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b28b6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b28b6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b28b6-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b28b6-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b28b6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b28b6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b28b6-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b28b6-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b28b6-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b28b6-136">End of client support</span></span><br/>    | <span data-ttu-id="b28b6-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b28b6-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b28b6-138">Producto</span><span class="sxs-lookup"><span data-stu-id="b28b6-138">Product</span></span><br/>                  | <span data-ttu-id="b28b6-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b28b6-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b28b6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b28b6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b28b6-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b28b6-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b28b6-142">IID</span><span class="sxs-lookup"><span data-stu-id="b28b6-142">IID</span></span><br/>                      | <span data-ttu-id="b28b6-143">IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="b28b6-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b28b6-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b28b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28b6-145">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="b28b6-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="b28b6-146">**IVMVirtualMachine::P arallelPorts**</span><span class="sxs-lookup"><span data-stu-id="b28b6-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

