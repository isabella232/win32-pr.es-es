---
title: Propiedad IVMVirtualPC VirtualMachines (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de máquinas virtuales.
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- Propiedad VirtualMachines Virtual PC
- Propiedad VirtualMachines Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad VirtualMachines
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e141208994fa3d759074e7cbb294e1e2158917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651422"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a><span data-ttu-id="66c82-106">IVMVirtualPC:: VirtualMachines (propiedad)</span><span class="sxs-lookup"><span data-stu-id="66c82-106">IVMVirtualPC::VirtualMachines property</span></span>

<span data-ttu-id="66c82-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66c82-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66c82-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66c82-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66c82-109">Recupera una colección enumerable de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="66c82-109">Retrieves an enumerable collection of virtual machines.</span></span>

<span data-ttu-id="66c82-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="66c82-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c82-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66c82-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a><span data-ttu-id="66c82-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="66c82-112">Property value</span></span>

<span data-ttu-id="66c82-113">Colección de objetos [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="66c82-113">A collection of [**IVMVirtualMachine**](ivmvirtualmachine.md) objects.</span></span> <span data-ttu-id="66c82-114">Vea [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span><span class="sxs-lookup"><span data-stu-id="66c82-114">See [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="66c82-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="66c82-115">Error codes</span></span>



| <span data-ttu-id="66c82-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="66c82-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="66c82-117">Significado</span><span class="sxs-lookup"><span data-stu-id="66c82-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66c82-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66c82-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="66c82-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="66c82-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="66c82-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66c82-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="66c82-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="66c82-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="66c82-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66c82-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="66c82-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="66c82-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="66c82-124"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="66c82-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="66c82-125">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="66c82-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66c82-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66c82-126">Requirements</span></span>



| <span data-ttu-id="66c82-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c82-127">Requirement</span></span> | <span data-ttu-id="66c82-128">Value</span><span class="sxs-lookup"><span data-stu-id="66c82-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c82-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66c82-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66c82-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="66c82-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66c82-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66c82-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66c82-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66c82-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66c82-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="66c82-133">End of client support</span></span><br/>    | <span data-ttu-id="66c82-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66c82-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66c82-135">Producto</span><span class="sxs-lookup"><span data-stu-id="66c82-135">Product</span></span><br/>                  | <span data-ttu-id="66c82-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66c82-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66c82-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66c82-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c82-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c82-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66c82-139">IID</span><span class="sxs-lookup"><span data-stu-id="66c82-139">IID</span></span><br/>                      | <span data-ttu-id="66c82-140">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="66c82-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="66c82-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="66c82-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c82-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="66c82-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

