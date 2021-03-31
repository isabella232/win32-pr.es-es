---
title: Propiedad SessionStateChangeTrigger. StateChange
description: Para scripting, obtiene o establece el tipo de Terminal Server cambio de sesión que desencadenaría un inicio de tarea.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Propiedad StateChange Programador de tareas
- Propiedad StateChange Programador de tareas, objeto SessionStateChangeTrigger
- Programador de tareas de objeto SessionStateChangeTrigger, propiedad StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801610"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="3ae27-106">Propiedad SessionStateChangeTrigger. StateChange</span><span class="sxs-lookup"><span data-stu-id="3ae27-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="3ae27-107">Para scripting, obtiene o establece el tipo de Terminal Server cambio de sesión que desencadenaría un inicio de tarea.</span><span class="sxs-lookup"><span data-stu-id="3ae27-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae27-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ae27-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="3ae27-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ae27-109">Property value</span></span>

<span data-ttu-id="3ae27-110">El tipo de Terminal Server cambio de sesión que desencadena la ejecución de una tarea.</span><span class="sxs-lookup"><span data-stu-id="3ae27-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="3ae27-111">Los valores posibles proceden de la enumeración de [**tipo de cambio de estado de sesión de tarea \_ \_ \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="3ae27-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="3ae27-112">Value</span><span class="sxs-lookup"><span data-stu-id="3ae27-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="3ae27-113">Significado</span><span class="sxs-lookup"><span data-stu-id="3ae27-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="3ae27-114"><dt>**Tarea \_ de \_Conexión**</dt> de la consola <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="3ae27-115">Terminal Server cambio del estado de conexión de la consola.</span><span class="sxs-lookup"><span data-stu-id="3ae27-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="3ae27-116">Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3ae27-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="3ae27-117"><dt>**Tarea \_ de \_Desconexión**</dt> de la consola <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3ae27-118">Terminal Server cambio de estado de desconexión de la consola.</span><span class="sxs-lookup"><span data-stu-id="3ae27-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="3ae27-119">Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3ae27-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="3ae27-120"><dt>**Tarea \_ de \_Conexión remota**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="3ae27-121">Terminal Server cambio de estado de la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="3ae27-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="3ae27-122">Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa de Conexión a Escritorio remoto desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="3ae27-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="3ae27-123"><dt>**Tarea \_ de \_Desconexión remota**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="3ae27-124">Terminal Server cambio de estado de desconexión remota.</span><span class="sxs-lookup"><span data-stu-id="3ae27-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="3ae27-125">Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa el programa Conexión a Escritorio remoto desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="3ae27-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="3ae27-126"><dt>**Tarea \_ de \_Bloqueo de sesión**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="3ae27-127">Terminal Server cambio de estado de la sesión bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3ae27-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="3ae27-128">Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3ae27-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="3ae27-129"><dt>**Tarea \_ de \_Desbloqueo de sesión**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="3ae27-130">Terminal Server cambio de estado desbloqueado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3ae27-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="3ae27-131">Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando se desbloquea el equipo.</span><span class="sxs-lookup"><span data-stu-id="3ae27-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="3ae27-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae27-132">Requirements</span></span>



| <span data-ttu-id="3ae27-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae27-133">Requirement</span></span> | <span data-ttu-id="3ae27-134">Value</span><span class="sxs-lookup"><span data-stu-id="3ae27-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae27-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae27-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae27-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae27-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ae27-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae27-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae27-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae27-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ae27-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ae27-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ae27-140"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ae27-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ae27-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae27-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ae27-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





