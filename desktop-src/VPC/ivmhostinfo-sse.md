---
title: Propiedad IVMHostInfo SSE (VPCCOMInterfaces. h)
description: Determina si el procesador admite el conjunto de instrucciones SSE. | Propiedad IVMHostInfo SSE (VPCCOMInterfaces. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- Propiedad SSE de Virtual PC
- Propiedad SSE Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362295"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="ead83-107">IVMHostInfo:: SSE (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ead83-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="ead83-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ead83-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ead83-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ead83-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ead83-110">Determina si el procesador admite el conjunto de instrucciones SSE.</span><span class="sxs-lookup"><span data-stu-id="ead83-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="ead83-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ead83-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead83-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ead83-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="ead83-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ead83-113">Property value</span></span>

<span data-ttu-id="ead83-114">**True** si el procesador del host admite las instrucciones de SSE; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="ead83-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ead83-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ead83-115">Error codes</span></span>



| <span data-ttu-id="ead83-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="ead83-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ead83-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ead83-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ead83-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ead83-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ead83-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ead83-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ead83-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ead83-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ead83-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ead83-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ead83-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ead83-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ead83-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ead83-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ead83-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead83-124">Requirements</span></span>



| <span data-ttu-id="ead83-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead83-125">Requirement</span></span> | <span data-ttu-id="ead83-126">Value</span><span class="sxs-lookup"><span data-stu-id="ead83-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead83-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead83-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ead83-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ead83-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ead83-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead83-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ead83-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ead83-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ead83-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ead83-131">End of client support</span></span><br/>    | <span data-ttu-id="ead83-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ead83-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ead83-133">Producto</span><span class="sxs-lookup"><span data-stu-id="ead83-133">Product</span></span><br/>                  | <span data-ttu-id="ead83-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ead83-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ead83-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ead83-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead83-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead83-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ead83-137">IID</span><span class="sxs-lookup"><span data-stu-id="ead83-137">IID</span></span><br/>                      | <span data-ttu-id="ead83-138">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="ead83-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ead83-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ead83-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead83-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="ead83-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

