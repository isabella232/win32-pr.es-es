---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Programador de tareas del elemento StopOnIdleEnd
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996993"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="190b2-104">Elemento StopOnIdleEnd (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="190b2-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="190b2-105">Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="190b2-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="190b2-106">El elemento **StopOnIdleEnd** se define mediante el tipo complejo de [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="190b2-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="190b2-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="190b2-107">Parent element</span></span>



| <span data-ttu-id="190b2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="190b2-108">Element</span></span>                                                                       | <span data-ttu-id="190b2-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="190b2-109">Derived from</span></span>                                                                 | <span data-ttu-id="190b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="190b2-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="190b2-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="190b2-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="190b2-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="190b2-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="190b2-113">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="190b2-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="190b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="190b2-114">Remarks</span></span>

<span data-ttu-id="190b2-115">Para el desarrollo de C++, consulte la [**propiedad StopOnIdleEnd de IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="190b2-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="190b2-116">Para el desarrollo de scripts, vea [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="190b2-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="190b2-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="190b2-117">Examples</span></span>

<span data-ttu-id="190b2-118">En el código XML siguiente se define un valor de inactivo que indica que la tarea no debe realizarse cuando finaliza la condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="190b2-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="190b2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="190b2-119">Requirements</span></span>



| <span data-ttu-id="190b2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="190b2-120">Requirement</span></span> | <span data-ttu-id="190b2-121">Value</span><span class="sxs-lookup"><span data-stu-id="190b2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="190b2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="190b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="190b2-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="190b2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="190b2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="190b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="190b2-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="190b2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="190b2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="190b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190b2-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="190b2-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





