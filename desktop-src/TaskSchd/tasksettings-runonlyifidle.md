---
title: Propiedad TaskSettings. RunOnlyIfIdle
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Programador de tareas de la propiedad RunOnlyIfIdle
- Programador de tareas de la propiedad RunOnlyIfIdle, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422155"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="82363-106">Propiedad TaskSettings. RunOnlyIfIdle</span><span class="sxs-lookup"><span data-stu-id="82363-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="82363-107">En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="82363-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="82363-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82363-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82363-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82363-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="82363-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="82363-110">Property value</span></span>

<span data-ttu-id="82363-111">Si es true, la propiedad indica que el Programador de tareas ejecutará la tarea solo si el equipo está en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="82363-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="82363-112">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="82363-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="82363-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82363-113">Remarks</span></span>

<span data-ttu-id="82363-114">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="82363-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="82363-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82363-115">Requirements</span></span>



| <span data-ttu-id="82363-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="82363-116">Requirement</span></span> | <span data-ttu-id="82363-117">Value</span><span class="sxs-lookup"><span data-stu-id="82363-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82363-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82363-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82363-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82363-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82363-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82363-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82363-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82363-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82363-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="82363-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="82363-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82363-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82363-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82363-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82363-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82363-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82363-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="82363-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82363-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="82363-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





