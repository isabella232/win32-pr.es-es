---
title: Propiedad de recuento de IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Número de puertos paralelos de esta colección.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMParallelPortCollection
- Interfaz IVMParallelPortCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996484"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="7432f-106">IVMParallelPortCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7432f-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="7432f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7432f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7432f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7432f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7432f-109">Recupera el número de puertos paralelos de esta colección.</span><span class="sxs-lookup"><span data-stu-id="7432f-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="7432f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7432f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7432f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7432f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="7432f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7432f-112">Property value</span></span>

<span data-ttu-id="7432f-113">El número de puertos paralelos.</span><span class="sxs-lookup"><span data-stu-id="7432f-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7432f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7432f-114">Error codes</span></span>



| <span data-ttu-id="7432f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="7432f-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="7432f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7432f-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="7432f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7432f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="7432f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7432f-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="7432f-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7432f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="7432f-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="7432f-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="7432f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7432f-121">Requirements</span></span>



| <span data-ttu-id="7432f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7432f-122">Requirement</span></span> | <span data-ttu-id="7432f-123">Value</span><span class="sxs-lookup"><span data-stu-id="7432f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7432f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7432f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7432f-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7432f-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7432f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7432f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7432f-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7432f-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7432f-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7432f-128">End of client support</span></span><br/>    | <span data-ttu-id="7432f-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7432f-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7432f-130">Producto</span><span class="sxs-lookup"><span data-stu-id="7432f-130">Product</span></span><br/>                  | <span data-ttu-id="7432f-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7432f-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7432f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7432f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7432f-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7432f-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7432f-134">IID</span><span class="sxs-lookup"><span data-stu-id="7432f-134">IID</span></span><br/>                      | <span data-ttu-id="7432f-135">IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="7432f-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7432f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7432f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7432f-137">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="7432f-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

