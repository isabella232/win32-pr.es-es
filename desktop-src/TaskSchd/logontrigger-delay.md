---
title: LogonTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto LogonTrigger
- Programador de tareas de objeto LogonTrigger, propiedad Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422038"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="0e9a0-106">LogonTrigger. Delay (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0e9a0-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="0e9a0-107">En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="0e9a0-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9a0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e9a0-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="0e9a0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0e9a0-109">Property value</span></span>

<span data-ttu-id="0e9a0-110">Valor que indica la cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="0e9a0-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="0e9a0-111">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="0e9a0-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9a0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e9a0-112">Remarks</span></span>

<span data-ttu-id="0e9a0-113">Al leer o escribir XML para una tarea, el retraso del desencadenador de inicio de sesión se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0e9a0-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9a0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e9a0-114">Requirements</span></span>



| <span data-ttu-id="0e9a0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e9a0-115">Requirement</span></span> | <span data-ttu-id="0e9a0-116">Value</span><span class="sxs-lookup"><span data-stu-id="0e9a0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9a0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9a0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9a0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e9a0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9a0-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9a0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e9a0-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0e9a0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e9a0-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e9a0-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e9a0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e9a0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9a0-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e9a0-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9a0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9a0-126">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="0e9a0-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="0e9a0-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0e9a0-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





