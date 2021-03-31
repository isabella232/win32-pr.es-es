---
title: Propiedad TaskSettings. WakeToRun
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llega el momento de ejecutar la tarea.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Programador de tareas de la propiedad WakeToRun
- Programador de tareas de la propiedad WakeToRun, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801753"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="7e7ea-106">Propiedad TaskSettings. WakeToRun</span><span class="sxs-lookup"><span data-stu-id="7e7ea-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="7e7ea-107">En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llega el momento de ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="7e7ea-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7ea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7ea-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7e7ea-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e7ea-110">Property value</span></span>

<span data-ttu-id="7e7ea-111">Si es true, la propiedad indica que el Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e7ea-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7ea-112">Remarks</span></span>

<span data-ttu-id="7e7ea-113">Cuando el servicio de Programador de tareas reactiva el equipo para ejecutar una tarea, es posible que la pantalla permanezca desactivada aunque el equipo ya no esté en modo de suspensión o hibernación.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="7e7ea-114">La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="7e7ea-115">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7ea-116">Requirements</span></span>



| <span data-ttu-id="7e7ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7ea-117">Requirement</span></span> | <span data-ttu-id="7e7ea-118">Value</span><span class="sxs-lookup"><span data-stu-id="7e7ea-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7ea-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7ea-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e7ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7e7ea-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7ea-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e7ea-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e7ea-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7e7ea-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e7ea-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7e7ea-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7e7ea-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e7ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e7ea-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7ea-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7ea-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7ea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7ea-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7e7ea-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





