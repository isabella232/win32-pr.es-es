---
title: Elemento WakeToRun (settingsType)
description: Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Programador de tareas del elemento WakeToRun
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686188"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="7fced-104">Elemento WakeToRun (settingsType)</span><span class="sxs-lookup"><span data-stu-id="7fced-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="7fced-105">Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7fced-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="7fced-106">El elemento **WakeToRun** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7fced-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7fced-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7fced-107">Parent element</span></span>



| <span data-ttu-id="7fced-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7fced-108">Element</span></span>                                                           | <span data-ttu-id="7fced-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7fced-109">Derived from</span></span>                                                         | <span data-ttu-id="7fced-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fced-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fced-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="7fced-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="7fced-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="7fced-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="7fced-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7fced-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7fced-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fced-114">Remarks</span></span>

<span data-ttu-id="7fced-115">Cuando el servicio de Programador de tareas reactiva el equipo para ejecutar una tarea, es posible que la pantalla permanezca desactivada aunque el equipo ya no esté en modo de suspensión o hibernación.</span><span class="sxs-lookup"><span data-stu-id="7fced-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="7fced-116">La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.</span><span class="sxs-lookup"><span data-stu-id="7fced-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="7fced-117">Para el desarrollo de C++, consulte la [**propiedad WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="7fced-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="7fced-118">Para el desarrollo de scripts, vea [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="7fced-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fced-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fced-119">Requirements</span></span>



| <span data-ttu-id="7fced-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fced-120">Requirement</span></span> | <span data-ttu-id="7fced-121">Value</span><span class="sxs-lookup"><span data-stu-id="7fced-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7fced-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fced-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fced-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fced-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7fced-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fced-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fced-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fced-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7fced-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fced-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fced-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="7fced-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7fced-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7fced-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





