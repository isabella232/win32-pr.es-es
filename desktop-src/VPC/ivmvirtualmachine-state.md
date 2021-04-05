---
title: Propiedad de estado IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera el estado actual de la máquina virtual.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Propiedad de estado Virtual PC
- Propiedad State Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad State
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996878"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="d3b59-106">IVMVirtualMachine:: State (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d3b59-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="d3b59-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3b59-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3b59-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3b59-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3b59-109">Recupera el estado actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3b59-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="d3b59-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d3b59-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b59-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3b59-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="d3b59-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d3b59-112">Property value</span></span>

<span data-ttu-id="d3b59-113">Estado actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3b59-113">The current state of the virtual machine.</span></span> <span data-ttu-id="d3b59-114">Para obtener una lista de valores, vea [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="d3b59-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3b59-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d3b59-115">Error codes</span></span>



| <span data-ttu-id="d3b59-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d3b59-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d3b59-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d3b59-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d3b59-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d3b59-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d3b59-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d3b59-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d3b59-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d3b59-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d3b59-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d3b59-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d3b59-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d3b59-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d3b59-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d3b59-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="d3b59-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d3b59-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d3b59-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d3b59-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d3b59-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3b59-126">Requirements</span></span>



| <span data-ttu-id="d3b59-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b59-127">Requirement</span></span> | <span data-ttu-id="d3b59-128">Value</span><span class="sxs-lookup"><span data-stu-id="d3b59-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b59-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3b59-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b59-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3b59-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3b59-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3b59-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b59-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d3b59-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3b59-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d3b59-133">End of client support</span></span><br/>    | <span data-ttu-id="d3b59-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3b59-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3b59-135">Producto</span><span class="sxs-lookup"><span data-stu-id="d3b59-135">Product</span></span><br/>                  | <span data-ttu-id="d3b59-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3b59-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3b59-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3b59-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b59-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b59-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3b59-139">IID</span><span class="sxs-lookup"><span data-stu-id="d3b59-139">IID</span></span><br/>                      | <span data-ttu-id="d3b59-140">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d3b59-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d3b59-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3b59-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b59-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d3b59-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

