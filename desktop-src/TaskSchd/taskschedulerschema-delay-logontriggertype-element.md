---
title: Elemento Delay (logonTriggerType)
description: Cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Programador de tareas del elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492796"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="f6464-104">Elemento Delay (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="f6464-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="f6464-105">Cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="f6464-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="f6464-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="f6464-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f6464-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="f6464-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="f6464-108">El elemento **Delay** se define mediante el tipo complejo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f6464-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f6464-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f6464-109">Parent element</span></span>



| <span data-ttu-id="f6464-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6464-110">Element</span></span>                                                                       | <span data-ttu-id="f6464-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f6464-111">Derived from</span></span>                                                                 | <span data-ttu-id="f6464-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6464-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f6464-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="f6464-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="f6464-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="f6464-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="f6464-115">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="f6464-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f6464-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6464-116">Remarks</span></span>

<span data-ttu-id="f6464-117">Para el desarrollo de scripting, el retraso del desencadenador de inicio de sesión se especifica mediante la propiedad [**LogonTrigger. Delay**](logontrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="f6464-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="f6464-118">En el desarrollo de C++, el identificador de usuario para el desencadenador logon se especifica mediante la propiedad [**ILogonTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="f6464-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6464-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6464-119">Requirements</span></span>



| <span data-ttu-id="f6464-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6464-120">Requirement</span></span> | <span data-ttu-id="f6464-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6464-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6464-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6464-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6464-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6464-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6464-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6464-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6464-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6464-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6464-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6464-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6464-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="f6464-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f6464-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f6464-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





