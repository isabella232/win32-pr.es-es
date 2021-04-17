---
title: Propiedad IVMVirtualPC MaximumParallelPortsPerVM (VPCCOMInterfaces. h)
description: Recupera el número máximo de puertos paralelos por máquina virtual.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- Propiedad MaximumParallelPortsPerVM Virtual PC
- Propiedad MaximumParallelPortsPerVM Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad MaximumParallelPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c5bed446a421190eb47630bde0d05f0cbcee7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695948"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a><span data-ttu-id="76ce2-106">IVMVirtualPC:: MaximumParallelPortsPerVM (propiedad)</span><span class="sxs-lookup"><span data-stu-id="76ce2-106">IVMVirtualPC::MaximumParallelPortsPerVM property</span></span>

<span data-ttu-id="76ce2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76ce2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76ce2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76ce2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76ce2-109">Recupera el número máximo de puertos paralelos por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="76ce2-109">Retrieves the maximum number of parallel ports per virtual machine.</span></span>

<span data-ttu-id="76ce2-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76ce2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ce2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76ce2-111">Syntax</span></span>


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="76ce2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="76ce2-112">Property value</span></span>

<span data-ttu-id="76ce2-113">El número máximo de puertos paralelos por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="76ce2-113">The maximum number of parallel ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="76ce2-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="76ce2-114">Error codes</span></span>



| <span data-ttu-id="76ce2-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="76ce2-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="76ce2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="76ce2-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76ce2-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76ce2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="76ce2-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="76ce2-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="76ce2-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="76ce2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="76ce2-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="76ce2-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="76ce2-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="76ce2-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="76ce2-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="76ce2-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="76ce2-123"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="76ce2-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="76ce2-124">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="76ce2-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="76ce2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ce2-125">Requirements</span></span>



| <span data-ttu-id="76ce2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ce2-126">Requirement</span></span> | <span data-ttu-id="76ce2-127">Value</span><span class="sxs-lookup"><span data-stu-id="76ce2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ce2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ce2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="76ce2-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="76ce2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76ce2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ce2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="76ce2-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="76ce2-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76ce2-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="76ce2-132">End of client support</span></span><br/>    | <span data-ttu-id="76ce2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76ce2-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76ce2-134">Producto</span><span class="sxs-lookup"><span data-stu-id="76ce2-134">Product</span></span><br/>                  | <span data-ttu-id="76ce2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76ce2-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76ce2-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76ce2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ce2-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ce2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76ce2-138">IID</span><span class="sxs-lookup"><span data-stu-id="76ce2-138">IID</span></span><br/>                      | <span data-ttu-id="76ce2-139">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="76ce2-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="76ce2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="76ce2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ce2-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="76ce2-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

