---
title: Elemento UseUnifiedSchedulingEngine (settingsType)
description: Especifica que se usará el motor de programación unificado para ejecutar esta tarea.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Programador de tareas del elemento UseUnifiedSchedulingEngine
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079156"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="ce220-104">Elemento UseUnifiedSchedulingEngine (settingsType)</span><span class="sxs-lookup"><span data-stu-id="ce220-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="ce220-105">Especifica que se usará el motor de programación unificado para ejecutar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="ce220-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="ce220-106">El elemento **UseUnifiedSchedulingEngine** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ce220-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce220-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ce220-107">Parent element</span></span>



| <span data-ttu-id="ce220-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce220-108">Element</span></span>                                                           | <span data-ttu-id="ce220-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ce220-109">Derived from</span></span>                                                         | <span data-ttu-id="ce220-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce220-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce220-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="ce220-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="ce220-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="ce220-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="ce220-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce220-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce220-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce220-114">Remarks</span></span>

<span data-ttu-id="ce220-115">La configuración predeterminada de este elemento es false.</span><span class="sxs-lookup"><span data-stu-id="ce220-115">The default setting for this element is False.</span></span>

<span data-ttu-id="ce220-116">En el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**ITaskSettings2:: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .</span><span class="sxs-lookup"><span data-stu-id="ce220-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ce220-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ce220-117">Examples</span></span>

<span data-ttu-id="ce220-118">En el código XML siguiente se define un elemento de configuración que especifica que se usará el motor de programación unificado para ejecutar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="ce220-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="ce220-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce220-119">Requirements</span></span>



| <span data-ttu-id="ce220-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce220-120">Requirement</span></span> | <span data-ttu-id="ce220-121">Value</span><span class="sxs-lookup"><span data-stu-id="ce220-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ce220-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce220-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce220-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce220-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ce220-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce220-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce220-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce220-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce220-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce220-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce220-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="ce220-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





