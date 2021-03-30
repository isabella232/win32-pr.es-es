---
title: Propiedad EmailAction. Attachments
description: En el caso de scripting, obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Programador de tareas de propiedades de datos adjuntos
- Propiedad Attachments Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802576"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="5bf5b-106">Propiedad EmailAction. Attachments</span><span class="sxs-lookup"><span data-stu-id="5bf5b-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="5bf5b-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-107">\[This object is no longer supported.</span></span> <span data-ttu-id="5bf5b-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="5bf5b-109">En el caso de scripting, obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="5bf5b-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf5b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bf5b-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="5bf5b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5bf5b-112">Property value</span></span>

<span data-ttu-id="5bf5b-113">Una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf5b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bf5b-114">Remarks</span></span>

<span data-ttu-id="5bf5b-115">Un máximo de ocho datos adjuntos puede estar en la matriz de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf5b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bf5b-116">Requirements</span></span>



| <span data-ttu-id="5bf5b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf5b-117">Requirement</span></span> | <span data-ttu-id="5bf5b-118">Value</span><span class="sxs-lookup"><span data-stu-id="5bf5b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf5b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bf5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf5b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5bf5b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bf5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf5b-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bf5b-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5bf5b-123">End of client support</span></span><br/>    | <span data-ttu-id="5bf5b-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5bf5b-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="5bf5b-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5bf5b-125">End of server support</span></span><br/>    | <span data-ttu-id="5bf5b-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5bf5b-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="5bf5b-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5bf5b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="5bf5b-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5bf5b-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5bf5b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5bf5b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bf5b-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bf5b-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf5b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bf5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf5b-132">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="5bf5b-133">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5bf5b-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

