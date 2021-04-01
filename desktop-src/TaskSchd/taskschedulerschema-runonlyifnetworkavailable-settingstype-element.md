---
title: Elemento RunOnlyIfNetworkAvailable (settingsType)
description: Especifica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Programador de tareas del elemento RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996883"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="6784c-104">Elemento RunOnlyIfNetworkAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="6784c-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="6784c-105">Especifica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.</span><span class="sxs-lookup"><span data-stu-id="6784c-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="6784c-106">El elemento **RunOnlyIfNetworkAvailable** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6784c-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6784c-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6784c-107">Parent element</span></span>



| <span data-ttu-id="6784c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6784c-108">Element</span></span>                                                           | <span data-ttu-id="6784c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6784c-109">Derived from</span></span>                                                         | <span data-ttu-id="6784c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6784c-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6784c-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="6784c-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6784c-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="6784c-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6784c-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6784c-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6784c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6784c-114">Remarks</span></span>

<span data-ttu-id="6784c-115">Para el desarrollo de C++, consulte la [**propiedad RunOnlyIfNetworkAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="6784c-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="6784c-116">Para el desarrollo de scripts, vea [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="6784c-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6784c-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6784c-117">Examples</span></span>

<span data-ttu-id="6784c-118">En el código XML siguiente se define un elemento de configuración que permite que la tarea se inicie solo si una red está disponible.</span><span class="sxs-lookup"><span data-stu-id="6784c-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="6784c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6784c-119">Requirements</span></span>



| <span data-ttu-id="6784c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6784c-120">Requirement</span></span> | <span data-ttu-id="6784c-121">Value</span><span class="sxs-lookup"><span data-stu-id="6784c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6784c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6784c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6784c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6784c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6784c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6784c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6784c-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6784c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6784c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6784c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6784c-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="6784c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





