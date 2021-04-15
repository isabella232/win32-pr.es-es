---
title: ActionCollection. Create (método)
description: En el caso de scripting, crea y agrega una nueva acción a la colección.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Crear método Programador de tareas
- Create Method Programador de tareas, ActionCollection Object
- Programador de tareas de objeto ActionCollection, Create (método)
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534618"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="13bb3-106">ActionCollection. Create (método)</span><span class="sxs-lookup"><span data-stu-id="13bb3-106">ActionCollection.Create method</span></span>

<span data-ttu-id="13bb3-107">En el caso de scripting, crea y agrega una nueva acción a la colección.</span><span class="sxs-lookup"><span data-stu-id="13bb3-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bb3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13bb3-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="13bb3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13bb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bb3-110">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="13bb3-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13bb3-111">Este parámetro se establece en una de las siguientes constantes de enumeración de [**\_ \_ tipo de acción de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="13bb3-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="13bb3-112">Value</span><span class="sxs-lookup"><span data-stu-id="13bb3-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="13bb3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="13bb3-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="13bb3-114"><dt>**Tarea \_ de ACCIÓN \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="13bb3-115">La acción realiza una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="13bb3-115">The action performs a command-line operation.</span></span> <span data-ttu-id="13bb3-116">Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.</span><span class="sxs-lookup"><span data-stu-id="13bb3-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="13bb3-117"><dt>**Tarea \_ de \_ \_ Controlador com de acción**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="13bb3-118">La acción activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="13bb3-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="13bb3-119"><dt>**Tarea \_ de ACCIÓN de \_ envío de \_ correo electrónico**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="13bb3-120">Esta acción envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="13bb3-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="13bb3-121"><dt>**Tarea \_ de ACCIÓN \_ Mostrar \_ mensaje**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="13bb3-122">Esta acción muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="13bb3-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bb3-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13bb3-123">Return value</span></span>

<span data-ttu-id="13bb3-124">Objeto de [**acción**](action.md) que representa la nueva acción.</span><span class="sxs-lookup"><span data-stu-id="13bb3-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bb3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13bb3-125">Remarks</span></span>

<span data-ttu-id="13bb3-126">No se pueden agregar más de 32 acciones a la colección.</span><span class="sxs-lookup"><span data-stu-id="13bb3-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bb3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13bb3-127">Requirements</span></span>



| <span data-ttu-id="13bb3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="13bb3-128">Requirement</span></span> | <span data-ttu-id="13bb3-129">Value</span><span class="sxs-lookup"><span data-stu-id="13bb3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13bb3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13bb3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13bb3-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13bb3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13bb3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13bb3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13bb3-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="13bb3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13bb3-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="13bb3-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="13bb3-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13bb3-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13bb3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13bb3-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bb3-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13bb3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="13bb3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bb3-139">**\_tipo de acción de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="13bb3-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="13bb3-140">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="13bb3-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="13bb3-141">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="13bb3-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="13bb3-142">**Acción**</span><span class="sxs-lookup"><span data-stu-id="13bb3-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="13bb3-143">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="13bb3-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="13bb3-144">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="13bb3-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="13bb3-145">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="13bb3-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="13bb3-146">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="13bb3-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





