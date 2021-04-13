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
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS

Administración remota de Windows los cmdlets de PowerShell pueden administrar trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS). Para obtener más información acerca de la administración remota de BITS, consulte [clases]( /previous-versions//dd904507(v=vs.85))de proveedor bits [y proveedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

En los siguientes ejemplos se requiere el [proveedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider). El proveedor de BITS está disponible después de instalar el servidor BITS compacto. Para obtener información acerca de cómo instalar el servidor compacto, consulte la documentación del [servidor de bits Compact](bits-compact-server.md) .

1.  Cree un trabajo de transferencia de BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    El cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario para conectarse al equipo remoto y asigna las credenciales al objeto $cred.

    El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) crea el trabajo de transferencia de bits en Client1 creando una instancia de la clase [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) y usando la información de la tabla hash definida en el parámetro *Valueset* . El parámetro *Valueset* especifica la información necesaria para rellenar los parámetros del método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) . En el ejemplo anterior, el usuario establece el parámetro de *tipo* en 0 (descargar). El usuario también especifica el nombre de los archivos remotos y locales para el trabajo de descarga. Para obtener más información sobre cómo crear trabajos de transferencia de BITS y obtener información detallada sobre los parámetros, vea método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .

    El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) asigna el resultado a la variable $result.

    > [!Note]  
    > El carácter de acento grave ( \` ) se usa para indicar un salto de línea.

     

2.  Establezca la prioridad del trabajo de transferencia de BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    El cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cambia la prioridad del nuevo trabajo de transferencia de bits a 0 (**\_ \_ \_ primer plano de prioridad del trabajo de BG**). Para obtener más información sobre los niveles de prioridad, consulte la enumeración [**\_ \_ prioridad del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .

3.  Reanude el trabajo de transferencia de BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    El cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , que establece el estado del trabajo en 2 (reanudar el trabajo).

4.  Administrar el trabajo de transferencia de BITS.

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

    

    El ejemplo anterior es un script para sondear el estado del trabajo y realizar una acción basada en el estado. Se pueden realizar las siguientes acciones:

    -   Si $result. El estado es 4 **( \_ \_ \_ error de estado del trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y cancela el trabajo.
    -   Si $result. El estado es 5 **( \_ \_ \_ \_ error transitorio de estado de trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y cancela el trabajo.
    -   Si $result. El estado es 6 (se **\_ \_ \_ transfirió el estado del trabajo de BG**), el cmdlet [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) llama al método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) y establece el estado en completado.

    Para obtener más información sobre los Estados de trabajo, consulte la enumeración [**\_ \_ Estado del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
