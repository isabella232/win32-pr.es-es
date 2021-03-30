---
title: Trigger. StartBoundary (propiedad)
description: En el caso de scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Programador de tareas de la propiedad StartBoundary
- Propiedad StartBoundary Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador, propiedad StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801747"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="45db4-106">Trigger. StartBoundary (propiedad)</span><span class="sxs-lookup"><span data-stu-id="45db4-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="45db4-107">En el caso de scripting, obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="45db4-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="45db4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45db4-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="45db4-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="45db4-109">Property value</span></span>

<span data-ttu-id="45db4-110">Fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="45db4-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="45db4-111">La fecha y la hora deben tener el formato siguiente: AAAA-MM-DDTHH: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="45db4-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="45db4-112">Por ejemplo, la fecha 11 de octubre de 2005 a 1:21:17 en la zona horaria del Pacífico se escribiría como 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="45db4-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="45db4-113">La sección (+-) HH: MM del formato describe la zona horaria como un número determinado de horas de antemano o detrás de la hora universal coordinada (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="45db4-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="45db4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45db4-114">Remarks</span></span>

<span data-ttu-id="45db4-115">Al leer o escribir XML para una tarea, el límite de inicio del desencadenador se especifica en el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="45db4-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="45db4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45db4-116">Requirements</span></span>



| <span data-ttu-id="45db4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="45db4-117">Requirement</span></span> | <span data-ttu-id="45db4-118">Value</span><span class="sxs-lookup"><span data-stu-id="45db4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45db4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45db4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45db4-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45db4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="45db4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45db4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45db4-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45db4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45db4-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="45db4-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="45db4-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="45db4-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="45db4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45db4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45db4-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45db4-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45db4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="45db4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45db4-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="45db4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





