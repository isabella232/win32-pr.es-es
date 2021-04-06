---
title: Propiedad EmailAction. ReplyTo
description: Para el scripting, obtiene o establece la dirección de correo electrónico a la que desea responder.
ms.assetid: 2b267e6e-c0c9-42ca-bc4a-cc18af5bcb9c
keywords:
- Propiedad ReplyTo Programador de tareas
- Propiedad ReplyTo Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad ReplyTo
topic_type:
- apiref
api_name:
- EmailAction.ReplyTo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ed1fd84245e4d938d329f0e9773271efec45b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905322"
---
# <a name="emailactionreplyto-property"></a><span data-ttu-id="983d2-106">Propiedad EmailAction. ReplyTo</span><span class="sxs-lookup"><span data-stu-id="983d2-106">EmailAction.ReplyTo property</span></span>

<span data-ttu-id="983d2-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="983d2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="983d2-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="983d2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="983d2-109">Para el scripting, obtiene o establece la dirección de correo electrónico a la que desea responder.</span><span class="sxs-lookup"><span data-stu-id="983d2-109">For scripting, gets or sets the email address that you want to reply to.</span></span>

<span data-ttu-id="983d2-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="983d2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="983d2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="983d2-111">Syntax</span></span>


```VB
EmailAction.ReplyTo As String
```



## <a name="property-value"></a><span data-ttu-id="983d2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="983d2-112">Property value</span></span>

<span data-ttu-id="983d2-113">La dirección de correo electrónico a la que desea responder.</span><span class="sxs-lookup"><span data-stu-id="983d2-113">The email address that you want to reply to.</span></span>

## <a name="requirements"></a><span data-ttu-id="983d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="983d2-114">Requirements</span></span>



| <span data-ttu-id="983d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="983d2-115">Requirement</span></span> | <span data-ttu-id="983d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="983d2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="983d2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="983d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="983d2-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="983d2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="983d2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="983d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="983d2-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="983d2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="983d2-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="983d2-121">End of client support</span></span><br/>    | <span data-ttu-id="983d2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="983d2-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="983d2-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="983d2-123">End of server support</span></span><br/>    | <span data-ttu-id="983d2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="983d2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="983d2-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="983d2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="983d2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="983d2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="983d2-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="983d2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="983d2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="983d2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983d2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="983d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983d2-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="983d2-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="983d2-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="983d2-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

