---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Programador de tareas del elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676827"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="cc7b2-104">Elemento MultipleInstancesPolicy (settingsType)</span><span class="sxs-lookup"><span data-stu-id="cc7b2-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="cc7b2-105">Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="cc7b2-106">El elemento **MultipleInstancesPolicy** se define mediante el tipo simple [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7b2-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cc7b2-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cc7b2-107">Parent element</span></span>



| <span data-ttu-id="cc7b2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc7b2-108">Element</span></span>                                                           | <span data-ttu-id="cc7b2-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="cc7b2-109">Derived from</span></span>                                                         | <span data-ttu-id="cc7b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc7b2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc7b2-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="cc7b2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="cc7b2-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="cc7b2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="cc7b2-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cc7b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc7b2-114">Remarks</span></span>

<span data-ttu-id="cc7b2-115">Para el desarrollo de C++, consulte la [**propiedad MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="cc7b2-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="cc7b2-116">Para el desarrollo de scripts, vea [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="cc7b2-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="cc7b2-117">Valores restringidos</span><span class="sxs-lookup"><span data-stu-id="cc7b2-117">Restricted Values</span></span>

<span data-ttu-id="cc7b2-118">Este elemento está restringido a los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="cc7b2-119">Parallel: inicia una nueva instancia mientras se está ejecutando una instancia existente.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="cc7b2-120">Queue: inicia una nueva instancia de Task una vez completadas todas las demás instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="cc7b2-121">IgnoreNew: valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-121">IgnoreNew: Default.</span></span> <span data-ttu-id="cc7b2-122">No inicia una nueva instancia de si se está ejecutando una instancia existente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="cc7b2-123">StopExisting: detiene una instancia existente de la tarea antes de iniciar una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="cc7b2-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc7b2-124">Examples</span></span>

<span data-ttu-id="cc7b2-125">En el código XML siguiente se define un elemento de configuración que permite que varias instancias de la tarea se ejecuten en paralelo.</span><span class="sxs-lookup"><span data-stu-id="cc7b2-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="cc7b2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc7b2-126">Requirements</span></span>



| <span data-ttu-id="cc7b2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc7b2-127">Requirement</span></span> | <span data-ttu-id="cc7b2-128">Value</span><span class="sxs-lookup"><span data-stu-id="cc7b2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc7b2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc7b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7b2-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc7b2-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc7b2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc7b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7b2-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc7b2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc7b2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc7b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7b2-134">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="cc7b2-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





