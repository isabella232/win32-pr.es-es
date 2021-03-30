---
title: Propiedad IVMVirtualMachine Velocidaddeprocesador (VPCCOMInterfaces. h)
description: Velocidad del procesador, en megahercios (MHz) o gigahercios (GHz).
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- Propiedad Velocidaddeprocesador Virtual PC
- Propiedad Velocidaddeprocesador Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad Velocidaddeprocesador
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492568"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a><span data-ttu-id="b5f6d-106">IVMVirtualMachine::P propiedad rocessorSpeed</span><span class="sxs-lookup"><span data-stu-id="b5f6d-106">IVMVirtualMachine::ProcessorSpeed property</span></span>

<span data-ttu-id="b5f6d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b5f6d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5f6d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b5f6d-109">Recupera la velocidad del procesador, en megahercios (MHz) o gigahercios (GHz).</span><span class="sxs-lookup"><span data-stu-id="b5f6d-109">Retrieves the speed of the processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="b5f6d-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f6d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5f6d-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="b5f6d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5f6d-112">Property value</span></span>

<span data-ttu-id="b5f6d-113">La velocidad, en megahercios o gigahercios.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-113">The speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5f6d-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b5f6d-114">Error codes</span></span>



| <span data-ttu-id="b5f6d-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b5f6d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b5f6d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f6d-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b5f6d-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5f6d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b5f6d-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b5f6d-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b5f6d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b5f6d-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b5f6d-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b5f6d-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b5f6d-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b5f6d-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b5f6d-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b5f6d-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b5f6d-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b5f6d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f6d-125">Requirements</span></span>



| <span data-ttu-id="b5f6d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f6d-126">Requirement</span></span> | <span data-ttu-id="b5f6d-127">Value</span><span class="sxs-lookup"><span data-stu-id="b5f6d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f6d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5f6d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f6d-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5f6d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5f6d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5f6d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f6d-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b5f6d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b5f6d-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b5f6d-132">End of client support</span></span><br/>    | <span data-ttu-id="b5f6d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b5f6d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b5f6d-134">Producto</span><span class="sxs-lookup"><span data-stu-id="b5f6d-134">Product</span></span><br/>                  | <span data-ttu-id="b5f6d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b5f6d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b5f6d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5f6d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f6d-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f6d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b5f6d-138">IID</span><span class="sxs-lookup"><span data-stu-id="b5f6d-138">IID</span></span><br/>                      | <span data-ttu-id="b5f6d-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b5f6d-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b5f6d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5f6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f6d-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b5f6d-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

