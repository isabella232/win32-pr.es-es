---
title: Propiedad IVMVirtualMachine HasSSE2 (VPCCOMInterfaces. h)
description: Determina si el procesador admite el conjunto de instrucciones SSE2. | Propiedad IVMVirtualMachine HasSSE2 (VPCCOMInterfaces. h)
ms.assetid: da9860cf-d1e4-4dc4-8c4c-1b83104ffbc6
keywords:
- Propiedad HasSSE2 Virtual PC
- Propiedad HasSSE2 Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad HasSSE2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE2
- IVMVirtualMachine.get_HasSSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18cd43919056a2a8563fc43b75d4c8fb8bd122a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653241"
---
# <a name="ivmvirtualmachinehassse2-property"></a><span data-ttu-id="3b0ad-107">IVMVirtualMachine:: HasSSE2 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3b0ad-107">IVMVirtualMachine::HasSSE2 property</span></span>

<span data-ttu-id="3b0ad-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3b0ad-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3b0ad-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3b0ad-110">Determina si el procesador admite el conjunto de instrucciones SSE2.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-110">Determines whether the processor supports the SSE2 instruction set.</span></span>

<span data-ttu-id="3b0ad-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0ad-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b0ad-112">Syntax</span></span>


```C++
HRESULT get_HasSSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="3b0ad-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3b0ad-113">Property value</span></span>

<span data-ttu-id="3b0ad-114">**True** si el procesador admite el conjunto de instrucciones SSE2, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-114">**TRUE** if the processor supported the SSE2 instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b0ad-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3b0ad-115">Error codes</span></span>



| <span data-ttu-id="3b0ad-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3b0ad-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3b0ad-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3b0ad-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3b0ad-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ad-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3b0ad-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3b0ad-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ad-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3b0ad-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3b0ad-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3b0ad-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3b0ad-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="3b0ad-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ad-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3b0ad-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3b0ad-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3b0ad-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b0ad-126">Requirements</span></span>



| <span data-ttu-id="3b0ad-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b0ad-127">Requirement</span></span> | <span data-ttu-id="3b0ad-128">Value</span><span class="sxs-lookup"><span data-stu-id="3b0ad-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0ad-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b0ad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0ad-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b0ad-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b0ad-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b0ad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0ad-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b0ad-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3b0ad-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3b0ad-133">End of client support</span></span><br/>    | <span data-ttu-id="3b0ad-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b0ad-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3b0ad-135">Producto</span><span class="sxs-lookup"><span data-stu-id="3b0ad-135">Product</span></span><br/>                  | <span data-ttu-id="3b0ad-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3b0ad-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3b0ad-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b0ad-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b0ad-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ad-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3b0ad-139">IID</span><span class="sxs-lookup"><span data-stu-id="3b0ad-139">IID</span></span><br/>                      | <span data-ttu-id="3b0ad-140">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3b0ad-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3b0ad-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b0ad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0ad-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3b0ad-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

