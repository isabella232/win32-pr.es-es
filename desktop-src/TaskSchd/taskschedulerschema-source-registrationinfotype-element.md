---
title: Elemento Source (registrationInfoType)
description: Especifica el origen desde el que se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento de origen Programador de tareas
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422031"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="01499-105">Elemento Source (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="01499-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="01499-106">Especifica el origen desde el que se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="01499-106">Specifies where the task originated from.</span></span> <span data-ttu-id="01499-107">Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.</span><span class="sxs-lookup"><span data-stu-id="01499-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="01499-108">El elemento de **origen** se define mediante el tipo complejo de [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="01499-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="01499-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="01499-109">Parent element</span></span>



| <span data-ttu-id="01499-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="01499-110">Element</span></span>                                                                           | <span data-ttu-id="01499-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="01499-111">Derived from</span></span>                                                                         | <span data-ttu-id="01499-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="01499-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01499-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="01499-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="01499-114">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="01499-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="01499-115">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="01499-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="01499-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01499-116">Remarks</span></span>

<span data-ttu-id="01499-117">Para el desarrollo de scripting, el origen de una tarea se especifica mediante la propiedad [**RegistrationInfo. Source**](registrationinfo-source.md) .</span><span class="sxs-lookup"><span data-stu-id="01499-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="01499-118">En el desarrollo de C++, el origen de una tarea se especifica mediante la propiedad [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .</span><span class="sxs-lookup"><span data-stu-id="01499-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="01499-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01499-119">Requirements</span></span>



| <span data-ttu-id="01499-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="01499-120">Requirement</span></span> | <span data-ttu-id="01499-121">Value</span><span class="sxs-lookup"><span data-stu-id="01499-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01499-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01499-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01499-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="01499-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01499-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01499-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01499-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="01499-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01499-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="01499-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01499-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="01499-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="01499-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="01499-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





