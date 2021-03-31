---
title: TaskService. GetRunningTasks, método
description: En el caso de scripting, obtiene una colección de tareas en ejecución.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Método GetRunningTasks Programador de tareas
- Método GetRunningTasks Programador de tareas, objeto TaskService
- Programador de tareas de objeto TaskService, método GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803955"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="54584-106">TaskService. GetRunningTasks, método</span><span class="sxs-lookup"><span data-stu-id="54584-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="54584-107">En el caso de scripting, obtiene una colección de tareas en ejecución.</span><span class="sxs-lookup"><span data-stu-id="54584-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="54584-108">**TaskService. GetRunningTasks** solo devolverá una colección de tareas en ejecución que se ejecutan en el contexto de seguridad de un usuario o debajo de él.</span><span class="sxs-lookup"><span data-stu-id="54584-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="54584-109">Por ejemplo, para los miembros del grupo administradores, **GetRunningTasks** devolverá una colección de todas las tareas en ejecución, pero para los miembros del grupo usuarios, **GetRunningTasks** solo devolverá una colección de tareas que se ejecutan en el contexto de seguridad del grupo usuarios.</span><span class="sxs-lookup"><span data-stu-id="54584-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="54584-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54584-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="54584-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54584-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54584-112">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="54584-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54584-113">Pase 1 para devolver todas las tareas en ejecución, incluidas las tareas ocultas.</span><span class="sxs-lookup"><span data-stu-id="54584-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="54584-114">Pase 0 para devolver una colección de tareas en ejecución que no son tareas ocultas.</span><span class="sxs-lookup"><span data-stu-id="54584-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54584-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54584-115">Return value</span></span>

<span data-ttu-id="54584-116">Objeto [**RunningTaskCollection**](runningtaskcollection.md) que contiene las tareas que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="54584-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="54584-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54584-117">Requirements</span></span>



| <span data-ttu-id="54584-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54584-118">Requirement</span></span> | <span data-ttu-id="54584-119">Value</span><span class="sxs-lookup"><span data-stu-id="54584-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54584-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54584-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54584-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54584-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54584-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54584-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54584-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="54584-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54584-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="54584-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="54584-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54584-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54584-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54584-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54584-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54584-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54584-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="54584-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54584-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="54584-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





