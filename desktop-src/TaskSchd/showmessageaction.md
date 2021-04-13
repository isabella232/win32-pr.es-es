---
title: Objeto ShowMessageAction
description: En el caso de scripting, representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Objeto ShowMessageAction Programador de tareas
- Programador de tareas de objeto ShowMessageAction, descrito
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422099"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="ea567-105">Objeto ShowMessageAction</span><span class="sxs-lookup"><span data-stu-id="ea567-105">ShowMessageAction object</span></span>

<span data-ttu-id="ea567-106">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="ea567-106">\[This object is no longer supported.</span></span> <span data-ttu-id="ea567-107">Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.\]</span><span class="sxs-lookup"><span data-stu-id="ea567-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="ea567-108">En el caso de scripting, representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.</span><span class="sxs-lookup"><span data-stu-id="ea567-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="ea567-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea567-109">Members</span></span>

<span data-ttu-id="ea567-110">El objeto **ShowMessageAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ea567-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="ea567-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea567-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea567-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea567-112">Properties</span></span>

<span data-ttu-id="ea567-113">El objeto **ShowMessageAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea567-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="ea567-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea567-114">Property</span></span>                                                        | <span data-ttu-id="ea567-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ea567-115">Access type</span></span>           | <span data-ttu-id="ea567-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea567-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea567-117">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="ea567-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="ea567-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ea567-118">Read/write</span></span><br/> | <span data-ttu-id="ea567-119">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="ea567-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="ea567-120">Obtiene o establece el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="ea567-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="ea567-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="ea567-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="ea567-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ea567-122">Read/write</span></span><br/> | <span data-ttu-id="ea567-123">Obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ea567-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="ea567-124">**Title**</span><span class="sxs-lookup"><span data-stu-id="ea567-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="ea567-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ea567-125">Read/write</span></span><br/> | <span data-ttu-id="ea567-126">Obtiene o establece el título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ea567-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="ea567-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ea567-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="ea567-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea567-128">Read-only</span></span><br/>  | <span data-ttu-id="ea567-129">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="ea567-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="ea567-130">Obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="ea567-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="ea567-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea567-131">Remarks</span></span>

<span data-ttu-id="ea567-132">En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo.</span><span class="sxs-lookup"><span data-stu-id="ea567-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="ea567-133">Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad [**LogonType**](principal-logontype.md) de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ea567-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="ea567-134">Al leer o escribir su propio XML para una tarea, se especifica una acción de cuadro de mensaje mediante el elemento [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ea567-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="ea567-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ea567-135">Examples</span></span>

<span data-ttu-id="ea567-136">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de cuadro de mensaje (scripting)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea567-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea567-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea567-137">Requirements</span></span>



| <span data-ttu-id="ea567-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea567-138">Requirement</span></span> | <span data-ttu-id="ea567-139">Value</span><span class="sxs-lookup"><span data-stu-id="ea567-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea567-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea567-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ea567-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea567-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ea567-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea567-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ea567-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea567-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea567-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ea567-144">End of client support</span></span><br/>    | <span data-ttu-id="ea567-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea567-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="ea567-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ea567-146">End of server support</span></span><br/>    | <span data-ttu-id="ea567-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea567-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ea567-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ea567-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea567-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea567-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea567-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea567-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea567-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea567-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

