---
title: Propiedad TaskSettings. DisallowStartIfOnBatteries
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Programador de tareas de la propiedad DisallowStartIfOnBatteries
- Programador de tareas de la propiedad DisallowStartIfOnBatteries, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150841"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="219f3-106">Propiedad TaskSettings. DisallowStartIfOnBatteries</span><span class="sxs-lookup"><span data-stu-id="219f3-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="219f3-107">En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="219f3-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="219f3-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="219f3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="219f3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="219f3-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="219f3-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="219f3-110">Property value</span></span>

<span data-ttu-id="219f3-111">Un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="219f3-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="219f3-112">Si es true, la tarea no se iniciará si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="219f3-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="219f3-113">Si es false, la tarea se iniciará si el equipo se ejecuta con baterías.</span><span class="sxs-lookup"><span data-stu-id="219f3-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="219f3-114">El valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="219f3-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="219f3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="219f3-115">Remarks</span></span>

<span data-ttu-id="219f3-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="219f3-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="219f3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="219f3-117">Requirements</span></span>



| <span data-ttu-id="219f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="219f3-118">Requirement</span></span> | <span data-ttu-id="219f3-119">Value</span><span class="sxs-lookup"><span data-stu-id="219f3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="219f3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="219f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="219f3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="219f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="219f3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="219f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="219f3-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="219f3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="219f3-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="219f3-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="219f3-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="219f3-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="219f3-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="219f3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="219f3-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="219f3-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="219f3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="219f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219f3-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="219f3-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





