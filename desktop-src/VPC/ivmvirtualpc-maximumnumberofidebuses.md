---
title: Propiedad IVMVirtualPC MaximumNumberOfIDEBuses (VPCCOMInterfaces. h)
description: Recupera el número máximo de buses permitidos para el IDE.
ms.assetid: 7b88eda4-0f66-4e26-96cb-1e9ebef9d0b8
keywords:
- Propiedad MaximumNumberOfIDEBuses Virtual PC
- Propiedad MaximumNumberOfIDEBuses Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad MaximumNumberOfIDEBuses
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNumberOfIDEBuses
- IVMVirtualPC.get_MaximumNumberOfIDEBuses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceabc071c0bf294eed3423d36c2c019586754101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078804"
---
# <a name="ivmvirtualpcmaximumnumberofidebuses-property"></a><span data-ttu-id="ff67f-106">IVMVirtualPC:: MaximumNumberOfIDEBuses (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ff67f-106">IVMVirtualPC::MaximumNumberOfIDEBuses property</span></span>

<span data-ttu-id="ff67f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ff67f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff67f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff67f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff67f-109">Recupera el número máximo de buses permitidos para el IDE.</span><span class="sxs-lookup"><span data-stu-id="ff67f-109">Retrieves the maximum number of buses allowed for IDE.</span></span>

<span data-ttu-id="ff67f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff67f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff67f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff67f-111">Syntax</span></span>


```C++
HRESULT get_MaximumNumberOfIDEBuses(
  [out, retval] long *maxNumBuses
);
```



## <a name="property-value"></a><span data-ttu-id="ff67f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ff67f-112">Property value</span></span>

<span data-ttu-id="ff67f-113">Número máximo de buses permitidos para IDE.</span><span class="sxs-lookup"><span data-stu-id="ff67f-113">The maximum number of buses allowed for IDE.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff67f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ff67f-114">Error codes</span></span>



| <span data-ttu-id="ff67f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="ff67f-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="ff67f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ff67f-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff67f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff67f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ff67f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff67f-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ff67f-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ff67f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="ff67f-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ff67f-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ff67f-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ff67f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="ff67f-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ff67f-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ff67f-123"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ff67f-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="ff67f-124">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="ff67f-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff67f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff67f-125">Requirements</span></span>



| <span data-ttu-id="ff67f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff67f-126">Requirement</span></span> | <span data-ttu-id="ff67f-127">Value</span><span class="sxs-lookup"><span data-stu-id="ff67f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff67f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff67f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff67f-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff67f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff67f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff67f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff67f-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ff67f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff67f-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ff67f-132">End of client support</span></span><br/>    | <span data-ttu-id="ff67f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff67f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff67f-134">Producto</span><span class="sxs-lookup"><span data-stu-id="ff67f-134">Product</span></span><br/>                  | <span data-ttu-id="ff67f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff67f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff67f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff67f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff67f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff67f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff67f-138">IID</span><span class="sxs-lookup"><span data-stu-id="ff67f-138">IID</span></span><br/>                      | <span data-ttu-id="ff67f-139">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ff67f-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ff67f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff67f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff67f-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="ff67f-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

