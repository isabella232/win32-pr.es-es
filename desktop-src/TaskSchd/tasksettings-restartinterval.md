---
title: Propiedad TaskSettings.RestartInterval
description: Para el scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Propiedad RestartInterval Programador de tareas
- Propiedad RestartInterval Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734150"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="5854d-106">Propiedad TaskSettings.RestartInterval</span><span class="sxs-lookup"><span data-stu-id="5854d-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="5854d-107">Para el scripting, obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5854d-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="5854d-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5854d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5854d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5854d-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="5854d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5854d-110">Property value</span></span>

<span data-ttu-id="5854d-111">Valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5854d-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="5854d-112">Si se establece esta propiedad, también se debe establecer la propiedad [**RestartCount.**](tasksettings-restartcount.md)</span><span class="sxs-lookup"><span data-stu-id="5854d-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="5854d-113">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="5854d-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="5854d-114">El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="5854d-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="5854d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5854d-115">Remarks</span></span>

<span data-ttu-id="5854d-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento Interval**](taskschedulerschema-interval-restarttype-element.md) del Programador de tareas esquema.</span><span class="sxs-lookup"><span data-stu-id="5854d-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5854d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5854d-117">Requirements</span></span>



| <span data-ttu-id="5854d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5854d-118">Requirement</span></span> | <span data-ttu-id="5854d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5854d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5854d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5854d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5854d-121">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="5854d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5854d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5854d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5854d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5854d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5854d-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5854d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5854d-125"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5854d-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5854d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5854d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5854d-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5854d-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5854d-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5854d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5854d-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5854d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





