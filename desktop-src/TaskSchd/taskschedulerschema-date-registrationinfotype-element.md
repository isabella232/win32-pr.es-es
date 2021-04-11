---
title: Elemento Date (registrationInfoType)
description: Especifica la fecha y hora en que se registra la tarea.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Programador de tareas de elemento de fecha
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150604"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="8cc80-104">Elemento Date (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="8cc80-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="8cc80-105">Especifica la fecha y hora en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="8cc80-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="8cc80-106">El elemento **Date** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc80-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8cc80-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8cc80-107">Parent element</span></span>



| <span data-ttu-id="8cc80-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8cc80-108">Element</span></span>                                                                           | <span data-ttu-id="8cc80-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8cc80-109">Derived from</span></span>                                                                         | <span data-ttu-id="8cc80-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cc80-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cc80-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="8cc80-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="8cc80-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="8cc80-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="8cc80-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="8cc80-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8cc80-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cc80-114">Remarks</span></span>

<span data-ttu-id="8cc80-115">Para el desarrollo de scripting, la fecha de registro de una tarea se especifica mediante la propiedad [**RegistrationInfo. Date**](registrationinfo-date.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc80-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="8cc80-116">En el desarrollo de C++, la fecha de registro de una tarea se especifica mediante la propiedad [**IRegistrationInfo::D Alizar**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .</span><span class="sxs-lookup"><span data-stu-id="8cc80-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc80-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc80-117">Requirements</span></span>



| <span data-ttu-id="8cc80-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc80-118">Requirement</span></span> | <span data-ttu-id="8cc80-119">Value</span><span class="sxs-lookup"><span data-stu-id="8cc80-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cc80-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc80-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc80-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8cc80-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cc80-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc80-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc80-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cc80-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cc80-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cc80-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc80-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8cc80-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8cc80-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8cc80-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





