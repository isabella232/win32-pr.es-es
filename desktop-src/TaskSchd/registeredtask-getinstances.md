---
title: RegisteredTask. GetInstances, método
description: En el caso de scripting, devuelve todas las instancias de la tarea registrada actualmente en ejecución.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Programador de tareas
- Método GetInstances Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150807"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="22e45-106">RegisteredTask. GetInstances, método</span><span class="sxs-lookup"><span data-stu-id="22e45-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="22e45-107">En el caso de scripting, devuelve todas las instancias de la tarea registrada actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="22e45-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="22e45-108">**RegisteredTask. GetInstances** solo devolverá las instancias de la tarea registrada actualmente en ejecución que se ejecutan en el contexto de seguridad de un usuario o debajo de él.</span><span class="sxs-lookup"><span data-stu-id="22e45-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="22e45-109">Por ejemplo, para los miembros del grupo administradores, **GetInstances** devolverá todas las instancias de la tarea registrada actualmente en ejecución, pero para los miembros del grupo usuarios, **GetInstances** solo devolverá las instancias de la tarea registrada actualmente en ejecución que se ejecutan en el contexto de seguridad del grupo usuarios.</span><span class="sxs-lookup"><span data-stu-id="22e45-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="22e45-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22e45-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="22e45-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22e45-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e45-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="22e45-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="22e45-113">Este parámetro se reserva para uso futuro y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="22e45-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22e45-114">*runningTasks* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22e45-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22e45-115">Un objeto [**RunningTaskCollection**](runningtaskcollection.md) que contiene todas las instancias de la tarea que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="22e45-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e45-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22e45-116">Return value</span></span>

<span data-ttu-id="22e45-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="22e45-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e45-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e45-118">Requirements</span></span>



| <span data-ttu-id="22e45-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e45-119">Requirement</span></span> | <span data-ttu-id="22e45-120">Value</span><span class="sxs-lookup"><span data-stu-id="22e45-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22e45-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22e45-121">Minimum supported client</span></span><br/> | <span data-ttu-id="22e45-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22e45-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="22e45-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22e45-123">Minimum supported server</span></span><br/> | <span data-ttu-id="22e45-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="22e45-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22e45-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="22e45-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="22e45-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22e45-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22e45-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22e45-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22e45-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e45-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e45-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="22e45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e45-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="22e45-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="22e45-131">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="22e45-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





