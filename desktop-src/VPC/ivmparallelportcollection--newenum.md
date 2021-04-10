---
title: Propiedad _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
ms.assetid: 2e26fba7-bcc0-4bb3-bf89-3c62cbd2b37e
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMParallelPortCollection
- Interfaz IVMParallelPortCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMParallelPortCollection._NewEnum
- IVMParallelPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7b0a7330e38abaa604c84c2b703bd5d908619a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003498"
---
# <a name="ivmparallelportcollection_newenum-property"></a><span data-ttu-id="abad8-107">IVMParallelPortCollection:: \_ NewEnum (propiedad)</span><span class="sxs-lookup"><span data-stu-id="abad8-107">IVMParallelPortCollection::\_NewEnum property</span></span>

<span data-ttu-id="abad8-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abad8-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="abad8-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="abad8-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="abad8-110">Recupera un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="abad8-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="abad8-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="abad8-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abad8-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abad8-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="abad8-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="abad8-113">Property value</span></span>

<span data-ttu-id="abad8-114">Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="abad8-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="abad8-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="abad8-115">Error codes</span></span>



| <span data-ttu-id="abad8-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="abad8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="abad8-117">Significado</span><span class="sxs-lookup"><span data-stu-id="abad8-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="abad8-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="abad8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="abad8-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="abad8-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="abad8-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="abad8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="abad8-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="abad8-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="abad8-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="abad8-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="abad8-123">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="abad8-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="abad8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abad8-124">Requirements</span></span>



| <span data-ttu-id="abad8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="abad8-125">Requirement</span></span> | <span data-ttu-id="abad8-126">Value</span><span class="sxs-lookup"><span data-stu-id="abad8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abad8-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abad8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="abad8-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="abad8-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abad8-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abad8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="abad8-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="abad8-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="abad8-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="abad8-131">End of client support</span></span><br/>    | <span data-ttu-id="abad8-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abad8-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="abad8-133">Producto</span><span class="sxs-lookup"><span data-stu-id="abad8-133">Product</span></span><br/>                  | <span data-ttu-id="abad8-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="abad8-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="abad8-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abad8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="abad8-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="abad8-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="abad8-137">IID</span><span class="sxs-lookup"><span data-stu-id="abad8-137">IID</span></span><br/>                      | <span data-ttu-id="abad8-138">IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="abad8-138">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="abad8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="abad8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abad8-140">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="abad8-140">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

