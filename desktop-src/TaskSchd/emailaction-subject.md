---
title: EmailAction. Subject (propiedad)
description: Para el scripting, obtiene o establece el asunto del mensaje de correo electrónico.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Propiedad de asunto Programador de tareas
- Propiedad Subject Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677215"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="f6368-106">EmailAction. Subject (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f6368-106">EmailAction.Subject property</span></span>

<span data-ttu-id="f6368-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="f6368-107">\[This object is no longer supported.</span></span> <span data-ttu-id="f6368-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="f6368-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="f6368-109">Para el scripting, obtiene o establece el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f6368-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="f6368-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f6368-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6368-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6368-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="f6368-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f6368-112">Property value</span></span>

<span data-ttu-id="f6368-113">Asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f6368-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6368-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6368-114">Remarks</span></span>

<span data-ttu-id="f6368-115">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="f6368-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="f6368-116">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6368-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="f6368-117">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6368-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="f6368-118">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="f6368-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6368-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6368-119">Requirements</span></span>



| <span data-ttu-id="f6368-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6368-120">Requirement</span></span> | <span data-ttu-id="f6368-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6368-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6368-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6368-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6368-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6368-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f6368-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6368-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6368-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6368-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6368-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f6368-126">End of client support</span></span><br/>    | <span data-ttu-id="f6368-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6368-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="f6368-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f6368-128">End of server support</span></span><br/>    | <span data-ttu-id="f6368-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6368-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f6368-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f6368-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6368-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f6368-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f6368-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6368-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6368-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6368-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6368-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6368-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6368-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="f6368-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="f6368-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f6368-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

