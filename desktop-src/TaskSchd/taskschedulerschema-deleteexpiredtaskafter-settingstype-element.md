---
title: Elemento DeleteExpiredTaskAfter (settingsType)
description: Especifica la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Programador de tareas del elemento DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685944"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="c4245-104">Elemento DeleteExpiredTaskAfter (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c4245-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="c4245-105">Especifica la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.</span><span class="sxs-lookup"><span data-stu-id="c4245-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="c4245-106">Si no se especifica ningún valor para este elemento, el servicio Programador de tareas no eliminará la tarea.</span><span class="sxs-lookup"><span data-stu-id="c4245-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="c4245-107">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="c4245-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c4245-108">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="c4245-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="c4245-109">El elemento **DeleteExpiredTaskAfter** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c4245-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c4245-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c4245-110">Parent element</span></span>



| <span data-ttu-id="c4245-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4245-111">Element</span></span>                                                           | <span data-ttu-id="c4245-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c4245-112">Derived from</span></span>                                                         | <span data-ttu-id="c4245-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4245-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4245-114">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="c4245-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c4245-115">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c4245-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c4245-116">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="c4245-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c4245-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4245-117">Remarks</span></span>

<span data-ttu-id="c4245-118">Para el desarrollo de C++, consulte la [**propiedad DeleteExpiredTaskAfter de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="c4245-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="c4245-119">Para el desarrollo de scripts, vea [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="c4245-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c4245-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c4245-120">Examples</span></span>

<span data-ttu-id="c4245-121">En el código XML siguiente se define un elemento de configuración que elimina una tarea expirada después de una semana.</span><span class="sxs-lookup"><span data-stu-id="c4245-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="c4245-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4245-122">Requirements</span></span>



| <span data-ttu-id="c4245-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4245-123">Requirement</span></span> | <span data-ttu-id="c4245-124">Value</span><span class="sxs-lookup"><span data-stu-id="c4245-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4245-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4245-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c4245-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c4245-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4245-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4245-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c4245-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4245-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4245-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4245-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4245-130">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c4245-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





