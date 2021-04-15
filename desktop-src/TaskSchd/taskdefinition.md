---
title: Objeto TaskDefinition
description: Objeto de scripting que define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Objeto TaskDefinition Programador de tareas
- Programador de tareas de objeto TaskDefinition, descrito
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534462"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="51786-105">Objeto TaskDefinition</span><span class="sxs-lookup"><span data-stu-id="51786-105">TaskDefinition object</span></span>

<span data-ttu-id="51786-106">Objeto de scripting que define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.</span><span class="sxs-lookup"><span data-stu-id="51786-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="51786-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="51786-107">Members</span></span>

<span data-ttu-id="51786-108">El objeto **TaskDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="51786-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="51786-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51786-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51786-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51786-110">Properties</span></span>

<span data-ttu-id="51786-111">El objeto **TaskDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="51786-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="51786-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51786-112">Property</span></span>                                                               | <span data-ttu-id="51786-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="51786-113">Access type</span></span>           | <span data-ttu-id="51786-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="51786-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51786-115">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="51786-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="51786-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-116">Read/write</span></span><br/> | <span data-ttu-id="51786-117">Obtiene o establece una colección de acciones que realiza la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="51786-118">**Data**</span><span class="sxs-lookup"><span data-stu-id="51786-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="51786-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-119">Read/write</span></span><br/> | <span data-ttu-id="51786-120">Obtiene o establece los datos asociados a la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="51786-121">El servicio Programador de tareas omite estos datos, pero lo usan terceros que desean ampliar el formato de la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="51786-122">**Principal**</span><span class="sxs-lookup"><span data-stu-id="51786-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="51786-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-123">Read/write</span></span><br/> | <span data-ttu-id="51786-124">Obtiene o establece la entidad de seguridad de la tarea que proporciona las credenciales de seguridad para la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="51786-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="51786-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="51786-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-126">Read/write</span></span><br/> | <span data-ttu-id="51786-127">Obtiene o establece la información de registro que se utiliza para describir una tarea, como la descripción de la tarea, el autor de la tarea y la fecha en que se ha registrado la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="51786-128">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="51786-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="51786-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-129">Read/write</span></span><br/> | <span data-ttu-id="51786-130">Obtiene o establece la configuración que define cómo realiza la tarea el servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="51786-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="51786-131">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="51786-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="51786-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-132">Read/write</span></span><br/> | <span data-ttu-id="51786-133">Obtiene o establece una colección de desencadenadores que se utilizan para iniciar una tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="51786-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="51786-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="51786-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51786-135">Read/write</span></span><br/> | <span data-ttu-id="51786-136">Obtiene o establece la definición con formato XML de la tarea.</span><span class="sxs-lookup"><span data-stu-id="51786-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="51786-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51786-137">Remarks</span></span>

<span data-ttu-id="51786-138">Al leer o escribir su propio XML para una tarea, se especifica una definición de tarea mediante el elemento [**Task**](taskschedulerschema-task-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="51786-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="51786-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51786-139">Examples</span></span>

<span data-ttu-id="51786-140">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) , ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="51786-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51786-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51786-141">Requirements</span></span>



| <span data-ttu-id="51786-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="51786-142">Requirement</span></span> | <span data-ttu-id="51786-143">Value</span><span class="sxs-lookup"><span data-stu-id="51786-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51786-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51786-144">Minimum supported client</span></span><br/> | <span data-ttu-id="51786-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="51786-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="51786-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51786-146">Minimum supported server</span></span><br/> | <span data-ttu-id="51786-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="51786-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51786-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="51786-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="51786-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="51786-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="51786-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51786-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51786-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51786-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





