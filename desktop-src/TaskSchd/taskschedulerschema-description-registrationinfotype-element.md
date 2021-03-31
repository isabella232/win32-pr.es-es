---
title: Elemento Description (registrationInfoType)
description: Especifica la descripción de la tarea.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Elemento Description Programador de tareas
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801766"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="0ca61-104">Elemento Description (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="0ca61-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="0ca61-105">Especifica la descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="0ca61-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="0ca61-106">El elemento **Description** se define mediante el tipo complejo de [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0ca61-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0ca61-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="0ca61-107">Parent element</span></span>



| <span data-ttu-id="0ca61-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ca61-108">Element</span></span>                                                                           | <span data-ttu-id="0ca61-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="0ca61-109">Derived from</span></span>                                                                         | <span data-ttu-id="0ca61-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ca61-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ca61-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="0ca61-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="0ca61-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="0ca61-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="0ca61-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="0ca61-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0ca61-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ca61-114">Remarks</span></span>

<span data-ttu-id="0ca61-115">Para el desarrollo de scripting, la descripción de una tarea se especifica mediante la propiedad [**RegistrationInfo. Description**](registrationinfo-description.md) .</span><span class="sxs-lookup"><span data-stu-id="0ca61-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="0ca61-116">En el desarrollo de C++, la descripción de una tarea se especifica mediante la propiedad [**IRegistrationInfo::D Descripción**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .</span><span class="sxs-lookup"><span data-stu-id="0ca61-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca61-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ca61-117">Requirements</span></span>



| <span data-ttu-id="0ca61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca61-118">Requirement</span></span> | <span data-ttu-id="0ca61-119">Value</span><span class="sxs-lookup"><span data-stu-id="0ca61-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ca61-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ca61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca61-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ca61-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ca61-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ca61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca61-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ca61-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ca61-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ca61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca61-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="0ca61-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0ca61-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0ca61-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





