---
title: Propiedad IVMVirtualMachine ParallelPorts (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de puertos paralelos.
ms.assetid: 458e6e77-3728-4b5c-910b-f958f42785e4
keywords:
- Propiedad ParallelPorts Virtual PC
- Propiedad ParallelPorts Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad ParallelPorts
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ParallelPorts
- IVMVirtualMachine.get_ParallelPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aba742a206857e73e0d1447f422f7182fb7a304
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150943"
---
# <a name="ivmvirtualmachineparallelports-property"></a><span data-ttu-id="b9bae-106">IVMVirtualMachine::P propiedad arallelPorts</span><span class="sxs-lookup"><span data-stu-id="b9bae-106">IVMVirtualMachine::ParallelPorts property</span></span>

<span data-ttu-id="b9bae-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b9bae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b9bae-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b9bae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b9bae-109">Recupera una colección enumerable de puertos paralelos.</span><span class="sxs-lookup"><span data-stu-id="b9bae-109">Retrieves an enumerable collection of parallel ports.</span></span>

<span data-ttu-id="b9bae-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b9bae-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9bae-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9bae-111">Syntax</span></span>


```C++
HRESULT get_ParallelPorts(
  [out, retval] IVMParallelPortCollection **parallelPortCollection
);
```



## <a name="property-value"></a><span data-ttu-id="b9bae-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9bae-112">Property value</span></span>

<span data-ttu-id="b9bae-113">Objeto [**IVMParallelPortCollection**](ivmparallelportcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bae-113">An [**IVMParallelPortCollection**](ivmparallelportcollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9bae-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b9bae-114">Error codes</span></span>



| <span data-ttu-id="b9bae-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b9bae-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b9bae-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b9bae-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b9bae-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9bae-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b9bae-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9bae-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b9bae-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b9bae-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b9bae-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b9bae-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b9bae-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b9bae-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b9bae-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="b9bae-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b9bae-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b9bae-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b9bae-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b9bae-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b9bae-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9bae-125">Requirements</span></span>



| <span data-ttu-id="b9bae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9bae-126">Requirement</span></span> | <span data-ttu-id="b9bae-127">Value</span><span class="sxs-lookup"><span data-stu-id="b9bae-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bae-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9bae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b9bae-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9bae-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9bae-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9bae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b9bae-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9bae-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b9bae-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b9bae-132">End of client support</span></span><br/>    | <span data-ttu-id="b9bae-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9bae-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b9bae-134">Producto</span><span class="sxs-lookup"><span data-stu-id="b9bae-134">Product</span></span><br/>                  | <span data-ttu-id="b9bae-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b9bae-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b9bae-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9bae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9bae-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9bae-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b9bae-138">IID</span><span class="sxs-lookup"><span data-stu-id="b9bae-138">IID</span></span><br/>                      | <span data-ttu-id="b9bae-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b9bae-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b9bae-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9bae-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bae-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b9bae-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

