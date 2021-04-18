---
title: Elemento StopIfGoingOnBatteries (settingsType)
description: Especifica que la tarea se detendrá si el equipo pasa a baterías.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Programador de tareas del elemento StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685938"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="cbed0-104">Elemento StopIfGoingOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="cbed0-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="cbed0-105">Especifica que la tarea se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="cbed0-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="cbed0-106">El elemento **StopIfGoingOnBatteries** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cbed0-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cbed0-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cbed0-107">Parent element</span></span>



| <span data-ttu-id="cbed0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cbed0-108">Element</span></span>                                                           | <span data-ttu-id="cbed0-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="cbed0-109">Derived from</span></span>                                                         | <span data-ttu-id="cbed0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbed0-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbed0-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="cbed0-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="cbed0-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="cbed0-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="cbed0-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="cbed0-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cbed0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbed0-114">Remarks</span></span>

<span data-ttu-id="cbed0-115">La configuración predeterminada de este elemento es false.</span><span class="sxs-lookup"><span data-stu-id="cbed0-115">The default setting for this element is False.</span></span> <span data-ttu-id="cbed0-116">Tenga en cuenta que el valor predeterminado ha cambiado respecto a las versiones anteriores de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="cbed0-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="cbed0-117">Para el desarrollo de scripting, este valor se especifica mediante la propiedad [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="cbed0-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="cbed0-118">En el desarrollo de C++, este valor se especifica mediante la propiedad [**ITaskSettings:: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="cbed0-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="cbed0-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cbed0-119">Examples</span></span>

<span data-ttu-id="cbed0-120">En el código XML siguiente se define un elemento de configuración que permite una finalización rígida de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cbed0-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="cbed0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbed0-121">Requirements</span></span>



| <span data-ttu-id="cbed0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbed0-122">Requirement</span></span> | <span data-ttu-id="cbed0-123">Value</span><span class="sxs-lookup"><span data-stu-id="cbed0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cbed0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbed0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cbed0-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cbed0-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cbed0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbed0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cbed0-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbed0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbed0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbed0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbed0-129">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="cbed0-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





