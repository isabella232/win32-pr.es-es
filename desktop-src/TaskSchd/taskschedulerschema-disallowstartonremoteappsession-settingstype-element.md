---
title: Elemento DisallowStartOnRemoteAppSession (settingsType)
description: Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión local de aplicaciones remotas integrada (raíl).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Programador de tareas del elemento DisallowStartOnRemoteAppSession
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685945"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="8094b-104">Elemento DisallowStartOnRemoteAppSession (settingsType)</span><span class="sxs-lookup"><span data-stu-id="8094b-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="8094b-105">Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión local de aplicaciones remotas integrada (raíl).</span><span class="sxs-lookup"><span data-stu-id="8094b-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="8094b-106">El elemento **DisallowStartOnRemoteAppSession** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8094b-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8094b-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8094b-107">Parent element</span></span>



| <span data-ttu-id="8094b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8094b-108">Element</span></span>                                                           | <span data-ttu-id="8094b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8094b-109">Derived from</span></span>                                                         | <span data-ttu-id="8094b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8094b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8094b-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="8094b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="8094b-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="8094b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="8094b-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8094b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8094b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8094b-114">Remarks</span></span>

<span data-ttu-id="8094b-115">La configuración predeterminada de este elemento es false.</span><span class="sxs-lookup"><span data-stu-id="8094b-115">The default setting for this element is False.</span></span>

<span data-ttu-id="8094b-116">En el desarrollo de C++, se obtiene acceso a esta información a través de la propiedad [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .</span><span class="sxs-lookup"><span data-stu-id="8094b-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="8094b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8094b-117">Examples</span></span>

<span data-ttu-id="8094b-118">En el código XML siguiente se define un elemento de configuración que no permite que la tarea se inicie si la tarea se desencadena para ejecutarse en una sesión de raíl.</span><span class="sxs-lookup"><span data-stu-id="8094b-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="8094b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8094b-119">Requirements</span></span>



| <span data-ttu-id="8094b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8094b-120">Requirement</span></span> | <span data-ttu-id="8094b-121">Value</span><span class="sxs-lookup"><span data-stu-id="8094b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8094b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8094b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8094b-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8094b-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8094b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8094b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8094b-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8094b-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8094b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8094b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8094b-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8094b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





