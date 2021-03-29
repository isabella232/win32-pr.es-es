---
title: Elemento ExecutionTimeLimit (settingsType)
description: Cantidad de tiempo permitido para completar la tarea.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Programador de tareas del elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905072"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="7a67d-104">Elemento ExecutionTimeLimit (settingsType)</span><span class="sxs-lookup"><span data-stu-id="7a67d-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="7a67d-105">Cantidad de tiempo permitido para completar la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="7a67d-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="7a67d-106">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="7a67d-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="7a67d-107">Un valor de PT0S permitirá que la tarea se ejecute indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="7a67d-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="7a67d-108">El elemento **ExecutionTimeLimit** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7a67d-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7a67d-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7a67d-109">Parent element</span></span>



| <span data-ttu-id="7a67d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a67d-110">Element</span></span>                                                           | <span data-ttu-id="7a67d-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7a67d-111">Derived from</span></span>                                                         | <span data-ttu-id="7a67d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a67d-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a67d-113">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="7a67d-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="7a67d-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="7a67d-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="7a67d-115">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7a67d-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7a67d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a67d-116">Remarks</span></span>

<span data-ttu-id="7a67d-117">Para el desarrollo de C++, consulte la [**propiedad ExecutionTimeLimit de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="7a67d-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="7a67d-118">Para el desarrollo de scripts, vea [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="7a67d-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a67d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a67d-119">Requirements</span></span>



| <span data-ttu-id="7a67d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a67d-120">Requirement</span></span> | <span data-ttu-id="7a67d-121">Value</span><span class="sxs-lookup"><span data-stu-id="7a67d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a67d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a67d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a67d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a67d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a67d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a67d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a67d-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a67d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a67d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a67d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a67d-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="7a67d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





