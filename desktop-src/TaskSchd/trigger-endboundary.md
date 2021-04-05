---
title: Trigger. EndBoundary (propiedad)
description: En el caso de scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Programador de tareas de la propiedad EndBoundary
- Propiedad EndBoundary Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador, propiedad EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079154"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="ffac0-107">Trigger. EndBoundary (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ffac0-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="ffac0-108">En el caso de scripting, obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="ffac0-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="ffac0-109">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="ffac0-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffac0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffac0-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="ffac0-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffac0-111">Property value</span></span>

<span data-ttu-id="ffac0-112">Fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="ffac0-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="ffac0-113">La fecha y la hora deben tener el formato siguiente: AAAA-MM-DDTHH: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="ffac0-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="ffac0-114">Por ejemplo, la fecha 11 de octubre de 2005 a 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="ffac0-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="ffac0-115">La sección (+-) HH: MM del formato describe la zona horaria como un número determinado de horas de antemano o detrás de la hora universal coordinada (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="ffac0-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffac0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffac0-116">Remarks</span></span>

<span data-ttu-id="ffac0-117">Al leer o escribir XML para una tarea, se especifica la propiedad Enabled mediante el elemento [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ffac0-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffac0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffac0-118">Requirements</span></span>



| <span data-ttu-id="ffac0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffac0-119">Requirement</span></span> | <span data-ttu-id="ffac0-120">Value</span><span class="sxs-lookup"><span data-stu-id="ffac0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffac0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffac0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ffac0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ffac0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ffac0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffac0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ffac0-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffac0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ffac0-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ffac0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffac0-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ffac0-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ffac0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffac0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffac0-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffac0-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffac0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffac0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffac0-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ffac0-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





