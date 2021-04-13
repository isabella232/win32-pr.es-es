---
title: Propiedad TaskSettings. Enabled
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propiedad Enabled Programador de tareas
- Propiedad Enabled Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422437"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="0efb5-107">Propiedad TaskSettings. Enabled</span><span class="sxs-lookup"><span data-stu-id="0efb5-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="0efb5-108">En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0efb5-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="0efb5-109">La tarea solo se puede realizar cuando este valor es true.</span><span class="sxs-lookup"><span data-stu-id="0efb5-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="0efb5-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0efb5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efb5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0efb5-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0efb5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0efb5-112">Property value</span></span>

<span data-ttu-id="0efb5-113">Si es true, la tarea está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0efb5-113">If True, the task is enabled.</span></span> <span data-ttu-id="0efb5-114">Si es false, la tarea no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0efb5-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efb5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0efb5-115">Remarks</span></span>

<span data-ttu-id="0efb5-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0efb5-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efb5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0efb5-117">Requirements</span></span>



| <span data-ttu-id="0efb5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0efb5-118">Requirement</span></span> | <span data-ttu-id="0efb5-119">Value</span><span class="sxs-lookup"><span data-stu-id="0efb5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0efb5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0efb5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0efb5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0efb5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0efb5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0efb5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0efb5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0efb5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0efb5-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0efb5-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="0efb5-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0efb5-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0efb5-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0efb5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0efb5-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0efb5-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0efb5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0efb5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efb5-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0efb5-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





