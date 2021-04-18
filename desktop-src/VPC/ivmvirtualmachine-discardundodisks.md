---
title: Método IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces. h)
description: Descarta los discos para deshacer.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Método DiscardUndoDisks Virtual PC
- Método DiscardUndoDisks Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método DiscardUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490936"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="d1593-106">IVMVirtualMachine::D método iscardUndoDisks</span><span class="sxs-lookup"><span data-stu-id="d1593-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="d1593-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1593-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1593-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1593-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1593-109">Descarta los discos para deshacer.</span><span class="sxs-lookup"><span data-stu-id="d1593-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1593-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1593-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="d1593-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1593-111">Parameters</span></span>

<span data-ttu-id="d1593-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d1593-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1593-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1593-113">Return value</span></span>

<span data-ttu-id="d1593-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d1593-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d1593-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1593-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="d1593-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1593-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1593-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1593-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="d1593-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1593-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d1593-119"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1593-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="d1593-120">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d1593-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d1593-121"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="d1593-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="d1593-122">Los discos para deshacer virtuales no se pueden descartar mientras la máquina virtual está en ejecución o en un estado guardado.</span><span class="sxs-lookup"><span data-stu-id="d1593-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="d1593-123"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1593-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="d1593-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d1593-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="d1593-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1593-125">Requirements</span></span>



| <span data-ttu-id="d1593-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1593-126">Requirement</span></span> | <span data-ttu-id="d1593-127">Value</span><span class="sxs-lookup"><span data-stu-id="d1593-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1593-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1593-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d1593-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1593-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1593-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1593-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d1593-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1593-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1593-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d1593-132">End of client support</span></span><br/>    | <span data-ttu-id="d1593-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1593-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1593-134">Producto</span><span class="sxs-lookup"><span data-stu-id="d1593-134">Product</span></span><br/>                  | <span data-ttu-id="d1593-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1593-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1593-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1593-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1593-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1593-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1593-138">IID</span><span class="sxs-lookup"><span data-stu-id="d1593-138">IID</span></span><br/>                      | <span data-ttu-id="d1593-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d1593-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1593-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1593-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1593-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d1593-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

