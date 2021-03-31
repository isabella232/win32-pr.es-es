---
title: Elemento DisallowStartIfOnBatteries (settingsType)
description: Especifica que la tarea no se iniciará si el equipo se está ejecutando con baterías.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Programador de tareas del elemento DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803980"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="720fc-104">Elemento DisallowStartIfOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="720fc-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="720fc-105">Especifica que la tarea no se iniciará si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="720fc-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="720fc-106">El elemento **DisallowStartIfOnBatteries** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="720fc-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="720fc-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="720fc-107">Parent element</span></span>



| <span data-ttu-id="720fc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="720fc-108">Element</span></span>                                                           | <span data-ttu-id="720fc-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="720fc-109">Derived from</span></span>                                                         | <span data-ttu-id="720fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="720fc-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="720fc-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="720fc-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="720fc-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="720fc-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="720fc-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="720fc-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="720fc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="720fc-114">Remarks</span></span>

<span data-ttu-id="720fc-115">La configuración predeterminada de este elemento es true.</span><span class="sxs-lookup"><span data-stu-id="720fc-115">The default setting for this element is True.</span></span>

<span data-ttu-id="720fc-116">Para el desarrollo de scripting, se tiene acceso a esta información a través de la propiedad [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="720fc-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="720fc-117">En el desarrollo de C++, se obtiene acceso a esta información a través de la propiedad [**ITaskSettings::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="720fc-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="720fc-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="720fc-118">Examples</span></span>

<span data-ttu-id="720fc-119">El siguiente código XML define un elemento de configuración que no permite que la tarea se ejecute si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="720fc-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="720fc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720fc-120">Requirements</span></span>



| <span data-ttu-id="720fc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="720fc-121">Requirement</span></span> | <span data-ttu-id="720fc-122">Value</span><span class="sxs-lookup"><span data-stu-id="720fc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="720fc-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="720fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="720fc-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="720fc-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="720fc-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="720fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="720fc-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="720fc-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="720fc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="720fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720fc-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="720fc-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





