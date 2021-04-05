---
title: Objeto RegistrationInfo
description: Objeto de scripting que proporciona la información administrativa que se puede utilizar para describir la tarea.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- Programador de tareas de información de registro, objeto
- Objeto RegistrationInfo Programador de tareas
- Programador de tareas de objeto RegistrationInfo, descrito
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079102"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="1931c-106">Objeto RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="1931c-106">RegistrationInfo object</span></span>

<span data-ttu-id="1931c-107">Objeto de scripting que proporciona la información administrativa que se puede utilizar para describir la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="1931c-108">Esta información incluye detalles como, por ejemplo, una descripción de la tarea, el autor de la tarea, la fecha de registro de la tarea y el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="1931c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1931c-109">Members</span></span>

<span data-ttu-id="1931c-110">El objeto **RegistrationInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1931c-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="1931c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1931c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1931c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1931c-112">Properties</span></span>

<span data-ttu-id="1931c-113">El objeto **RegistrationInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1931c-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="1931c-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1931c-114">Property</span></span>                                                                     | <span data-ttu-id="1931c-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1931c-115">Access type</span></span>           | <span data-ttu-id="1931c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1931c-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1931c-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="1931c-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="1931c-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-118">Read/write</span></span><br/> | <span data-ttu-id="1931c-119">Obtiene o establece el autor de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="1931c-120">**Date**</span><span class="sxs-lookup"><span data-stu-id="1931c-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="1931c-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-121">Read/write</span></span><br/> | <span data-ttu-id="1931c-122">Obtiene o establece la fecha y hora en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="1931c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1931c-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="1931c-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-124">Read/write</span></span><br/> | <span data-ttu-id="1931c-125">Obtiene o establece la descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1931c-126">**Documentación**</span><span class="sxs-lookup"><span data-stu-id="1931c-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="1931c-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-127">Read/write</span></span><br/> | <span data-ttu-id="1931c-128">Obtiene o establece cualquier documentación adicional para la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="1931c-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1931c-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="1931c-130">Obtiene o establece el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="1931c-131">**Origen**</span><span class="sxs-lookup"><span data-stu-id="1931c-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="1931c-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-132">Read/write</span></span><br/> | <span data-ttu-id="1931c-133">Obtiene o establece la ubicación de la que se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="1931c-134">Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="1931c-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="1931c-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="1931c-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="1931c-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-136">Read/write</span></span><br/> | <span data-ttu-id="1931c-137">Obtiene o establece el URI de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="1931c-138">**Versión**</span><span class="sxs-lookup"><span data-stu-id="1931c-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="1931c-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-139">Read/write</span></span><br/> | <span data-ttu-id="1931c-140">Obtiene o establece el número de versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="1931c-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="1931c-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="1931c-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1931c-142">Read/write</span></span><br/> | <span data-ttu-id="1931c-143">Obtiene o establece una versión con formato XML de la información de registro de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1931c-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="1931c-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1931c-144">Remarks</span></span>

<span data-ttu-id="1931c-145">La información de registro se puede utilizar para identificar una tarea a través de la interfaz de usuario de Programador de tareas o como criterio de búsqueda al enumerar las tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="1931c-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="1931c-146">Al leer o escribir XML para una tarea, se especifica la información de registro de la tarea en el elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="1931c-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="1931c-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1931c-147">Examples</span></span>

<span data-ttu-id="1931c-148">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="1931c-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1931c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1931c-149">Requirements</span></span>



| <span data-ttu-id="1931c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="1931c-150">Requirement</span></span> | <span data-ttu-id="1931c-151">Value</span><span class="sxs-lookup"><span data-stu-id="1931c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1931c-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1931c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1931c-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1931c-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1931c-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1931c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1931c-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1931c-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1931c-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1931c-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="1931c-157"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1931c-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1931c-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1931c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1931c-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1931c-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





