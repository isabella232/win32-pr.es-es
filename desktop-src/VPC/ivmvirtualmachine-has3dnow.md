---
title: Propiedad IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
description: Determina si el procesador admite el conjunto de instrucciones 3DNow. | Propiedad IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
ms.assetid: 525ee7f0-081c-4f87-b2b7-ffec09f632c4
keywords:
- Propiedad Has3DNow Virtual PC
- Propiedad Has3DNow Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad Has3DNow
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Has3DNow
- IVMVirtualMachine.get_Has3DNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b347fa802b999707e43019e9b7808c844c0288f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820834"
---
# <a name="ivmvirtualmachinehas3dnow-property"></a><span data-ttu-id="684a2-107">IVMVirtualMachine:: Has3DNow (propiedad)</span><span class="sxs-lookup"><span data-stu-id="684a2-107">IVMVirtualMachine::Has3DNow property</span></span>

<span data-ttu-id="684a2-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="684a2-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="684a2-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="684a2-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="684a2-110">Determina si el procesador admite el conjunto de instrucciones 3DNow.</span><span class="sxs-lookup"><span data-stu-id="684a2-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="684a2-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="684a2-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="684a2-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="684a2-112">Syntax</span></span>


```C++
HRESULT get_Has3DNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="684a2-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="684a2-113">Property value</span></span>

<span data-ttu-id="684a2-114">**True** si el procesador admite el conjunto de instrucciones 3DNow; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="684a2-114">**TRUE** if the processor supported the 3DNow instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="684a2-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="684a2-115">Error codes</span></span>



| <span data-ttu-id="684a2-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="684a2-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="684a2-117">Significado</span><span class="sxs-lookup"><span data-stu-id="684a2-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="684a2-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="684a2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="684a2-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="684a2-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="684a2-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="684a2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="684a2-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="684a2-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="684a2-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="684a2-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="684a2-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="684a2-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="684a2-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="684a2-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="684a2-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="684a2-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="684a2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="684a2-126">Requirements</span></span>



| <span data-ttu-id="684a2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="684a2-127">Requirement</span></span> | <span data-ttu-id="684a2-128">Value</span><span class="sxs-lookup"><span data-stu-id="684a2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="684a2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="684a2-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="684a2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="684a2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="684a2-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="684a2-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="684a2-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="684a2-133">End of client support</span></span><br/>    | <span data-ttu-id="684a2-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="684a2-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="684a2-135">Producto</span><span class="sxs-lookup"><span data-stu-id="684a2-135">Product</span></span><br/>                  | <span data-ttu-id="684a2-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="684a2-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="684a2-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="684a2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="684a2-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="684a2-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="684a2-139">IID</span><span class="sxs-lookup"><span data-stu-id="684a2-139">IID</span></span><br/>                      | <span data-ttu-id="684a2-140">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="684a2-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="684a2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="684a2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684a2-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="684a2-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

