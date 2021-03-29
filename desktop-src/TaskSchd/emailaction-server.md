---
title: EmailAction. Server (propiedad)
description: En el caso de scripting, obtiene o establece el nombre del servidor SMTP que se usa para enviar correo electrónico desde.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Programador de tareas de propiedades de servidor
- Propiedad Server Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad de servidor
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359752"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="acff2-106">EmailAction. Server (propiedad)</span><span class="sxs-lookup"><span data-stu-id="acff2-106">EmailAction.Server property</span></span>

<span data-ttu-id="acff2-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="acff2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="acff2-108">Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="acff2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="acff2-109">En el caso de scripting, obtiene o establece el nombre del servidor SMTP que se usa para enviar correo electrónico desde.</span><span class="sxs-lookup"><span data-stu-id="acff2-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="acff2-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="acff2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="acff2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acff2-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="acff2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="acff2-112">Property value</span></span>

<span data-ttu-id="acff2-113">El nombre del servidor que se usa para enviar correo electrónico desde.</span><span class="sxs-lookup"><span data-stu-id="acff2-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="acff2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acff2-114">Remarks</span></span>

<span data-ttu-id="acff2-115">Asegúrese de que el servidor SMTP que envía el correo electrónico está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="acff2-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="acff2-116">El correo electrónico se envía mediante la autenticación NTLM para los servidores SMTP de Windows, lo que significa que las credenciales de seguridad utilizadas para ejecutar la tarea también deben tener privilegios en el servidor SMTP para enviar un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="acff2-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="acff2-117">Si el servidor SMTP no es un servidor basado en Windows, se enviará el correo electrónico si el servidor permite el acceso anónimo.</span><span class="sxs-lookup"><span data-stu-id="acff2-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="acff2-118">Para obtener información acerca de la configuración del servidor SMTP, consulte [configuración](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)del servidor SMTP y, para obtener información acerca de la administración de la configuración del servidor SMTP, consulte [Administración de SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="acff2-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="acff2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acff2-119">Requirements</span></span>



| <span data-ttu-id="acff2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="acff2-120">Requirement</span></span> | <span data-ttu-id="acff2-121">Value</span><span class="sxs-lookup"><span data-stu-id="acff2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acff2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acff2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="acff2-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="acff2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="acff2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acff2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="acff2-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="acff2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acff2-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="acff2-126">End of client support</span></span><br/>    | <span data-ttu-id="acff2-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="acff2-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="acff2-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="acff2-128">End of server support</span></span><br/>    | <span data-ttu-id="acff2-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="acff2-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="acff2-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="acff2-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="acff2-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="acff2-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="acff2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acff2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acff2-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acff2-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acff2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="acff2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acff2-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="acff2-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="acff2-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="acff2-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

