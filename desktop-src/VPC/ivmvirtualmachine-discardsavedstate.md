---
title: Método IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Descarta cualquier información de estado guardada para una máquina virtual guardada.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Método DiscardSavedState Virtual PC
- Método DiscardSavedState Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079501"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="9d65f-106">IVMVirtualMachine::D método iscardSavedState</span><span class="sxs-lookup"><span data-stu-id="9d65f-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="9d65f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d65f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9d65f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9d65f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9d65f-109">Descarta cualquier información de estado guardada para una máquina virtual guardada.</span><span class="sxs-lookup"><span data-stu-id="9d65f-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d65f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d65f-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="9d65f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d65f-111">Parameters</span></span>

<span data-ttu-id="9d65f-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9d65f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d65f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d65f-113">Return value</span></span>

<span data-ttu-id="9d65f-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9d65f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9d65f-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d65f-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="9d65f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d65f-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d65f-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="9d65f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d65f-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="9d65f-119"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="9d65f-120">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="9d65f-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="9d65f-121"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="9d65f-122">La máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9d65f-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="9d65f-123"><dt>**Máquina virtual \_ NO se ha \_ \_ guardado el \_ \_ Estado de la máquina virtual**</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="9d65f-124">La máquina virtual no se está ejecutando, pero no tiene ningún estado guardado.</span><span class="sxs-lookup"><span data-stu-id="9d65f-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="9d65f-125"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="9d65f-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9d65f-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="9d65f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d65f-127">Requirements</span></span>



| <span data-ttu-id="9d65f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d65f-128">Requirement</span></span> | <span data-ttu-id="9d65f-129">Value</span><span class="sxs-lookup"><span data-stu-id="9d65f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d65f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d65f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9d65f-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d65f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d65f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d65f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9d65f-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9d65f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9d65f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9d65f-134">End of client support</span></span><br/>    | <span data-ttu-id="9d65f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d65f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9d65f-136">Producto</span><span class="sxs-lookup"><span data-stu-id="9d65f-136">Product</span></span><br/>                  | <span data-ttu-id="9d65f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9d65f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9d65f-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d65f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d65f-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d65f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9d65f-140">IID</span><span class="sxs-lookup"><span data-stu-id="9d65f-140">IID</span></span><br/>                      | <span data-ttu-id="9d65f-141">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="9d65f-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9d65f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d65f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d65f-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="9d65f-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

