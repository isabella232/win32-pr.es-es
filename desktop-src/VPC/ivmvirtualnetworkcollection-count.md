---
title: Propiedad de recuento de IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Recupera el número de redes virtuales de esta colección.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMVirtualNetworkCollection
- Interfaz IVMVirtualNetworkCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803200"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="386dc-106">IVMVirtualNetworkCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="386dc-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="386dc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="386dc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="386dc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="386dc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="386dc-109">Recupera el número de redes virtuales de esta colección.</span><span class="sxs-lookup"><span data-stu-id="386dc-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="386dc-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="386dc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="386dc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="386dc-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="386dc-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="386dc-112">Property value</span></span>

<span data-ttu-id="386dc-113">El número de redes virtuales.</span><span class="sxs-lookup"><span data-stu-id="386dc-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="386dc-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="386dc-114">Error codes</span></span>



| <span data-ttu-id="386dc-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="386dc-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="386dc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="386dc-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="386dc-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="386dc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="386dc-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="386dc-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="386dc-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="386dc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="386dc-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="386dc-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="386dc-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="386dc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="386dc-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="386dc-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="386dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="386dc-123">Requirements</span></span>



| <span data-ttu-id="386dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="386dc-124">Requirement</span></span> | <span data-ttu-id="386dc-125">Value</span><span class="sxs-lookup"><span data-stu-id="386dc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="386dc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="386dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="386dc-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="386dc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="386dc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="386dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="386dc-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="386dc-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="386dc-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="386dc-130">End of client support</span></span><br/>    | <span data-ttu-id="386dc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="386dc-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="386dc-132">Producto</span><span class="sxs-lookup"><span data-stu-id="386dc-132">Product</span></span><br/>                  | <span data-ttu-id="386dc-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="386dc-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="386dc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="386dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="386dc-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="386dc-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="386dc-136">IID</span><span class="sxs-lookup"><span data-stu-id="386dc-136">IID</span></span><br/>                      | <span data-ttu-id="386dc-137">IID \_ IVMVirtualNetworkCollection se define como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="386dc-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="386dc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="386dc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386dc-139">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="386dc-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

