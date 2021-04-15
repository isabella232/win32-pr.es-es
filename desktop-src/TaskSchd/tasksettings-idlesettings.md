---
title: Propiedad TaskSettings. IdleSettings
description: En el caso de scripting, obtiene o establece la información que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Programador de tareas de la propiedad IdleSettings
- Programador de tareas de la propiedad IdleSettings, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676849"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="373aa-106">Propiedad TaskSettings. IdleSettings</span><span class="sxs-lookup"><span data-stu-id="373aa-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="373aa-107">En el caso de scripting, obtiene o establece la información que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="373aa-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="373aa-108">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="373aa-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="373aa-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="373aa-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="373aa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="373aa-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="373aa-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="373aa-111">Property value</span></span>

<span data-ttu-id="373aa-112">Objeto [**IdleSettings**](idlesettings.md) que especifica cómo el programador de tareas controla la tarea cuando el equipo entra en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="373aa-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="373aa-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="373aa-113">Remarks</span></span>

<span data-ttu-id="373aa-114">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="373aa-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="373aa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="373aa-115">Requirements</span></span>



| <span data-ttu-id="373aa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="373aa-116">Requirement</span></span> | <span data-ttu-id="373aa-117">Value</span><span class="sxs-lookup"><span data-stu-id="373aa-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="373aa-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="373aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="373aa-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="373aa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="373aa-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="373aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="373aa-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="373aa-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="373aa-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="373aa-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="373aa-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="373aa-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="373aa-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="373aa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="373aa-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="373aa-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373aa-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="373aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373aa-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="373aa-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





