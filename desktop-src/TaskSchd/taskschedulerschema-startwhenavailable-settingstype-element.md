---
title: Elemento StartWhenAvailable (settingsType)
description: Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Programador de tareas del elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996086"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="2c4da-104">Elemento StartWhenAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="2c4da-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="2c4da-105">Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.</span><span class="sxs-lookup"><span data-stu-id="2c4da-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="2c4da-106">El elemento **StartWhenAvailable** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c4da-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2c4da-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2c4da-107">Parent element</span></span>



| <span data-ttu-id="2c4da-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c4da-108">Element</span></span>                                                           | <span data-ttu-id="2c4da-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2c4da-109">Derived from</span></span>                                                         | <span data-ttu-id="2c4da-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c4da-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c4da-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="2c4da-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="2c4da-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="2c4da-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="2c4da-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="2c4da-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c4da-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c4da-114">Remarks</span></span>

<span data-ttu-id="2c4da-115">Esta propiedad solo se aplica a las tareas con tiempo.</span><span class="sxs-lookup"><span data-stu-id="2c4da-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="2c4da-116">Para el desarrollo de C++, consulte la [**propiedad StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="2c4da-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="2c4da-117">Para el desarrollo de scripts, vea [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="2c4da-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2c4da-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2c4da-118">Examples</span></span>

<span data-ttu-id="2c4da-119">En el código XML siguiente se define un elemento de configuración que permite al Programador de tareas iniciar la tarea cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="2c4da-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="2c4da-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c4da-120">Requirements</span></span>



| <span data-ttu-id="2c4da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c4da-121">Requirement</span></span> | <span data-ttu-id="2c4da-122">Value</span><span class="sxs-lookup"><span data-stu-id="2c4da-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c4da-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4da-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4da-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c4da-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4da-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4da-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c4da-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c4da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4da-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="2c4da-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





