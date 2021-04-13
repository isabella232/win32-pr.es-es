---
title: Enumeración VMTaskResult (VPCCOMInterfaces. h)
description: Especifica el resultado de una tarea.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Enumeración de VMTaskResult Virtual PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535295"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="31f32-104">Enumeración VMTaskResult</span><span class="sxs-lookup"><span data-stu-id="31f32-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="31f32-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="31f32-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31f32-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="31f32-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31f32-107">Especifica el resultado de una tarea.</span><span class="sxs-lookup"><span data-stu-id="31f32-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f32-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31f32-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="31f32-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="31f32-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31f32-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="31f32-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-111">La tarea se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="31f32-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="31f32-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-113">Se canceló la tarea.</span><span class="sxs-lookup"><span data-stu-id="31f32-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**</span><span class="sxs-lookup"><span data-stu-id="31f32-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-115">La tarea tenía un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="31f32-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError en**</span><span class="sxs-lookup"><span data-stu-id="31f32-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-117">Memoria insuficiente para completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="31f32-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**</span><span class="sxs-lookup"><span data-stu-id="31f32-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-119">La tarea tenía un error al escribir en el disco (Asegúrese de que hay suficiente espacio en disco).</span><span class="sxs-lookup"><span data-stu-id="31f32-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**</span><span class="sxs-lookup"><span data-stu-id="31f32-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-121">No se pudo restaurar la máquina virtual porque el estado guardado era incompatible.</span><span class="sxs-lookup"><span data-stu-id="31f32-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult \_ TimeOutError**</span><span class="sxs-lookup"><span data-stu-id="31f32-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-123">Se agotó el tiempo de espera de la tarea.</span><span class="sxs-lookup"><span data-stu-id="31f32-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**</span><span class="sxs-lookup"><span data-stu-id="31f32-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-125">Se leyó un valor de preferencia no válido durante el procesamiento de la tarea.</span><span class="sxs-lookup"><span data-stu-id="31f32-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult \_ ThreadCrashError**</span><span class="sxs-lookup"><span data-stu-id="31f32-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-127">Un subproceso asociado a la tarea se bloqueó.</span><span class="sxs-lookup"><span data-stu-id="31f32-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**</span><span class="sxs-lookup"><span data-stu-id="31f32-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="31f32-129">Se anuló el cierre solicitado.</span><span class="sxs-lookup"><span data-stu-id="31f32-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31f32-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f32-130">Requirements</span></span>



| <span data-ttu-id="31f32-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f32-131">Requirement</span></span> | <span data-ttu-id="31f32-132">Value</span><span class="sxs-lookup"><span data-stu-id="31f32-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f32-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f32-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31f32-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="31f32-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31f32-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f32-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31f32-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="31f32-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31f32-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="31f32-137">End of client support</span></span><br/>    | <span data-ttu-id="31f32-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31f32-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31f32-139">Producto</span><span class="sxs-lookup"><span data-stu-id="31f32-139">Product</span></span><br/>                  | <span data-ttu-id="31f32-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31f32-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31f32-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31f32-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f32-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f32-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f32-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="31f32-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f32-144">**IVMTask:: result**</span><span class="sxs-lookup"><span data-stu-id="31f32-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

