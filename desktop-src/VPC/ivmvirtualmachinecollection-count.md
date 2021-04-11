---
title: Propiedad de recuento de IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera el número de máquinas virtuales de esta colección.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMVirtualMachineCollection
- Interfaz IVMVirtualMachineCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150942"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="fe04a-106">IVMVirtualMachineCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fe04a-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="fe04a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fe04a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fe04a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fe04a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fe04a-109">Recupera el número de máquinas virtuales de esta colección.</span><span class="sxs-lookup"><span data-stu-id="fe04a-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="fe04a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe04a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe04a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe04a-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="fe04a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fe04a-112">Property value</span></span>

<span data-ttu-id="fe04a-113">El número de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fe04a-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe04a-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fe04a-114">Error codes</span></span>



| <span data-ttu-id="fe04a-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="fe04a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fe04a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fe04a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fe04a-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe04a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fe04a-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe04a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="fe04a-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fe04a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fe04a-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="fe04a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="fe04a-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fe04a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fe04a-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fe04a-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fe04a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe04a-123">Requirements</span></span>



| <span data-ttu-id="fe04a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe04a-124">Requirement</span></span> | <span data-ttu-id="fe04a-125">Value</span><span class="sxs-lookup"><span data-stu-id="fe04a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe04a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe04a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fe04a-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe04a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe04a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe04a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fe04a-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe04a-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fe04a-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fe04a-130">End of client support</span></span><br/>    | <span data-ttu-id="fe04a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe04a-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="fe04a-132">Producto</span><span class="sxs-lookup"><span data-stu-id="fe04a-132">Product</span></span><br/>                  | <span data-ttu-id="fe04a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fe04a-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="fe04a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe04a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe04a-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe04a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="fe04a-136">IID</span><span class="sxs-lookup"><span data-stu-id="fe04a-136">IID</span></span><br/>                      | <span data-ttu-id="fe04a-137">IID \_ IVMVirtualMachineCollection se define como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="fe04a-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe04a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe04a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe04a-139">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="fe04a-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

