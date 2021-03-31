---
title: Elemento volatile
description: Indica si la tarea se deshabilita automáticamente cada vez que se inicia Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Elemento volatile Programador de tareas
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803637"
---
# <a name="volatile-element"></a><span data-ttu-id="5a5de-104">Elemento volatile</span><span class="sxs-lookup"><span data-stu-id="5a5de-104">Volatile Element</span></span>

<span data-ttu-id="5a5de-105">Indica si la tarea se deshabilita automáticamente cada vez que se inicia Windows.</span><span class="sxs-lookup"><span data-stu-id="5a5de-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="5a5de-106">El elemento **volatile** se define mediante el tipo complejo [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5a5de-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5a5de-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5a5de-107">Parent element</span></span>



| <span data-ttu-id="5a5de-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a5de-108">Element</span></span>                                                           | <span data-ttu-id="5a5de-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5a5de-109">Derived from</span></span> | <span data-ttu-id="5a5de-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a5de-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a5de-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="5a5de-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="5a5de-112">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="5a5de-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a5de-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a5de-113">Remarks</span></span>

<span data-ttu-id="5a5de-114">En la programación de C++, esta configuración de inactividad se especifica mediante la propiedad [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .</span><span class="sxs-lookup"><span data-stu-id="5a5de-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a5de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a5de-115">Requirements</span></span>



| <span data-ttu-id="5a5de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a5de-116">Requirement</span></span> | <span data-ttu-id="5a5de-117">Value</span><span class="sxs-lookup"><span data-stu-id="5a5de-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a5de-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a5de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5de-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a5de-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="5a5de-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a5de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5de-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a5de-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a5de-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a5de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5de-123">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5a5de-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5a5de-124">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5a5de-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





