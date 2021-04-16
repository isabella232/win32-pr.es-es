---
title: Elemento version (registrationInfoType)
description: Especifica el número de versión de la tarea.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento version Programador de tareas
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685880"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="b144a-104">Elemento version (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="b144a-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="b144a-105">Especifica el número de versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b144a-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="b144a-106">El elemento **version** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b144a-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b144a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b144a-107">Parent element</span></span>



| <span data-ttu-id="b144a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b144a-108">Element</span></span>                                                                           | <span data-ttu-id="b144a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b144a-109">Derived from</span></span>                                                                         | <span data-ttu-id="b144a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b144a-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b144a-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b144a-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="b144a-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="b144a-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="b144a-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="b144a-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b144a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b144a-114">Remarks</span></span>

<span data-ttu-id="b144a-115">Para el desarrollo de scripting, la versión de una tarea se especifica mediante la propiedad [**RegistrationInfo. version**](registrationinfo-version.md) .</span><span class="sxs-lookup"><span data-stu-id="b144a-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="b144a-116">En el desarrollo de C++, la versión de una tarea se especifica mediante la propiedad [**IRegistrationInfo:: version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .</span><span class="sxs-lookup"><span data-stu-id="b144a-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b144a-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b144a-117">Examples</span></span>

<span data-ttu-id="b144a-118">El siguiente código XML define la versión de una tarea.</span><span class="sxs-lookup"><span data-stu-id="b144a-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="b144a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b144a-119">Requirements</span></span>



| <span data-ttu-id="b144a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b144a-120">Requirement</span></span> | <span data-ttu-id="b144a-121">Value</span><span class="sxs-lookup"><span data-stu-id="b144a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b144a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b144a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b144a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b144a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b144a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b144a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b144a-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b144a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b144a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b144a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b144a-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b144a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b144a-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b144a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





