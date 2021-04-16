---
title: Elemento Enabled (settingsType)
description: Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Programador de tareas de elementos habilitados
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676942"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="6c800-105">Elemento Enabled (settingsType)</span><span class="sxs-lookup"><span data-stu-id="6c800-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="6c800-106">Especifica que la tarea está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6c800-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="6c800-107">La tarea solo se puede realizar cuando este valor es true.</span><span class="sxs-lookup"><span data-stu-id="6c800-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="6c800-108">El elemento **Enabled** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c800-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6c800-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6c800-109">Parent element</span></span>



| <span data-ttu-id="6c800-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c800-110">Element</span></span>                                                           | <span data-ttu-id="6c800-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6c800-111">Derived from</span></span>                                                         | <span data-ttu-id="6c800-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c800-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c800-113">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="6c800-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6c800-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="6c800-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6c800-115">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6c800-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c800-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c800-116">Remarks</span></span>

<span data-ttu-id="6c800-117">Para el desarrollo de C++, vea la [**propiedad Enabled de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="6c800-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="6c800-118">Para el desarrollo de scripts, vea [**TaskSettings. Enabled**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="6c800-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c800-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6c800-119">Examples</span></span>

<span data-ttu-id="6c800-120">Para obtener un ejemplo completo del XML de una tarea que está habilitada, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="6c800-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c800-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c800-121">Requirements</span></span>



| <span data-ttu-id="6c800-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c800-122">Requirement</span></span> | <span data-ttu-id="6c800-123">Value</span><span class="sxs-lookup"><span data-stu-id="6c800-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c800-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c800-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c800-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6c800-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c800-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c800-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c800-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c800-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





