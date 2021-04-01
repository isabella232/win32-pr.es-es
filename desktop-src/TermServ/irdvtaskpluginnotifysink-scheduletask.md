---
title: IRDVTaskPluginNotifySink ScheduleTask (método)
description: Llamado por el agente de tareas para programar una tarea.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask (método) Servicios de Escritorio remoto
- Método ScheduleTask Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- IRDVTaskPluginNotifySink interface Servicios de Escritorio remoto, ScheduleTask (método)
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905597"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="f934f-106">IRDVTaskPluginNotifySink:: ScheduleTask (método)</span><span class="sxs-lookup"><span data-stu-id="f934f-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="f934f-107">Llamado por el agente de tareas para programar una tarea.</span><span class="sxs-lookup"><span data-stu-id="f934f-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="f934f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f934f-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="f934f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f934f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f934f-110">*ftStartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-111">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="f934f-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="f934f-112">La hora de inicio de la tarea más temprana, en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="f934f-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="f934f-113">*ftEndTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-114">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="f934f-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="f934f-115">Hora de finalización de la tarea, en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="f934f-115">The task end time, in UTC.</span></span> <span data-ttu-id="f934f-116">Pasar un valor de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a ceros si no se especifica ninguna hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="f934f-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f934f-117">*ftDeadline* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-118">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="f934f-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="f934f-119">Fecha límite de la tarea, en UTC.</span><span class="sxs-lookup"><span data-stu-id="f934f-119">The task deadline, in UTC.</span></span> <span data-ttu-id="f934f-120">Se usa para establecer la prioridad de varias tareas que se encuentran dentro de su ventana de inicio.</span><span class="sxs-lookup"><span data-stu-id="f934f-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="f934f-121">Si se debe iniciar más de una tarea, primero se iniciará la que tenga la fecha límite más temprana.</span><span class="sxs-lookup"><span data-stu-id="f934f-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="f934f-122">*bstrLabel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f934f-123">Type: **BSTR**</span></span>

<span data-ttu-id="f934f-124">Etiqueta de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f934f-124">The label for the task.</span></span> <span data-ttu-id="f934f-125">Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="f934f-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f934f-126">*bstrIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f934f-127">Type: **BSTR**</span></span>

<span data-ttu-id="f934f-128">Identificador único de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f934f-128">The identifier of the task.</span></span> <span data-ttu-id="f934f-129">Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="f934f-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f934f-130">*saContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f934f-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f934f-131">Tipo: **SAFEARRAY (byte)**</span><span class="sxs-lookup"><span data-stu-id="f934f-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="f934f-132">Datos opcionales para la tarea.</span><span class="sxs-lookup"><span data-stu-id="f934f-132">Optional data for the task.</span></span> <span data-ttu-id="f934f-133">Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="f934f-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f934f-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f934f-134">Return value</span></span>

<span data-ttu-id="f934f-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f934f-135">Type: **HRESULT**</span></span>

<span data-ttu-id="f934f-136">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f934f-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f934f-137">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f934f-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f934f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f934f-138">Requirements</span></span>



| <span data-ttu-id="f934f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f934f-139">Requirement</span></span> | <span data-ttu-id="f934f-140">Value</span><span class="sxs-lookup"><span data-stu-id="f934f-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="f934f-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f934f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f934f-142">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="f934f-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="f934f-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f934f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f934f-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f934f-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f934f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f934f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f934f-146">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="f934f-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

