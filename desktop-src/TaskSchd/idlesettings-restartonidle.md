---
title: Propiedad IdleSettings. RestartOnIdle
description: En el caso de scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Programador de tareas de la propiedad RestartOnIdle
- Programador de tareas de la propiedad RestartOnIdle, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686000"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="79e5b-106">Propiedad IdleSettings. RestartOnIdle</span><span class="sxs-lookup"><span data-stu-id="79e5b-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="79e5b-107">En el caso de scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.</span><span class="sxs-lookup"><span data-stu-id="79e5b-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79e5b-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="79e5b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="79e5b-109">Property value</span></span>

<span data-ttu-id="79e5b-110">Un valor booleano que indica si la tarea debe reiniciarse cuando el equipo se recorre en una condición de inactividad más de una vez.</span><span class="sxs-lookup"><span data-stu-id="79e5b-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="79e5b-111">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="79e5b-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e5b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79e5b-112">Remarks</span></span>

<span data-ttu-id="79e5b-113">Esta propiedad solo se usa si la propiedad [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="79e5b-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="79e5b-114">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="79e5b-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e5b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e5b-115">Requirements</span></span>



| <span data-ttu-id="79e5b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e5b-116">Requirement</span></span> | <span data-ttu-id="79e5b-117">Value</span><span class="sxs-lookup"><span data-stu-id="79e5b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e5b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79e5b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79e5b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79e5b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79e5b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79e5b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79e5b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79e5b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79e5b-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79e5b-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="79e5b-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79e5b-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79e5b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79e5b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e5b-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e5b-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e5b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="79e5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e5b-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="79e5b-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="79e5b-128">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="79e5b-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





