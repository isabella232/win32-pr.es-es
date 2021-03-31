---
title: Propiedad de recuento de IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Recupera el número de interfaces de red de esta colección.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMNetworkAdapterCollection
- Interfaz IVMNetworkAdapterCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149856"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="b969e-106">IVMNetworkAdapterCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b969e-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="b969e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b969e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b969e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b969e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b969e-109">Recupera el número de interfaces de red de esta colección.</span><span class="sxs-lookup"><span data-stu-id="b969e-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="b969e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b969e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b969e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b969e-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="b969e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b969e-112">Property value</span></span>

<span data-ttu-id="b969e-113">El número de interfaces de red.</span><span class="sxs-lookup"><span data-stu-id="b969e-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b969e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b969e-114">Error codes</span></span>



| <span data-ttu-id="b969e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b969e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b969e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b969e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b969e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b969e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b969e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b969e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b969e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b969e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b969e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b969e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b969e-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b969e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b969e-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b969e-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b969e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b969e-123">Requirements</span></span>



| <span data-ttu-id="b969e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b969e-124">Requirement</span></span> | <span data-ttu-id="b969e-125">Value</span><span class="sxs-lookup"><span data-stu-id="b969e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b969e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b969e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b969e-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b969e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b969e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b969e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b969e-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b969e-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b969e-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b969e-130">End of client support</span></span><br/>    | <span data-ttu-id="b969e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b969e-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="b969e-132">Producto</span><span class="sxs-lookup"><span data-stu-id="b969e-132">Product</span></span><br/>                  | <span data-ttu-id="b969e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b969e-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="b969e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b969e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b969e-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b969e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="b969e-136">IID</span><span class="sxs-lookup"><span data-stu-id="b969e-136">IID</span></span><br/>                      | <span data-ttu-id="b969e-137">IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-eBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="b969e-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b969e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b969e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b969e-139">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="b969e-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

