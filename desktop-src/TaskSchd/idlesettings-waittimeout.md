---
title: Propiedad IdleSettings. WaitTimeout
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Programador de tareas de la propiedad WaitTimeout
- Programador de tareas de la propiedad WaitTimeout, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079474"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="c2303-106">Propiedad IdleSettings. WaitTimeout</span><span class="sxs-lookup"><span data-stu-id="c2303-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="c2303-107">En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2303-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="c2303-108">Si no se especifica ningún valor para esta propiedad, el servicio Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2303-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2303-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2303-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="c2303-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c2303-110">Property value</span></span>

<span data-ttu-id="c2303-111">Valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2303-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="c2303-112">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="c2303-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c2303-113">El tiempo mínimo permitido es 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="c2303-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="c2303-114">Si este valor es **null**, el retraso se establecerá en el valor predeterminado de 1 hora.</span><span class="sxs-lookup"><span data-stu-id="c2303-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2303-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2303-115">Remarks</span></span>

<span data-ttu-id="c2303-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="c2303-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c2303-117">Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad **IdleSettings. WaitTimeout** .</span><span class="sxs-lookup"><span data-stu-id="c2303-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2303-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2303-118">Requirements</span></span>



| <span data-ttu-id="c2303-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2303-119">Requirement</span></span> | <span data-ttu-id="c2303-120">Value</span><span class="sxs-lookup"><span data-stu-id="c2303-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2303-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2303-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2303-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2303-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c2303-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2303-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2303-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2303-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2303-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c2303-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2303-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2303-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2303-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2303-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2303-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2303-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2303-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2303-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2303-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c2303-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c2303-131">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="c2303-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





