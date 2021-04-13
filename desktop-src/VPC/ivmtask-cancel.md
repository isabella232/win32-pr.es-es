---
title: Método CANCEL IVMTask (VPCCOMInterfaces. h)
description: Cancela la tarea.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Cancelar método virtual PC
- Método CANCEL Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, método CANCEL
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359845"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="98587-106">IVMTask:: CANCEL (método)</span><span class="sxs-lookup"><span data-stu-id="98587-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="98587-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="98587-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="98587-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="98587-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="98587-109">Cancela la tarea.</span><span class="sxs-lookup"><span data-stu-id="98587-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="98587-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98587-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="98587-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98587-111">Parameters</span></span>

<span data-ttu-id="98587-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="98587-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98587-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98587-113">Return value</span></span>

<span data-ttu-id="98587-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="98587-114">This method can return one of these values.</span></span>



| <span data-ttu-id="98587-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98587-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="98587-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="98587-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="98587-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="98587-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="98587-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="98587-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="98587-119"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="98587-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="98587-120">La tarea no se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="98587-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="98587-121"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="98587-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="98587-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="98587-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98587-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98587-123">Requirements</span></span>



| <span data-ttu-id="98587-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="98587-124">Requirement</span></span> | <span data-ttu-id="98587-125">Value</span><span class="sxs-lookup"><span data-stu-id="98587-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98587-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98587-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98587-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="98587-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98587-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98587-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98587-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="98587-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="98587-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="98587-130">End of client support</span></span><br/>    | <span data-ttu-id="98587-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98587-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="98587-132">Producto</span><span class="sxs-lookup"><span data-stu-id="98587-132">Product</span></span><br/>                  | <span data-ttu-id="98587-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="98587-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="98587-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98587-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="98587-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="98587-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="98587-136">IID</span><span class="sxs-lookup"><span data-stu-id="98587-136">IID</span></span><br/>                      | <span data-ttu-id="98587-137">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="98587-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="98587-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="98587-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98587-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="98587-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

