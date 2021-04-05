---
title: Propiedad IVMVirtualPC SuggestedMaximumMemoryPerVM (VPCCOMInterfaces. h)
description: Recupera la cantidad máxima de memoria física sugerida para cada máquina virtual, en megabytes, para evitar las condiciones de memoria insuficiente en el host.
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- Propiedad SuggestedMaximumMemoryPerVM Virtual PC
- Propiedad SuggestedMaximumMemoryPerVM Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad SuggestedMaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142c4ade861116876342d598fbf10b5925fa100e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079763"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a><span data-ttu-id="0009b-106">IVMVirtualPC:: SuggestedMaximumMemoryPerVM (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0009b-106">IVMVirtualPC::SuggestedMaximumMemoryPerVM property</span></span>

<span data-ttu-id="0009b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0009b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0009b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0009b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0009b-109">Recupera la cantidad máxima de memoria física sugerida para cada máquina virtual, en megabytes, para evitar las condiciones de memoria insuficiente en el host.</span><span class="sxs-lookup"><span data-stu-id="0009b-109">Retrieves the suggested maximum allowable quantity of physical memory per virtual machine, in megabytes, to avoid low memory conditions on the host.</span></span>

<span data-ttu-id="0009b-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0009b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0009b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0009b-111">Syntax</span></span>


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="0009b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0009b-112">Property value</span></span>

<span data-ttu-id="0009b-113">La cantidad máxima permitida, en megabytes, de la memoria física por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0009b-113">The suggested maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0009b-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0009b-114">Error codes</span></span>



| <span data-ttu-id="0009b-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="0009b-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="0009b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0009b-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0009b-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0009b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="0009b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0009b-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0009b-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0009b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="0009b-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="0009b-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0009b-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0009b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="0009b-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0009b-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="0009b-123"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="0009b-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="0009b-124">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="0009b-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0009b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0009b-125">Requirements</span></span>



| <span data-ttu-id="0009b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0009b-126">Requirement</span></span> | <span data-ttu-id="0009b-127">Value</span><span class="sxs-lookup"><span data-stu-id="0009b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0009b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0009b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0009b-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0009b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0009b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0009b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0009b-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0009b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0009b-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0009b-132">End of client support</span></span><br/>    | <span data-ttu-id="0009b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0009b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0009b-134">Producto</span><span class="sxs-lookup"><span data-stu-id="0009b-134">Product</span></span><br/>                  | <span data-ttu-id="0009b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0009b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0009b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0009b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0009b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0009b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0009b-138">IID</span><span class="sxs-lookup"><span data-stu-id="0009b-138">IID</span></span><br/>                      | <span data-ttu-id="0009b-139">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="0009b-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0009b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0009b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0009b-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="0009b-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

