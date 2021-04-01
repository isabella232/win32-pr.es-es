---
title: Propiedad de recuento de IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera el número de tareas de esta colección.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMTaskCollection
- Interfaz IVMTaskCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905432"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="35ac5-106">IVMTaskCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="35ac5-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="35ac5-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35ac5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35ac5-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35ac5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35ac5-109">Recupera el número de tareas de esta colección.</span><span class="sxs-lookup"><span data-stu-id="35ac5-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="35ac5-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="35ac5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ac5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35ac5-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="35ac5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="35ac5-112">Property value</span></span>

<span data-ttu-id="35ac5-113">El número de tareas.</span><span class="sxs-lookup"><span data-stu-id="35ac5-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35ac5-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="35ac5-114">Error codes</span></span>



| <span data-ttu-id="35ac5-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="35ac5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="35ac5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="35ac5-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="35ac5-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35ac5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="35ac5-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="35ac5-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="35ac5-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="35ac5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="35ac5-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="35ac5-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="35ac5-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="35ac5-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="35ac5-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="35ac5-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="35ac5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ac5-123">Requirements</span></span>



| <span data-ttu-id="35ac5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ac5-124">Requirement</span></span> | <span data-ttu-id="35ac5-125">Value</span><span class="sxs-lookup"><span data-stu-id="35ac5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ac5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ac5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35ac5-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="35ac5-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35ac5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ac5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35ac5-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35ac5-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35ac5-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="35ac5-130">End of client support</span></span><br/>    | <span data-ttu-id="35ac5-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35ac5-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35ac5-132">Producto</span><span class="sxs-lookup"><span data-stu-id="35ac5-132">Product</span></span><br/>                  | <span data-ttu-id="35ac5-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35ac5-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35ac5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35ac5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ac5-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ac5-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35ac5-136">IID</span><span class="sxs-lookup"><span data-stu-id="35ac5-136">IID</span></span><br/>                      | <span data-ttu-id="35ac5-137">IID \_ IVMTaskCollection se define como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="35ac5-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="35ac5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ac5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ac5-139">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="35ac5-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

