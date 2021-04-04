---
title: Propiedad EmailAction.Cc
description: En el caso de scripting, obtiene o establece la dirección o direcciones de correo electrónico que desea CC en el mensaje de correo electrónico.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Propiedad CC Programador de tareas
- Propiedad CC Programador de tareas, objeto EmailAction
- Objeto EmailAction Programador de tareas, propiedad CC
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802575"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="de51c-106">Propiedad EmailAction.Cc</span><span class="sxs-lookup"><span data-stu-id="de51c-106">EmailAction.Cc property</span></span>

<span data-ttu-id="de51c-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="de51c-107">\[This object is no longer supported.</span></span> <span data-ttu-id="de51c-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="de51c-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="de51c-109">En el caso de scripting, obtiene o establece la dirección o direcciones de correo electrónico que desea CC en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="de51c-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="de51c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="de51c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de51c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de51c-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="de51c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de51c-112">Property value</span></span>

<span data-ttu-id="de51c-113">La dirección o direcciones de correo electrónico que desea incluir en CC en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="de51c-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de51c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de51c-114">Requirements</span></span>



| <span data-ttu-id="de51c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="de51c-115">Requirement</span></span> | <span data-ttu-id="de51c-116">Value</span><span class="sxs-lookup"><span data-stu-id="de51c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de51c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de51c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de51c-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="de51c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de51c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de51c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de51c-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="de51c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de51c-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="de51c-121">End of client support</span></span><br/>    | <span data-ttu-id="de51c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de51c-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="de51c-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="de51c-123">End of server support</span></span><br/>    | <span data-ttu-id="de51c-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de51c-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="de51c-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de51c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="de51c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de51c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de51c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de51c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de51c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de51c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de51c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="de51c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de51c-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="de51c-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="de51c-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="de51c-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

