---
title: Propiedad EventTrigger. ValueQueries
description: En el caso de scripting, obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de suscripción.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Programador de tareas de la propiedad ValueQueries
- Propiedad ValueQueries Programador de tareas, objeto EventTrigger
- Objeto EventTrigger Programador de tareas, propiedad ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534894"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="c2015-107">Propiedad EventTrigger. ValueQueries</span><span class="sxs-lookup"><span data-stu-id="c2015-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="c2015-108">En el caso de scripting, obtiene o establece una colección de consultas XPath con nombre.</span><span class="sxs-lookup"><span data-stu-id="c2015-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="c2015-109">Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de [**suscripción**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="c2015-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2015-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2015-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="c2015-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c2015-111">Property value</span></span>

<span data-ttu-id="c2015-112">Colección de de pares nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="c2015-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="c2015-113">Cada par nombre-valor de la colección define un nombre único para un valor de propiedad del evento que desencadena el desencadenador de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2015-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="c2015-114">El valor de propiedad del evento se define como una consulta de evento XPath.</span><span class="sxs-lookup"><span data-stu-id="c2015-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="c2015-115">Para obtener más información acerca de las consultas de eventos XPath, consulte [selección de eventos](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c2015-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2015-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2015-116">Remarks</span></span>

<span data-ttu-id="c2015-117">El nombre de la consulta se puede usar como una variable en las siguientes propiedades de acción:</span><span class="sxs-lookup"><span data-stu-id="c2015-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="c2015-118">**ShowMessageAction. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="c2015-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="c2015-119">**ShowMessageAction. title**</span><span class="sxs-lookup"><span data-stu-id="c2015-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="c2015-120">**ExecAction. arguments**</span><span class="sxs-lookup"><span data-stu-id="c2015-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="c2015-121">**ExecAction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="c2015-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="c2015-122">**EmailAction. Server**</span><span class="sxs-lookup"><span data-stu-id="c2015-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="c2015-123">**EmailAction. Subject**</span><span class="sxs-lookup"><span data-stu-id="c2015-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="c2015-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="c2015-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="c2015-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="c2015-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="c2015-126">**EmailAction. BCC**</span><span class="sxs-lookup"><span data-stu-id="c2015-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="c2015-127">**EmailAction. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="c2015-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="c2015-128">**EmailAction. from**</span><span class="sxs-lookup"><span data-stu-id="c2015-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="c2015-129">**EmailAction. Body**</span><span class="sxs-lookup"><span data-stu-id="c2015-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="c2015-130">**ComHandlerAction. Data**</span><span class="sxs-lookup"><span data-stu-id="c2015-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="c2015-131">Las cadenas de ejemplo de código siguientes muestran dos pares de nombre y valor que se pueden usar en una colección de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="c2015-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="c2015-132">Los valores devueltos por las consultas XPath pueden reemplazar las variables en la propiedad de una acción.</span><span class="sxs-lookup"><span data-stu-id="c2015-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="c2015-133">Se hace referencia a los valores por nombre, con `$(user)` y `$(machine)` , en la propiedad Action.</span><span class="sxs-lookup"><span data-stu-id="c2015-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="c2015-134">Por ejemplo, si `$(user)` `$(machine)` se usan las variables y en la cadena [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , el valor de las consultas XPath reemplazará las variables de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c2015-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="c2015-135">Para obtener más información sobre cómo escribir una cadena de consulta para determinados eventos, vea [selección de eventos](/previous-versions//aa385231(v=vs.85)) y [suscripción a eventos](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="c2015-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2015-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2015-136">Requirements</span></span>



| <span data-ttu-id="c2015-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2015-137">Requirement</span></span> | <span data-ttu-id="c2015-138">Value</span><span class="sxs-lookup"><span data-stu-id="c2015-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2015-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2015-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c2015-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2015-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c2015-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2015-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c2015-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2015-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2015-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c2015-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2015-144"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2015-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2015-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2015-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2015-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2015-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2015-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2015-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2015-148">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c2015-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c2015-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c2015-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

