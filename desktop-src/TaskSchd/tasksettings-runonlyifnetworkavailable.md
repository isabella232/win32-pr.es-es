---
title: Propiedad TaskSettings. RunOnlyIfNetworkAvailable
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Programador de tareas de la propiedad RunOnlyIfNetworkAvailable
- Programador de tareas de la propiedad RunOnlyIfNetworkAvailable, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905488"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="91448-106">Propiedad TaskSettings. RunOnlyIfNetworkAvailable</span><span class="sxs-lookup"><span data-stu-id="91448-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="91448-107">En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.</span><span class="sxs-lookup"><span data-stu-id="91448-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="91448-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="91448-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="91448-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91448-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="91448-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="91448-110">Property value</span></span>

<span data-ttu-id="91448-111">Si es true, la propiedad indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.</span><span class="sxs-lookup"><span data-stu-id="91448-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="91448-112">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="91448-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="91448-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91448-113">Remarks</span></span>

<span data-ttu-id="91448-114">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="91448-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="91448-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91448-115">Requirements</span></span>



| <span data-ttu-id="91448-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91448-116">Requirement</span></span> | <span data-ttu-id="91448-117">Value</span><span class="sxs-lookup"><span data-stu-id="91448-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91448-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91448-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91448-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91448-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="91448-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91448-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91448-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91448-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91448-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="91448-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="91448-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91448-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91448-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91448-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91448-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91448-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91448-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="91448-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91448-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="91448-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





