---
title: Propiedad IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Propiedad HasExclusiveAccess Virtual PC
- Propiedad HasExclusiveAccess Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, propiedad HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150952"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="b579b-106">IVMKeyboard:: HasExclusiveAccess (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b579b-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="b579b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b579b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b579b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b579b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b579b-109">Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado (VM) de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b579b-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="b579b-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b579b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b579b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b579b-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="b579b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b579b-112">Property value</span></span>

<span data-ttu-id="b579b-113">**True** si se ha adquirido acceso exclusivo al dispositivo de teclado de la máquina virtual; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="b579b-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b579b-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b579b-114">Error codes</span></span>



| <span data-ttu-id="b579b-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b579b-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="b579b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b579b-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b579b-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="b579b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b579b-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="b579b-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="b579b-120">El parámetro *isExclusive* es **null**.</span><span class="sxs-lookup"><span data-stu-id="b579b-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="b579b-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="b579b-122">El modo exclusivo solicitado ya está establecido para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b579b-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="b579b-123">Esto puede ocurrir cuando se intenta establecer el modo exclusivo cuando ya se ha adquirido o cuando se intenta liberar el modo exclusivo cuando no se ha adquirido previamente.</span><span class="sxs-lookup"><span data-stu-id="b579b-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="b579b-124"><dt>Máquina virtual \_ E \_ establezca \_ el \_ modo exclusivo \_ FAIL</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="b579b-125">No se pudo establecer o liberar el modo exclusivo como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="b579b-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="b579b-126">Esto puede deberse a que la máquina virtual ya no se está ejecutando o a que otro proceso ya ha adquirido el modo exclusivo en el dispositivo de teclado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b579b-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b579b-127"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="b579b-128">La cadena especificada está vacía o contiene un código de clave no válido.</span><span class="sxs-lookup"><span data-stu-id="b579b-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="b579b-129"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="b579b-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b579b-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="b579b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b579b-131">Requirements</span></span>



| <span data-ttu-id="b579b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b579b-132">Requirement</span></span> | <span data-ttu-id="b579b-133">Value</span><span class="sxs-lookup"><span data-stu-id="b579b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b579b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b579b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b579b-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b579b-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b579b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b579b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b579b-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b579b-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b579b-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b579b-138">End of client support</span></span><br/>    | <span data-ttu-id="b579b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b579b-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b579b-140">Producto</span><span class="sxs-lookup"><span data-stu-id="b579b-140">Product</span></span><br/>                  | <span data-ttu-id="b579b-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b579b-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b579b-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b579b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b579b-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b579b-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b579b-144">IID</span><span class="sxs-lookup"><span data-stu-id="b579b-144">IID</span></span><br/>                      | <span data-ttu-id="b579b-145">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="b579b-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b579b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b579b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b579b-147">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="b579b-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

