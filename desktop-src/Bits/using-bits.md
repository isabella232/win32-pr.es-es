---
title: Usar BITS
description: Usar BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, tareas
- BITS de transferencia de archivos
- Uso de BITS bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656389"
---
# <a name="using-bits"></a><span data-ttu-id="8f669-107">Usar BITS</span><span class="sxs-lookup"><span data-stu-id="8f669-107">Using BITS</span></span>

<span data-ttu-id="8f669-108">En los pasos siguientes se muestra cómo realizar una transferencia de archivos mediante las  [interfaces](bits-interfaces.md)de servicio de transferencia inteligente en segundo plano (bits).</span><span class="sxs-lookup"><span data-stu-id="8f669-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="8f669-109">**Para realizar una transferencia de archivos**</span><span class="sxs-lookup"><span data-stu-id="8f669-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="8f669-110">Conectarse al servicio BITS</span><span class="sxs-lookup"><span data-stu-id="8f669-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="8f669-111">Crear un trabajo de transferencia</span><span class="sxs-lookup"><span data-stu-id="8f669-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="8f669-112">Agregar archivos al trabajo</span><span class="sxs-lookup"><span data-stu-id="8f669-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="8f669-113">Inicio del trabajo</span><span class="sxs-lookup"><span data-stu-id="8f669-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="8f669-114">Determinar si los BITS transfirieron correctamente los archivos</span><span class="sxs-lookup"><span data-stu-id="8f669-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="8f669-115">Completar el trabajo</span><span class="sxs-lookup"><span data-stu-id="8f669-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="8f669-116">En los pasos anteriores se muestra cómo transferir archivos con los valores de propiedad predeterminados de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="8f669-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="8f669-117">Puede cambiar el comportamiento predeterminado cambiando uno o varios de los valores de propiedad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="8f669-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="8f669-118">Por ejemplo, puede cambiar la prioridad con la que se procesa el trabajo en relación con otros trabajos de la cola, especificar su propia configuración de proxy y registrarse para recibir la notificación de eventos cuando BITS haya transferido los archivos.</span><span class="sxs-lookup"><span data-stu-id="8f669-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="8f669-119">Para obtener más información, vea [establecer y recuperar las propiedades de un trabajo](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="8f669-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="8f669-120">Windows PowerShell proporciona un mecanismo sencillo para administrar muchas tareas de BITS.</span><span class="sxs-lookup"><span data-stu-id="8f669-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="8f669-121">Esta sección contiene los siguientes temas que muestran cómo usar los cmdlets de Windows PowerShell con BITS:</span><span class="sxs-lookup"><span data-stu-id="8f669-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="8f669-122">Uso de Windows PowerShell para crear trabajos de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="8f669-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="8f669-123">Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="8f669-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="8f669-124">Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact</span><span class="sxs-lookup"><span data-stu-id="8f669-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="8f669-125">A partir de Windows 10, versión 1607, también puede ejecutar cmdlets de PowerShell y usar BITSAdmin u otras aplicaciones que usan las [interfaces](bits-interfaces.md) de bits desde una línea de comandos remota de PowerShell conectada a otra máquina (física o virtual).</span><span class="sxs-lookup"><span data-stu-id="8f669-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="8f669-126">Esta funcionalidad no está disponible cuando se usa una línea de comandos de [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para una máquina virtual en la misma máquina física y no está disponible cuando se usan los cmdlets de WinRM.</span><span class="sxs-lookup"><span data-stu-id="8f669-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="8f669-127">Un trabajo de BITS creado a partir de una sesión remota de PowerShell se ejecutará en el contexto de la cuenta de usuario de la sesión y solo progresará cuando haya al menos una sesión de inicio de sesión local activa o una sesión de PowerShell remota asociada con esa cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f669-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="8f669-128">Para obtener más información, vea [para administrar sesiones remotas de PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="8f669-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="8f669-129">Esta sección también contiene los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f669-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="8f669-130">Prácticas recomendadas al usar BITS</span><span class="sxs-lookup"><span data-stu-id="8f669-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="8f669-131">Enumerar trabajos en la cola de transferencia</span><span class="sxs-lookup"><span data-stu-id="8f669-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="8f669-132">Enumerar archivos en un trabajo</span><span class="sxs-lookup"><span data-stu-id="8f669-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="8f669-133">Control de errores</span><span class="sxs-lookup"><span data-stu-id="8f669-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="8f669-134">Recuperar la respuesta de un trabajo de carga y respuesta</span><span class="sxs-lookup"><span data-stu-id="8f669-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="8f669-135">Para ver el código de ejemplo que usa las interfaces de BITS, vea [ejemplos y herramientas de bits](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8f669-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 