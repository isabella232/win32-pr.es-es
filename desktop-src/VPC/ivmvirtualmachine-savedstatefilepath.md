---
title: Propiedad IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces. h)
description: Recupera la ruta de acceso completa al archivo de estado guardado.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Propiedad SavedStateFilePath Virtual PC
- Propiedad SavedStateFilePath Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad SavedStateFilePath
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150839"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="83d66-106">IVMVirtualMachine:: SavedStateFilePath (propiedad)</span><span class="sxs-lookup"><span data-stu-id="83d66-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="83d66-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83d66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="83d66-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="83d66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="83d66-109">Recupera la ruta de acceso completa al archivo de estado guardado.</span><span class="sxs-lookup"><span data-stu-id="83d66-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="83d66-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="83d66-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d66-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83d66-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="83d66-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="83d66-112">Property value</span></span>

<span data-ttu-id="83d66-113">Ruta de acceso completa al archivo de estado guardado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83d66-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="83d66-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="83d66-114">Error codes</span></span>



| <span data-ttu-id="83d66-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="83d66-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="83d66-116">Significado</span><span class="sxs-lookup"><span data-stu-id="83d66-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="83d66-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83d66-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="83d66-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="83d66-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="83d66-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="83d66-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="83d66-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="83d66-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="83d66-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="83d66-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="83d66-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="83d66-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="83d66-123"><dt>Máquina virtual \_ NO se ha \_ \_ guardado el \_ \_ Estado de la máquina virtual</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="83d66-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="83d66-124">La máquina virtual no tiene ningún archivo de estado guardado asociado.</span><span class="sxs-lookup"><span data-stu-id="83d66-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="83d66-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="83d66-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="83d66-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="83d66-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="83d66-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83d66-127">Requirements</span></span>



| <span data-ttu-id="83d66-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83d66-128">Requirement</span></span> | <span data-ttu-id="83d66-129">Value</span><span class="sxs-lookup"><span data-stu-id="83d66-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d66-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83d66-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83d66-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="83d66-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83d66-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83d66-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83d66-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="83d66-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="83d66-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="83d66-134">End of client support</span></span><br/>    | <span data-ttu-id="83d66-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83d66-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="83d66-136">Producto</span><span class="sxs-lookup"><span data-stu-id="83d66-136">Product</span></span><br/>                  | <span data-ttu-id="83d66-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="83d66-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="83d66-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83d66-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="83d66-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="83d66-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="83d66-140">IID</span><span class="sxs-lookup"><span data-stu-id="83d66-140">IID</span></span><br/>                      | <span data-ttu-id="83d66-141">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="83d66-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="83d66-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="83d66-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d66-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="83d66-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

