---
title: Propiedad TaskSettings. AllowDemandStart
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Programador de tareas de la propiedad AllowDemandStart
- Programador de tareas de la propiedad AllowDemandStart, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422029"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="b4fd6-106">Propiedad TaskSettings. AllowDemandStart</span><span class="sxs-lookup"><span data-stu-id="b4fd6-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="b4fd6-107">En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="b4fd6-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fd6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4fd6-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b4fd6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4fd6-110">Property value</span></span>

<span data-ttu-id="b4fd6-111">Si es true, la tarea se puede ejecutar con el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="b4fd6-112">Si es false, la tarea no se puede ejecutar con el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="b4fd6-113">El valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4fd6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4fd6-114">Remarks</span></span>

<span data-ttu-id="b4fd6-115">Cuando esta propiedad se establece en true, la tarea puede iniciarse de forma independiente cuando algún desencadenador inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="b4fd6-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="b4fd6-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4fd6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4fd6-117">Requirements</span></span>



| <span data-ttu-id="b4fd6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4fd6-118">Requirement</span></span> | <span data-ttu-id="b4fd6-119">Value</span><span class="sxs-lookup"><span data-stu-id="b4fd6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fd6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4fd6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fd6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4fd6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b4fd6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4fd6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fd6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4fd6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4fd6-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4fd6-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4fd6-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4fd6-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4fd6-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4fd6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fd6-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4fd6-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4fd6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4fd6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fd6-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b4fd6-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





