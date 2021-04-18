---
title: Propiedad TaskSettings. RestartCount
description: En el caso de scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Programador de tareas de la propiedad RestartCount
- Programador de tareas de la propiedad RestartCount, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422156"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="09fc0-106">Propiedad TaskSettings. RestartCount</span><span class="sxs-lookup"><span data-stu-id="09fc0-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="09fc0-107">En el caso de scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="09fc0-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="09fc0-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="09fc0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fc0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09fc0-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="09fc0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="09fc0-110">Property value</span></span>

<span data-ttu-id="09fc0-111">Número de veces que el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="09fc0-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="09fc0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09fc0-112">Remarks</span></span>

<span data-ttu-id="09fc0-113">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Count**](taskschedulerschema-count-restarttype-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="09fc0-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fc0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fc0-114">Requirements</span></span>



| <span data-ttu-id="09fc0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fc0-115">Requirement</span></span> | <span data-ttu-id="09fc0-116">Value</span><span class="sxs-lookup"><span data-stu-id="09fc0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09fc0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09fc0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09fc0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09fc0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="09fc0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09fc0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09fc0-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="09fc0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09fc0-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="09fc0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="09fc0-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="09fc0-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="09fc0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09fc0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09fc0-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09fc0-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fc0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="09fc0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fc0-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="09fc0-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





