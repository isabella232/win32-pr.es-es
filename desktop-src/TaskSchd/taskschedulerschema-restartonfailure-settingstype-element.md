---
title: Elemento RestartOnFailure (settingsType)
description: Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Programador de tareas del elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274554"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="5f403-104">Elemento RestartOnFailure (settingsType)</span><span class="sxs-lookup"><span data-stu-id="5f403-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="5f403-105">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="5f403-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="5f403-106">El elemento **RestartOnFailure** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5f403-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5f403-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5f403-107">Parent element</span></span>



| <span data-ttu-id="5f403-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f403-108">Element</span></span>                                                           | <span data-ttu-id="5f403-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5f403-109">Derived from</span></span>                                                         | <span data-ttu-id="5f403-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f403-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f403-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="5f403-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5f403-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5f403-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5f403-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5f403-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5f403-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f403-114">Child elements</span></span>



| <span data-ttu-id="5f403-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f403-115">Element</span></span>                                                              | <span data-ttu-id="5f403-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f403-116">Type</span></span>         | <span data-ttu-id="5f403-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f403-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f403-118">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="5f403-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="5f403-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5f403-119">unsignedByte</span></span> | <span data-ttu-id="5f403-120">Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5f403-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="5f403-121">**Interval**</span><span class="sxs-lookup"><span data-stu-id="5f403-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="5f403-122">duration</span><span class="sxs-lookup"><span data-stu-id="5f403-122">duration</span></span>     | <span data-ttu-id="5f403-123">Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5f403-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="5f403-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f403-124">Remarks</span></span>

<span data-ttu-id="5f403-125">Cuando una aplicación especifica la configuración de la tarea, se obtiene acceso a esta información a través de las propiedades [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) y [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de la interfaz [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) .</span><span class="sxs-lookup"><span data-stu-id="5f403-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="5f403-126">En el caso de scripting, se obtiene acceso a esta información a través de las propiedades [**TaskSettings. RestartCount**](tasksettings-restartcount.md) y [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="5f403-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="5f403-127">Ambos elementos secundarios se deben establecer para especificar cómo el Programador de tareas reinicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="5f403-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f403-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f403-128">Requirements</span></span>



| <span data-ttu-id="5f403-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f403-129">Requirement</span></span> | <span data-ttu-id="5f403-130">Value</span><span class="sxs-lookup"><span data-stu-id="5f403-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f403-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f403-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5f403-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f403-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f403-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f403-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5f403-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f403-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f403-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f403-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f403-136">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5f403-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





