---
title: Propiedad EmailAction. BCC
description: En el caso de scripting, obtiene o establece las direcciones de correo electrónico que desea incluir en el mensaje de correo electrónico.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- Propiedad BCC Programador de tareas
- Propiedad BCC Programador de tareas, objeto EmailAction
- Programador de tareas objeto EmailAction, propiedad BCC
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bded5e88c236123832956ce42413352348ea535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686002"
---
# <a name="emailactionbcc-property"></a><span data-ttu-id="af40b-106">Propiedad EmailAction. BCC</span><span class="sxs-lookup"><span data-stu-id="af40b-106">EmailAction.Bcc property</span></span>

<span data-ttu-id="af40b-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="af40b-107">\[This object is no longer supported.</span></span> <span data-ttu-id="af40b-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="af40b-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="af40b-109">En el caso de scripting, obtiene o establece las direcciones de correo electrónico que desea incluir en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="af40b-109">For scripting, gets or sets the email address or addresses that you want to Bcc in the email message.</span></span>

<span data-ttu-id="af40b-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="af40b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="af40b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af40b-111">Syntax</span></span>


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a><span data-ttu-id="af40b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="af40b-112">Property value</span></span>

<span data-ttu-id="af40b-113">La dirección o direcciones de correo electrónico que desea incluir en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="af40b-113">The email address or addresses that you want to Bcc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af40b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af40b-114">Requirements</span></span>



| <span data-ttu-id="af40b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af40b-115">Requirement</span></span> | <span data-ttu-id="af40b-116">Value</span><span class="sxs-lookup"><span data-stu-id="af40b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af40b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af40b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af40b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af40b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af40b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af40b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af40b-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af40b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af40b-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="af40b-121">End of client support</span></span><br/>    | <span data-ttu-id="af40b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af40b-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="af40b-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="af40b-123">End of server support</span></span><br/>    | <span data-ttu-id="af40b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af40b-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="af40b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="af40b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="af40b-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af40b-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af40b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af40b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af40b-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af40b-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af40b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="af40b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af40b-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="af40b-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="af40b-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="af40b-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

