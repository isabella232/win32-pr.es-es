---
title: Propiedad EmailAction. HeaderFields
description: En el caso de scripting, obtiene o establece la información de encabezado en el correo electrónico que desea enviar.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Programador de tareas de la propiedad HeaderFields
- Programador de tareas de la propiedad HeaderFields, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad HeaderFields
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905323"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="61788-106">Propiedad EmailAction. HeaderFields</span><span class="sxs-lookup"><span data-stu-id="61788-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="61788-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="61788-107">\[This object is no longer supported.</span></span> <span data-ttu-id="61788-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="61788-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="61788-109">En el caso de scripting, obtiene o establece la información de encabezado en el correo electrónico que desea enviar.</span><span class="sxs-lookup"><span data-stu-id="61788-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="61788-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="61788-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="61788-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61788-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="61788-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="61788-112">Property value</span></span>

<span data-ttu-id="61788-113">La información del encabezado en el correo electrónico que desea enviar.</span><span class="sxs-lookup"><span data-stu-id="61788-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="61788-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61788-114">Requirements</span></span>



| <span data-ttu-id="61788-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="61788-115">Requirement</span></span> | <span data-ttu-id="61788-116">Value</span><span class="sxs-lookup"><span data-stu-id="61788-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61788-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61788-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61788-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61788-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="61788-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61788-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61788-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="61788-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61788-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="61788-121">End of client support</span></span><br/>    | <span data-ttu-id="61788-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61788-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="61788-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="61788-123">End of server support</span></span><br/>    | <span data-ttu-id="61788-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61788-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="61788-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="61788-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="61788-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61788-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61788-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61788-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61788-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61788-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61788-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="61788-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61788-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="61788-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="61788-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="61788-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

