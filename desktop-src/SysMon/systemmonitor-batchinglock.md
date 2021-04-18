---
title: SystemMonitor.Batmétodo chingLock
description: Bloquea el monitor de sistema para impedir que muestre los datos de contador del contador o el archivo de registro recién agregados.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Método BatchingLock SysMon
- Método BatchingLock SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666021"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="79124-106">SystemMonitor.Batmétodo chingLock</span><span class="sxs-lookup"><span data-stu-id="79124-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="79124-107">Bloquea el monitor de sistema para impedir que muestre los datos de contador del contador o el archivo de registro recién agregados.</span><span class="sxs-lookup"><span data-stu-id="79124-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="79124-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79124-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="79124-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79124-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79124-110">*bloquear* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79124-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79124-111">Establézcalo en true para bloquear el monitor de sistema y evitar que muestre los datos de contador del contador o el archivo de registro recién agregados.</span><span class="sxs-lookup"><span data-stu-id="79124-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="79124-112">Establézcalo en false para quitar el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="79124-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="79124-113">*batchReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79124-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79124-114">Identifica el origen de los datos que está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="79124-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="79124-115">Use el mismo valor de razón al bloquear y desbloquear el recurso.</span><span class="sxs-lookup"><span data-stu-id="79124-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="79124-116">Para ver los valores posibles, consulte la enumeración [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .</span><span class="sxs-lookup"><span data-stu-id="79124-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79124-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79124-117">Return value</span></span>

<span data-ttu-id="79124-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="79124-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79124-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79124-119">Remarks</span></span>

<span data-ttu-id="79124-120">Debe llamar a este método dos veces, una vez para bloquear el origen (true) y otra para desbloquear el origen (false).</span><span class="sxs-lookup"><span data-stu-id="79124-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="79124-121">Solo puede colocar un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="79124-121">You can place only one lock.</span></span> <span data-ttu-id="79124-122">Por ejemplo, si establece el bloqueo de SysmonBatchAddFiles y, a continuación, realiza una segunda llamada con SysmonBatchAddCounters como motivo, la segunda llamada quita el bloqueo colocado por la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="79124-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="79124-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79124-123">Requirements</span></span>



| <span data-ttu-id="79124-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79124-124">Requirement</span></span> | <span data-ttu-id="79124-125">Value</span><span class="sxs-lookup"><span data-stu-id="79124-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79124-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79124-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79124-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79124-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79124-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79124-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79124-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79124-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79124-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79124-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79124-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="79124-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79124-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="79124-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79124-133">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="79124-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





