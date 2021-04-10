---
title: Elemento AllowStartOnDemand (settingsType)
description: Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Programador de tareas del elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996089"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="46bee-104">Elemento AllowStartOnDemand (settingsType)</span><span class="sxs-lookup"><span data-stu-id="46bee-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="46bee-105">Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="46bee-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="46bee-106">El elemento **AllowStartOnDemand** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="46bee-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="46bee-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="46bee-107">Parent element</span></span>



| <span data-ttu-id="46bee-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="46bee-108">Element</span></span>                                                           | <span data-ttu-id="46bee-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="46bee-109">Derived from</span></span>                                                         | <span data-ttu-id="46bee-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="46bee-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="46bee-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="46bee-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="46bee-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="46bee-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="46bee-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="46bee-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="46bee-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46bee-114">Remarks</span></span>

<span data-ttu-id="46bee-115">Cuando este elemento se establece en true, la tarea se puede iniciar independientemente de cuando cualquier desencadenador inicie la tarea.</span><span class="sxs-lookup"><span data-stu-id="46bee-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="46bee-116">Para el desarrollo de C++, vea la [**propiedad AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="46bee-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="46bee-117">Para el desarrollo de scripts, vea [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="46bee-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="46bee-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="46bee-118">Examples</span></span>

<span data-ttu-id="46bee-119">Para obtener un ejemplo completo del XML de una tarea que permite el inicio de la demanda, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="46bee-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46bee-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46bee-120">Requirements</span></span>



| <span data-ttu-id="46bee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46bee-121">Requirement</span></span> | <span data-ttu-id="46bee-122">Value</span><span class="sxs-lookup"><span data-stu-id="46bee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46bee-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46bee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46bee-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46bee-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46bee-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46bee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46bee-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="46bee-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46bee-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="46bee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46bee-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="46bee-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





