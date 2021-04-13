---
title: ShowMessage (actionGroup) (elemento)
description: Representa una acción que muestra un cuadro de mensaje.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359697"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="bec07-104">ShowMessage (actionGroup) (elemento)</span><span class="sxs-lookup"><span data-stu-id="bec07-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="bec07-105">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bec07-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="bec07-106">El elemento **ShowMessage** está definido por [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="bec07-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="bec07-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="bec07-107">Parent element</span></span>



| <span data-ttu-id="bec07-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bec07-108">Element</span></span>                                                                    | <span data-ttu-id="bec07-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bec07-109">Derived from</span></span>                                                       | <span data-ttu-id="bec07-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bec07-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="bec07-111">**Acciones (taskType)**</span><span class="sxs-lookup"><span data-stu-id="bec07-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="bec07-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="bec07-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="bec07-113">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="bec07-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="bec07-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bec07-114">Child elements</span></span>



| <span data-ttu-id="bec07-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="bec07-115">Element</span></span>                                                            | <span data-ttu-id="bec07-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="bec07-116">Type</span></span>           | <span data-ttu-id="bec07-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bec07-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="bec07-118">**Principal**</span><span class="sxs-lookup"><span data-stu-id="bec07-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="bec07-119">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="bec07-119">nonEmptyString</span></span> | <span data-ttu-id="bec07-120">Especifica el texto que se va a mostrar en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bec07-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="bec07-121">**Title**</span><span class="sxs-lookup"><span data-stu-id="bec07-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="bec07-122">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="bec07-122">nonEmptyString</span></span> | <span data-ttu-id="bec07-123">Especifica el título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bec07-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="bec07-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bec07-124">Remarks</span></span>

<span data-ttu-id="bec07-125">Para el desarrollo de scripting, se especifica una acción de cuadro de mensaje mediante el objeto [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="bec07-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="bec07-126">En el desarrollo de C++, se especifica una acción de cuadro de mensaje mediante la interfaz [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .</span><span class="sxs-lookup"><span data-stu-id="bec07-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="bec07-127">**Windows 8 y Windows Server 2012:** Este elemento se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="bec07-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="bec07-128">Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="bec07-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="bec07-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bec07-129">Examples</span></span>

<span data-ttu-id="bec07-130">Para obtener un ejemplo completo del XML de una tarea que usa una acción de cuadro de mensaje, vea [ejemplo de cuadro de mensaje (XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bec07-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bec07-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bec07-131">Requirements</span></span>



| <span data-ttu-id="bec07-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec07-132">Requirement</span></span> | <span data-ttu-id="bec07-133">Value</span><span class="sxs-lookup"><span data-stu-id="bec07-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bec07-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bec07-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bec07-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bec07-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bec07-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bec07-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bec07-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bec07-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bec07-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bec07-138">End of client support</span></span><br/>    | <span data-ttu-id="bec07-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bec07-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="bec07-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bec07-140">End of server support</span></span><br/>    | <span data-ttu-id="bec07-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bec07-141">Windows Server 2008 R2</span></span><br/>                    |



 

