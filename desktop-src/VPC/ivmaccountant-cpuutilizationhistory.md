---
title: Propiedad IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces. h)
description: Recupera el uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Propiedad CPUUtilizationHistory Virtual PC
- Propiedad CPUUtilizationHistory Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492911"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="2cf8e-106">IVMAccountant:: CPUUtilizationHistory (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2cf8e-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="2cf8e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2cf8e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2cf8e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2cf8e-109">Recupera el uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).</span><span class="sxs-lookup"><span data-stu-id="2cf8e-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="2cf8e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf8e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cf8e-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="2cf8e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2cf8e-112">Property value</span></span>

<span data-ttu-id="2cf8e-113">El uso de CPU reciente de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="2cf8e-114">Estos datos se devuelven como una matriz de 60 elementos que representan el porcentaje de uso de CPU en cada segundo durante el último minuto.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="2cf8e-115">Variant Type es VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cf8e-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2cf8e-116">Error codes</span></span>



| <span data-ttu-id="2cf8e-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="2cf8e-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2cf8e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="2cf8e-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cf8e-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2cf8e-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2cf8e-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2cf8e-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2cf8e-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2cf8e-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="2cf8e-123"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2cf8e-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="2cf8e-124">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-124">The virtual machine is not running.</span></span> <span data-ttu-id="2cf8e-125">Todos los elementos de la matriz 60 se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="2cf8e-126"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2cf8e-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2cf8e-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2cf8e-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="2cf8e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf8e-128">Requirements</span></span>



| <span data-ttu-id="2cf8e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf8e-129">Requirement</span></span> | <span data-ttu-id="2cf8e-130">Value</span><span class="sxs-lookup"><span data-stu-id="2cf8e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf8e-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf8e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf8e-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cf8e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cf8e-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf8e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf8e-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2cf8e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2cf8e-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2cf8e-135">End of client support</span></span><br/>    | <span data-ttu-id="2cf8e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cf8e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2cf8e-137">Producto</span><span class="sxs-lookup"><span data-stu-id="2cf8e-137">Product</span></span><br/>                  | <span data-ttu-id="2cf8e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2cf8e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2cf8e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cf8e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf8e-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf8e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2cf8e-141">IID</span><span class="sxs-lookup"><span data-stu-id="2cf8e-141">IID</span></span><br/>                      | <span data-ttu-id="2cf8e-142">IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="2cf8e-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="2cf8e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf8e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf8e-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="2cf8e-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

