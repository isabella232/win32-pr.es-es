---
title: SecurityDescriptor (registrationInfoType), elemento
description: Especifica el descriptor de seguridad de la tarea.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Elemento SecurityDescriptor Programador de tareas
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079044"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="5aa76-104">SecurityDescriptor (registrationInfoType), elemento</span><span class="sxs-lookup"><span data-stu-id="5aa76-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="5aa76-105">Especifica el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5aa76-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="5aa76-106">El elemento **SecurityDescriptor** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa76-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5aa76-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5aa76-107">Parent element</span></span>



| <span data-ttu-id="5aa76-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5aa76-108">Element</span></span>                                                                           | <span data-ttu-id="5aa76-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5aa76-109">Derived from</span></span>                                                                         | <span data-ttu-id="5aa76-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa76-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5aa76-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="5aa76-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="5aa76-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="5aa76-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="5aa76-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="5aa76-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5aa76-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa76-114">Remarks</span></span>

<span data-ttu-id="5aa76-115">Para el desarrollo de scripting, el descriptor de seguridad de una tarea se especifica mediante la propiedad [**RegistrationInfo. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa76-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="5aa76-116">En el desarrollo de C++, el descriptor de seguridad de una tarea se especifica mediante la propiedad [**IRegistrationInfo:: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="5aa76-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa76-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa76-117">Requirements</span></span>



| <span data-ttu-id="5aa76-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa76-118">Requirement</span></span> | <span data-ttu-id="5aa76-119">Value</span><span class="sxs-lookup"><span data-stu-id="5aa76-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5aa76-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa76-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5aa76-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5aa76-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa76-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5aa76-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5aa76-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa76-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa76-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5aa76-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5aa76-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5aa76-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





