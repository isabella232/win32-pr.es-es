---
title: Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS
description: Administración remota de Windows los cmdlets de PowerShell pueden administrar trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538986"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="a32ab-103">Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="a32ab-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="a32ab-104">Administración remota de Windows los cmdlets de PowerShell pueden administrar trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="a32ab-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="a32ab-105">Para obtener más información acerca de la administración remota de BITS, consulte [clases]( /previous-versions//dd904507(v=vs.85))de proveedor bits [y proveedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="a32ab-106">En los siguientes ejemplos se requiere el [proveedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="a32ab-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="a32ab-107">El proveedor de BITS está disponible después de instalar el servidor BITS compacto.</span><span class="sxs-lookup"><span data-stu-id="a32ab-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="a32ab-108">Para obtener información acerca de cómo instalar el servidor compacto, consulte la documentación del [servidor de bits Compact](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="a32ab-109">Cree un trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="a32ab-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a32ab-110">El cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario para conectarse al equipo remoto y asigna las credenciales al objeto $cred.</span><span class="sxs-lookup"><span data-stu-id="a32ab-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="a32ab-111">El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crea el trabajo de transferencia de bits en Client1 creando una instancia de la clase [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) y usando la información de la tabla hash definida en el parámetro *Valueset* .</span><span class="sxs-lookup"><span data-stu-id="a32ab-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="a32ab-112">El parámetro *Valueset* especifica la información necesaria para rellenar los parámetros del método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="a32ab-113">En el ejemplo anterior, el usuario establece el parámetro de *tipo* en 0 (descargar).</span><span class="sxs-lookup"><span data-stu-id="a32ab-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="a32ab-114">El usuario también especifica el nombre de los archivos remotos y locales para el trabajo de descarga.</span><span class="sxs-lookup"><span data-stu-id="a32ab-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="a32ab-115">Para obtener más información sobre cómo crear trabajos de transferencia de BITS y obtener información detallada sobre los parámetros, vea método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="a32ab-116">El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) asigna el resultado a la variable $result.</span><span class="sxs-lookup"><span data-stu-id="a32ab-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="a32ab-117">El carácter de acento grave ( \` ) se usa para indicar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a32ab-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="a32ab-118">Establezca la prioridad del trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="a32ab-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a32ab-119">El cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cambia la prioridad del nuevo trabajo de transferencia de bits a 0 (**\_ \_ \_ primer plano de prioridad del trabajo de BG**).</span><span class="sxs-lookup"><span data-stu-id="a32ab-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="a32ab-120">Para obtener más información sobre los niveles de prioridad, consulte la enumeración [**\_ \_ prioridad del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="a32ab-121">Reanude el trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="a32ab-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="a32ab-122">El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , que establece el estado del trabajo en 2 (reanudar el trabajo).</span><span class="sxs-lookup"><span data-stu-id="a32ab-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="a32ab-123">Administrar el trabajo de transferencia de BITS.</span><span class="sxs-lookup"><span data-stu-id="a32ab-123">Manage the BITS transfer job.</span></span>

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    <span data-ttu-id="a32ab-124">El ejemplo anterior es un script para sondear el estado del trabajo y realizar una acción basada en el estado.</span><span class="sxs-lookup"><span data-stu-id="a32ab-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="a32ab-125">Se pueden realizar las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a32ab-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="a32ab-126">Si $result. El estado es 4 **( \_ \_ \_ error de estado del trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y cancela el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a32ab-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="a32ab-127">Si $result. El estado es 5 **( \_ \_ \_ \_ error transitorio de estado de trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y cancela el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a32ab-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="a32ab-128">Si $result. El estado es 6 (se **\_ \_ \_ transfirió el estado del trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y establece el estado en completado.</span><span class="sxs-lookup"><span data-stu-id="a32ab-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="a32ab-129">Para obtener más información sobre los Estados de trabajo, consulte la enumeración [**\_ \_ Estado del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .</span><span class="sxs-lookup"><span data-stu-id="a32ab-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a32ab-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a32ab-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a32ab-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a32ab-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="a32ab-132">Invoke-WsmanAction</span><span class="sxs-lookup"><span data-stu-id="a32ab-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="a32ab-133">Set-WsmanInstance</span><span class="sxs-lookup"><span data-stu-id="a32ab-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
