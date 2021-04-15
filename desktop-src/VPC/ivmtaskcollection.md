---
title: Interfaz IVMTaskCollection (VPCCOMInterfaces. h)
description: Define la colección de objetos Task. Para obtener un objeto IVMTaskCollection, use la propiedad Tasks de IVMVirtualPC.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Interfaz IVMTaskCollection Virtual PC
- Interfaz IVMTaskCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422505"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="da3c0-106">Interfaz IVMTaskCollection</span><span class="sxs-lookup"><span data-stu-id="da3c0-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="da3c0-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da3c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="da3c0-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da3c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="da3c0-109">Define la colección de objetos Task.</span><span class="sxs-lookup"><span data-stu-id="da3c0-109">Defines the collection of task objects.</span></span> <span data-ttu-id="da3c0-110">Para obtener un objeto **IVMTaskCollection** , use la propiedad [**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="da3c0-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="da3c0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="da3c0-111">Members</span></span>

<span data-ttu-id="da3c0-112">La interfaz **IVMTaskCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="da3c0-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="da3c0-113">**IVMTaskCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="da3c0-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="da3c0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da3c0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da3c0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da3c0-115">Properties</span></span>

<span data-ttu-id="da3c0-116">La interfaz **IVMTaskCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="da3c0-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="da3c0-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da3c0-117">Property</span></span>                                                   | <span data-ttu-id="da3c0-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="da3c0-118">Access type</span></span>          | <span data-ttu-id="da3c0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="da3c0-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="da3c0-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="da3c0-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="da3c0-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="da3c0-121">Read-only</span></span><br/> | <span data-ttu-id="da3c0-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="da3c0-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="da3c0-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="da3c0-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="da3c0-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="da3c0-124">Read-only</span></span><br/> | <span data-ttu-id="da3c0-125">Número de tareas de esta colección.</span><span class="sxs-lookup"><span data-stu-id="da3c0-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="da3c0-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da3c0-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="da3c0-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="da3c0-127">Read-only</span></span><br/> | <span data-ttu-id="da3c0-128">Objeto de tarea que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="da3c0-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="da3c0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da3c0-129">Requirements</span></span>



| <span data-ttu-id="da3c0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="da3c0-130">Requirement</span></span> | <span data-ttu-id="da3c0-131">Value</span><span class="sxs-lookup"><span data-stu-id="da3c0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3c0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da3c0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="da3c0-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="da3c0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da3c0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da3c0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="da3c0-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="da3c0-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="da3c0-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="da3c0-136">End of client support</span></span><br/>    | <span data-ttu-id="da3c0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da3c0-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="da3c0-138">Producto</span><span class="sxs-lookup"><span data-stu-id="da3c0-138">Product</span></span><br/>                  | <span data-ttu-id="da3c0-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="da3c0-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="da3c0-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da3c0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="da3c0-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="da3c0-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="da3c0-142">IID</span><span class="sxs-lookup"><span data-stu-id="da3c0-142">IID</span></span><br/>                      | <span data-ttu-id="da3c0-143">IID \_ IVMTaskCollection se define como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="da3c0-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="da3c0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="da3c0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3c0-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="da3c0-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="da3c0-146">**IVMVirtualPC:: Tasks**</span><span class="sxs-lookup"><span data-stu-id="da3c0-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

