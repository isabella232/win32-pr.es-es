---
title: Propiedad TaskSettings. AllowHardTerminate
description: Para scripting, obtiene o establece un valor booleano que indica que el servicio de Programador de tareas puede finalizar la tarea mediante TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Programador de tareas de la propiedad AllowHardTerminate
- Programador de tareas de la propiedad AllowHardTerminate, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802960"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="9aae8-106">Propiedad TaskSettings. AllowHardTerminate</span><span class="sxs-lookup"><span data-stu-id="9aae8-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="9aae8-107">Para scripting, obtiene o establece un valor booleano que indica que el servicio de Programador de tareas puede finalizar la tarea mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="9aae8-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="9aae8-108">El servicio intentará cerrar la tarea en ejecución mediante el envío de la notificación de [**\_ cierre de WM**](../winmsg/wm-close.md) y, si la tarea no responde, la tarea se terminará solo si esta propiedad está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="9aae8-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="9aae8-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9aae8-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aae8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aae8-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9aae8-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9aae8-111">Property value</span></span>

<span data-ttu-id="9aae8-112">Si es true, la tarea se puede finalizar mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="9aae8-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="9aae8-113">Si es false, la tarea no se puede finalizar mediante **TerminateProcess**.</span><span class="sxs-lookup"><span data-stu-id="9aae8-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aae8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aae8-114">Remarks</span></span>

<span data-ttu-id="9aae8-115">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9aae8-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aae8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aae8-116">Requirements</span></span>



| <span data-ttu-id="9aae8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aae8-117">Requirement</span></span> | <span data-ttu-id="9aae8-118">Value</span><span class="sxs-lookup"><span data-stu-id="9aae8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aae8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aae8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9aae8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9aae8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9aae8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aae8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9aae8-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9aae8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9aae8-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9aae8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9aae8-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9aae8-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aae8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aae8-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aae8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aae8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aae8-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9aae8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

