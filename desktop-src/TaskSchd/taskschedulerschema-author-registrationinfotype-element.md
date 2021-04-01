---
title: Elemento Author (registrationInfoType)
description: Especifica el autor de la tarea.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Programador de tareas del elemento Author
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996610"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="86f08-104">Elemento Author (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="86f08-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="86f08-105">Especifica el autor de la tarea.</span><span class="sxs-lookup"><span data-stu-id="86f08-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="86f08-106">El tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento **Author** .</span><span class="sxs-lookup"><span data-stu-id="86f08-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="86f08-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="86f08-107">Parent element</span></span>



| <span data-ttu-id="86f08-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="86f08-108">Element</span></span>                                                                           | <span data-ttu-id="86f08-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="86f08-109">Derived from</span></span>                                                                         | <span data-ttu-id="86f08-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="86f08-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86f08-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="86f08-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="86f08-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="86f08-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="86f08-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="86f08-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="86f08-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86f08-114">Remarks</span></span>

<span data-ttu-id="86f08-115">Para el desarrollo de scripting, el autor de la tarea se especifica mediante la propiedad [**RegistrationInfo. Author**](registrationinfo-author.md) .</span><span class="sxs-lookup"><span data-stu-id="86f08-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="86f08-116">En el desarrollo de C++, el autor de la tarea se especifica mediante la propiedad [**IRegistrationInfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .</span><span class="sxs-lookup"><span data-stu-id="86f08-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="86f08-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86f08-117">Examples</span></span>

<span data-ttu-id="86f08-118">En el código XML siguiente se define el autor de una tarea.</span><span class="sxs-lookup"><span data-stu-id="86f08-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="86f08-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86f08-119">Requirements</span></span>



| <span data-ttu-id="86f08-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="86f08-120">Requirement</span></span> | <span data-ttu-id="86f08-121">Value</span><span class="sxs-lookup"><span data-stu-id="86f08-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86f08-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86f08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86f08-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86f08-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="86f08-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86f08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86f08-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86f08-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86f08-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f08-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f08-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="86f08-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="86f08-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="86f08-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





