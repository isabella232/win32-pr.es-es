---
title: Interfaz IVMParallelPort (VPCCOMInterfaces. h)
description: Define un puerto paralelo dentro de una máquina virtual.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Interfaz IVMParallelPort Virtual PC
- Interfaz IVMParallelPort Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696040"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="261ad-105">Interfaz IVMParallelPort</span><span class="sxs-lookup"><span data-stu-id="261ad-105">IVMParallelPort interface</span></span>

<span data-ttu-id="261ad-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="261ad-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="261ad-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="261ad-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="261ad-108">Define un puerto paralelo dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="261ad-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="261ad-109">Esta interfaz permite configurar puertos paralelos dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="261ad-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="261ad-110">Puede recuperar un objeto **IVMParallelPort** del objeto [**IVMParallelPortCollection**](ivmparallelportcollection.md) devuelto desde la propiedad [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="261ad-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="261ad-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="261ad-111">Members</span></span>

<span data-ttu-id="261ad-112">La interfaz **IVMParallelPort** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="261ad-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="261ad-113">**IVMParallelPort** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="261ad-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="261ad-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="261ad-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="261ad-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="261ad-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="261ad-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="261ad-116">Methods</span></span>

<span data-ttu-id="261ad-117">La interfaz **IVMParallelPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="261ad-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="261ad-118">Método</span><span class="sxs-lookup"><span data-stu-id="261ad-118">Method</span></span>                              | <span data-ttu-id="261ad-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="261ad-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="261ad-120">**\_id**</span><span class="sxs-lookup"><span data-stu-id="261ad-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="261ad-121">Recupera el identificador interno del puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="261ad-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="261ad-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="261ad-122">Properties</span></span>

<span data-ttu-id="261ad-123">La interfaz **IVMParallelPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="261ad-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="261ad-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="261ad-124">Property</span></span>                                        | <span data-ttu-id="261ad-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="261ad-125">Access type</span></span>           | <span data-ttu-id="261ad-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="261ad-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="261ad-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="261ad-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="261ad-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="261ad-128">Read/write</span></span><br/> | <span data-ttu-id="261ad-129">Nombre del puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="261ad-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="261ad-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="261ad-130">Requirements</span></span>



| <span data-ttu-id="261ad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="261ad-131">Requirement</span></span> | <span data-ttu-id="261ad-132">Value</span><span class="sxs-lookup"><span data-stu-id="261ad-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="261ad-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="261ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="261ad-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="261ad-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="261ad-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="261ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="261ad-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="261ad-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="261ad-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="261ad-137">End of client support</span></span><br/>    | <span data-ttu-id="261ad-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="261ad-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="261ad-139">Producto</span><span class="sxs-lookup"><span data-stu-id="261ad-139">Product</span></span><br/>                  | <span data-ttu-id="261ad-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="261ad-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="261ad-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="261ad-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="261ad-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="261ad-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="261ad-143">IID</span><span class="sxs-lookup"><span data-stu-id="261ad-143">IID</span></span><br/>                      | <span data-ttu-id="261ad-144">IID \_ IVMParallelPort se define como 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="261ad-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

