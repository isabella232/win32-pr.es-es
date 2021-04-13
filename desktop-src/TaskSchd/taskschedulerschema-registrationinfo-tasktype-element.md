---
title: Elemento RegistrationInfo (taskType)
description: Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- información de registro Programador de tareas, elemento XML
- Programador de tareas del elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491675"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="aa892-105">Elemento RegistrationInfo (taskType)</span><span class="sxs-lookup"><span data-stu-id="aa892-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="aa892-106">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="aa892-107">El elemento **RegistrationInfo** se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="aa892-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="aa892-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="aa892-108">Parent element</span></span>



| <span data-ttu-id="aa892-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa892-109">Element</span></span>                                          | <span data-ttu-id="aa892-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="aa892-110">Derived from</span></span>                                                 | <span data-ttu-id="aa892-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa892-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="aa892-112">**Task**</span><span class="sxs-lookup"><span data-stu-id="aa892-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="aa892-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="aa892-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="aa892-114">Define la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="aa892-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="aa892-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa892-115">Child elements</span></span>



| <span data-ttu-id="aa892-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa892-116">Element</span></span>                                                                                                                  | <span data-ttu-id="aa892-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa892-117">Type</span></span>     | <span data-ttu-id="aa892-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa892-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa892-119">**Autor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="aa892-120">string</span><span class="sxs-lookup"><span data-stu-id="aa892-120">string</span></span>   | <span data-ttu-id="aa892-121">Especifica el autor de la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="aa892-122">**Fecha (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="aa892-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="aa892-123">dateTime</span></span> | <span data-ttu-id="aa892-124">Especifica la fecha y hora en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="aa892-125">**Descripción (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="aa892-126">string</span><span class="sxs-lookup"><span data-stu-id="aa892-126">string</span></span>   | <span data-ttu-id="aa892-127">Especifica la descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="aa892-128">**Documentación (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="aa892-129">string</span><span class="sxs-lookup"><span data-stu-id="aa892-129">string</span></span>   | <span data-ttu-id="aa892-130">Especifica cualquier documentación adicional para la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="aa892-131">**SecurityDescriptor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="aa892-132">string</span><span class="sxs-lookup"><span data-stu-id="aa892-132">string</span></span>   | <span data-ttu-id="aa892-133">Especifica el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="aa892-134">**Origen (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="aa892-135">string</span><span class="sxs-lookup"><span data-stu-id="aa892-135">string</span></span>   | <span data-ttu-id="aa892-136">Especifica el origen desde el que se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-136">Specifies where the task originated from.</span></span> <span data-ttu-id="aa892-137">Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.</span><span class="sxs-lookup"><span data-stu-id="aa892-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="aa892-138">**URI (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="aa892-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="aa892-139">anyURI</span></span>   | <span data-ttu-id="aa892-140">Especifica el URI de la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="aa892-141">**Versión (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="aa892-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="aa892-142">string</span><span class="sxs-lookup"><span data-stu-id="aa892-142">string</span></span>   | <span data-ttu-id="aa892-143">Especifica el número de versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="aa892-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="aa892-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa892-144">Remarks</span></span>

<span data-ttu-id="aa892-145">Para el desarrollo de scripts, la información de registro de una tarea se especifica mediante la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aa892-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="aa892-146">En el desarrollo de C++, la información de registro de una tarea se especifica mediante la [**propiedad RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span><span class="sxs-lookup"><span data-stu-id="aa892-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa892-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa892-147">Requirements</span></span>



| <span data-ttu-id="aa892-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa892-148">Requirement</span></span> | <span data-ttu-id="aa892-149">Value</span><span class="sxs-lookup"><span data-stu-id="aa892-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa892-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa892-150">Minimum supported client</span></span><br/> | <span data-ttu-id="aa892-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa892-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa892-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa892-152">Minimum supported server</span></span><br/> | <span data-ttu-id="aa892-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa892-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa892-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa892-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa892-155">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="aa892-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="aa892-156">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="aa892-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





