---
title: Propiedad EmailAction.To
description: En el caso de scripting, obtiene o establece las direcciones de correo electrónico a las que desea enviar el correo electrónico.
ms.assetid: 592ae58c-a519-4f1b-8976-315befa77e1e
keywords:
- A la propiedad Programador de tareas
- A la propiedad Programador de tareas, objeto EmailAction
- Objeto EmailAction Programador de tareas, a propiedad
topic_type:
- apiref
api_name:
- EmailAction.To
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a7d09a0962fa4fbd680341ba7f046ef4a5eacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491104"
---
# <a name="emailactionto-property"></a><span data-ttu-id="1dc56-106">Propiedad EmailAction.To</span><span class="sxs-lookup"><span data-stu-id="1dc56-106">EmailAction.To property</span></span>

<span data-ttu-id="1dc56-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="1dc56-107">\[This object is no longer supported.</span></span> <span data-ttu-id="1dc56-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="1dc56-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="1dc56-109">En el caso de scripting, obtiene o establece las direcciones de correo electrónico a las que desea enviar el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1dc56-109">For scripting, gets or sets the email address or addresses that you want to send the email to.</span></span>

<span data-ttu-id="1dc56-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1dc56-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc56-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dc56-111">Syntax</span></span>


```VB
EmailAction.To As String
```



## <a name="property-value"></a><span data-ttu-id="1dc56-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1dc56-112">Property value</span></span>

<span data-ttu-id="1dc56-113">La dirección o direcciones de correo electrónico a las que desea enviar el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1dc56-113">The email address or addresses that you want to send the email to.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc56-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc56-114">Requirements</span></span>



| <span data-ttu-id="1dc56-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc56-115">Requirement</span></span> | <span data-ttu-id="1dc56-116">Value</span><span class="sxs-lookup"><span data-stu-id="1dc56-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc56-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc56-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc56-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc56-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1dc56-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc56-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc56-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc56-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1dc56-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1dc56-121">End of client support</span></span><br/>    | <span data-ttu-id="1dc56-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1dc56-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="1dc56-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1dc56-123">End of server support</span></span><br/>    | <span data-ttu-id="1dc56-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1dc56-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="1dc56-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1dc56-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1dc56-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1dc56-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1dc56-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1dc56-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc56-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc56-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc56-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dc56-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc56-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="1dc56-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="1dc56-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="1dc56-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

