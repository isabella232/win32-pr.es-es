---
title: Propiedad EventTrigger. subscription
description: En el caso de scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Programador de tareas de propiedad de suscripción
- Propiedad subscription Programador de tareas, objeto EventTrigger
- Objeto EventTrigger Programador de tareas, propiedad subscription
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686128"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="4fb84-106">Propiedad EventTrigger. subscription</span><span class="sxs-lookup"><span data-stu-id="4fb84-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="4fb84-107">En el caso de scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4fb84-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb84-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fb84-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="4fb84-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4fb84-109">Property value</span></span>

<span data-ttu-id="4fb84-110">Cadena de consulta que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4fb84-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb84-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fb84-111">Remarks</span></span>

<span data-ttu-id="4fb84-112">Al leer o escribir su propio XML para una tarea, la suscripción de eventos se especifica mediante el elemento de [**suscripción**](taskschedulerschema-subscription-eventtriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4fb84-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="4fb84-113">Para obtener más información sobre cómo escribir una cadena de consulta para determinados eventos, vea [selección de eventos](/previous-versions//aa385231(v=vs.85)) y [suscripción a eventos](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="4fb84-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4fb84-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4fb84-114">Examples</span></span>

<span data-ttu-id="4fb84-115">La siguiente cadena de consulta define una suscripción a todos los eventos de nivel 2 en el canal del sistema:</span><span class="sxs-lookup"><span data-stu-id="4fb84-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="4fb84-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fb84-116">Requirements</span></span>



| <span data-ttu-id="4fb84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb84-117">Requirement</span></span> | <span data-ttu-id="4fb84-118">Value</span><span class="sxs-lookup"><span data-stu-id="4fb84-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb84-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb84-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4fb84-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4fb84-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb84-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fb84-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fb84-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4fb84-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fb84-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fb84-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fb84-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fb84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb84-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb84-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb84-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb84-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4fb84-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4fb84-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="4fb84-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

