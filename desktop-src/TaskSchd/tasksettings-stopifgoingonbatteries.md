---
title: Propiedad TaskSettings. StopIfGoingOnBatteries
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Programador de tareas de la propiedad StopIfGoingOnBatteries
- Programador de tareas de la propiedad StopIfGoingOnBatteries, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492245"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="3ddc0-106">Propiedad TaskSettings. StopIfGoingOnBatteries</span><span class="sxs-lookup"><span data-stu-id="3ddc0-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="3ddc0-107">En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="3ddc0-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddc0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ddc0-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3ddc0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ddc0-110">Property value</span></span>

<span data-ttu-id="3ddc0-111">Un valor booleano que indica que la tarea se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3ddc0-112">Si es true, la propiedad indica que la tarea se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3ddc0-113">Si es false, la propiedad indica que la tarea no se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3ddc0-114">El valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-114">The default is True.</span></span> <span data-ttu-id="3ddc0-115">Vea la sección Comentarios para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddc0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ddc0-116">Remarks</span></span>

<span data-ttu-id="3ddc0-117">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="3ddc0-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddc0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ddc0-118">Requirements</span></span>



| <span data-ttu-id="3ddc0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ddc0-119">Requirement</span></span> | <span data-ttu-id="3ddc0-120">Value</span><span class="sxs-lookup"><span data-stu-id="3ddc0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddc0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ddc0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddc0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ddc0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ddc0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ddc0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddc0-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ddc0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ddc0-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ddc0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ddc0-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ddc0-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ddc0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ddc0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ddc0-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddc0-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddc0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ddc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddc0-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="3ddc0-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





