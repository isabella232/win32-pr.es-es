---
title: Elemento RunOnlyIfIdle (settingsType)
description: Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Programador de tareas del elemento RunOnlyIfIdle
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079633"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="bbff6-104">Elemento RunOnlyIfIdle (settingsType)</span><span class="sxs-lookup"><span data-stu-id="bbff6-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="bbff6-105">Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="bbff6-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="bbff6-106">El elemento **RunOnlyIfIdle** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bbff6-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bbff6-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="bbff6-107">Parent element</span></span>



| <span data-ttu-id="bbff6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bbff6-108">Element</span></span>                                                           | <span data-ttu-id="bbff6-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bbff6-109">Derived from</span></span>                                                         | <span data-ttu-id="bbff6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbff6-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbff6-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="bbff6-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="bbff6-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="bbff6-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="bbff6-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="bbff6-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bbff6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbff6-114">Remarks</span></span>

<span data-ttu-id="bbff6-115">Para el desarrollo de C++, consulte la [**propiedad RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="bbff6-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="bbff6-116">Para el desarrollo de scripts, vea [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="bbff6-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbff6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbff6-117">Requirements</span></span>



| <span data-ttu-id="bbff6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbff6-118">Requirement</span></span> | <span data-ttu-id="bbff6-119">Value</span><span class="sxs-lookup"><span data-stu-id="bbff6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbff6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbff6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbff6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bbff6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbff6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbff6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbff6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbff6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbff6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbff6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbff6-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="bbff6-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bbff6-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="bbff6-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





