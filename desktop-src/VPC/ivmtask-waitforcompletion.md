---
title: Método IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Método WaitForCompletion Virtual PC
- Método WaitForCompletion Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, método WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695988"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="ba222-106">IVMTask:: WaitForCompletion (método)</span><span class="sxs-lookup"><span data-stu-id="ba222-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="ba222-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ba222-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba222-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba222-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba222-109">Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="ba222-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba222-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba222-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="ba222-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba222-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba222-112">*tiempo de espera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba222-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba222-113">Tiempo, en milisegundos, que este método esperará a la finalización de la tarea antes de devolver el control al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ba222-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="ba222-114">Un valor de-1 especifica que el método esperará hasta que se complete la tarea sin que se agote el tiempo de espera. Otros valores de tiempo de espera válidos oscilan entre 0 y 4 millones milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ba222-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba222-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba222-115">Return value</span></span>

<span data-ttu-id="ba222-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ba222-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ba222-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba222-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ba222-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba222-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ba222-119"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ba222-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ba222-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba222-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="ba222-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ba222-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="ba222-122">El parámetro *timeout* no es válido.</span><span class="sxs-lookup"><span data-stu-id="ba222-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ba222-123"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ba222-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ba222-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ba222-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ba222-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba222-125">Remarks</span></span>

<span data-ttu-id="ba222-126">El método **WaitForCompletion** coloca el subproceso de ejecución actual en modo de suspensión hasta que lo devuelve.</span><span class="sxs-lookup"><span data-stu-id="ba222-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="ba222-127">No se recomienda especificar una espera infinita (timeout =-1) a menos que sea absolutamente crítico que la tarea se complete en cualquier circunstancia.</span><span class="sxs-lookup"><span data-stu-id="ba222-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba222-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba222-128">Requirements</span></span>



| <span data-ttu-id="ba222-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba222-129">Requirement</span></span> | <span data-ttu-id="ba222-130">Value</span><span class="sxs-lookup"><span data-stu-id="ba222-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba222-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba222-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ba222-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba222-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba222-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba222-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ba222-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ba222-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba222-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ba222-135">End of client support</span></span><br/>    | <span data-ttu-id="ba222-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba222-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba222-137">Producto</span><span class="sxs-lookup"><span data-stu-id="ba222-137">Product</span></span><br/>                  | <span data-ttu-id="ba222-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba222-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba222-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba222-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba222-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba222-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ba222-141">IID</span><span class="sxs-lookup"><span data-stu-id="ba222-141">IID</span></span><br/>                      | <span data-ttu-id="ba222-142">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="ba222-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="ba222-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba222-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba222-144">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="ba222-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

