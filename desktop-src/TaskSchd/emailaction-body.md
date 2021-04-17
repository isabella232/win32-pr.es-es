---
title: EmailAction. Body (propiedad)
description: En el caso de scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Propiedad del cuerpo Programador de tareas
- Propiedad Body Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676781"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="dbc2c-106">EmailAction. Body (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dbc2c-106">EmailAction.Body property</span></span>

<span data-ttu-id="dbc2c-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-107">\[This object is no longer supported.</span></span> <span data-ttu-id="dbc2c-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="dbc2c-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="dbc2c-109">En el caso de scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="dbc2c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc2c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbc2c-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="dbc2c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dbc2c-112">Property value</span></span>

<span data-ttu-id="dbc2c-113">El cuerpo del correo electrónico que contiene el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc2c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbc2c-114">Remarks</span></span>

<span data-ttu-id="dbc2c-115">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="dbc2c-116">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="dbc2c-117">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="dbc2c-118">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="dbc2c-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc2c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc2c-119">Requirements</span></span>



| <span data-ttu-id="dbc2c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc2c-120">Requirement</span></span> | <span data-ttu-id="dbc2c-121">Value</span><span class="sxs-lookup"><span data-stu-id="dbc2c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc2c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbc2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc2c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dbc2c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dbc2c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbc2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc2c-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbc2c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbc2c-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dbc2c-126">End of client support</span></span><br/>    | <span data-ttu-id="dbc2c-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbc2c-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="dbc2c-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="dbc2c-128">End of server support</span></span><br/>    | <span data-ttu-id="dbc2c-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbc2c-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="dbc2c-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dbc2c-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="dbc2c-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dbc2c-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dbc2c-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbc2c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbc2c-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbc2c-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc2c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbc2c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc2c-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="dbc2c-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="dbc2c-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="dbc2c-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

