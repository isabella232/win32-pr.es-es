---
title: Propiedad UndoAction de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Acción predeterminada que se realizará en todas las unidades de deshacer cuando se apague la máquina virtual.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Propiedad UndoAction Virtual PC
- Propiedad UndoAction Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad UndoAction
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492214"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="658cc-106">IVMVirtualMachine:: UndoAction (propiedad)</span><span class="sxs-lookup"><span data-stu-id="658cc-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="658cc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="658cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="658cc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="658cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="658cc-109">Recupera y establece la acción predeterminada que se va a realizar en todas las unidades de deshacer cuando se desactiva la máquina virtual con el [**método de**](ivmvirtualmachine-turnoff.md) desactivación o se apaga con el método [**Shutdown**](ivmguestos-shutdown.md) o se desactiva desde dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="658cc-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="658cc-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="658cc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="658cc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="658cc-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="658cc-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="658cc-112">Property value</span></span>

<span data-ttu-id="658cc-113">Especifica la acción predeterminada que se realizará en todas las unidades de deshacer cuando se apague la máquina virtual desde el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="658cc-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="658cc-114">Para obtener una lista de valores, vea [**VMUndoAction**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="658cc-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="658cc-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="658cc-115">Error codes</span></span>



| <span data-ttu-id="658cc-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="658cc-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="658cc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="658cc-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="658cc-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="658cc-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="658cc-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="658cc-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="658cc-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="658cc-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="658cc-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="658cc-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="658cc-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="658cc-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="658cc-123">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="658cc-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="658cc-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="658cc-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="658cc-125">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="658cc-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="658cc-126"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="658cc-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="658cc-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="658cc-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="658cc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="658cc-128">Requirements</span></span>



| <span data-ttu-id="658cc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="658cc-129">Requirement</span></span> | <span data-ttu-id="658cc-130">Value</span><span class="sxs-lookup"><span data-stu-id="658cc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="658cc-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="658cc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="658cc-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="658cc-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="658cc-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="658cc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="658cc-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="658cc-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="658cc-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="658cc-135">End of client support</span></span><br/>    | <span data-ttu-id="658cc-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="658cc-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="658cc-137">Producto</span><span class="sxs-lookup"><span data-stu-id="658cc-137">Product</span></span><br/>                  | <span data-ttu-id="658cc-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="658cc-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="658cc-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="658cc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="658cc-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="658cc-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="658cc-141">IID</span><span class="sxs-lookup"><span data-stu-id="658cc-141">IID</span></span><br/>                      | <span data-ttu-id="658cc-142">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="658cc-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="658cc-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="658cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658cc-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="658cc-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

