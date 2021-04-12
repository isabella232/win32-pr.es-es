---
title: Action. Type (propiedad)
description: En el caso de scripting, obtiene el tipo de la acción.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Propiedad Type Programador de tareas
- Propiedad Type Programador de tareas, objeto Action
- Objeto de acción Programador de tareas, propiedad de tipo
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491704"
---
# <a name="actiontype-property"></a><span data-ttu-id="accd3-106">Action. Type (propiedad)</span><span class="sxs-lookup"><span data-stu-id="accd3-106">Action.Type property</span></span>

<span data-ttu-id="accd3-107">En el caso de scripting, obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="accd3-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="accd3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="accd3-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="accd3-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="accd3-109">Property value</span></span>

<span data-ttu-id="accd3-110">Esta propiedad devuelve una de las siguientes constantes de enumeración de [**\_ \_ tipo de acción de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="accd3-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="accd3-111">Value</span><span class="sxs-lookup"><span data-stu-id="accd3-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="accd3-112">Significado</span><span class="sxs-lookup"><span data-stu-id="accd3-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="accd3-113"><dt>**Tarea \_ de ACCIÓN \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="accd3-114">Esta acción realiza una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="accd3-114">This action performs a command-line operation.</span></span> <span data-ttu-id="accd3-115">Por ejemplo, la acción podría ejecutar un script, iniciar un ejecutable o, si se proporciona el nombre de un documento, buscar su aplicación asociada e iniciar la aplicación con el documento.</span><span class="sxs-lookup"><span data-stu-id="accd3-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="accd3-116"><dt>**Tarea \_ de \_ \_ Controlador com de acción**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="accd3-117">Esta acción activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="accd3-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="accd3-118"><dt>**Tarea \_ de ACCIÓN de \_ envío de \_ correo electrónico**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="accd3-119">Esta acción envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="accd3-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="accd3-120"><dt>**Tarea \_ de ACCIÓN \_ Mostrar \_ mensaje**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="accd3-121">Esta acción muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="accd3-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="accd3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="accd3-122">Remarks</span></span>

<span data-ttu-id="accd3-123">El tipo de acción se define cuando se crea la acción y no se puede cambiar más adelante.</span><span class="sxs-lookup"><span data-stu-id="accd3-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="accd3-124">Para obtener información sobre cómo crear una acción, vea [**ActionCollection. Create**](actioncollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="accd3-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="accd3-125">Para obtener información sobre cómo funcionan conjuntamente las acciones y tareas, vea [acciones de tarea](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="accd3-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="accd3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accd3-126">Requirements</span></span>



| <span data-ttu-id="accd3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="accd3-127">Requirement</span></span> | <span data-ttu-id="accd3-128">Value</span><span class="sxs-lookup"><span data-stu-id="accd3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="accd3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accd3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="accd3-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="accd3-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="accd3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accd3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="accd3-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="accd3-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="accd3-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="accd3-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="accd3-134"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="accd3-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="accd3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="accd3-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="accd3-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="accd3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="accd3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accd3-138">**\_tipo de acción de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="accd3-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="accd3-139">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="accd3-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="accd3-140">**Acción**</span><span class="sxs-lookup"><span data-stu-id="accd3-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





