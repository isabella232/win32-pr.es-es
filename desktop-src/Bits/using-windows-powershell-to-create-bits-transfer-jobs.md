---
title: Utilizar Windows PowerShell para crear trabajos de transferencia de BITS
description: Puede usar cmdlets de PowerShell para crear trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS) sincrónicos y asincrónicos.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807531"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Utilizar Windows PowerShell para crear trabajos de transferencia de BITS

Puede usar cmdlets de PowerShell para crear trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS) sincrónicos y asincrónicos.

En todos los ejemplos de este tema se usa el cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Para usar el cmdlet, asegúrese de importar primero el módulo. Para instalar el módulo, ejecute el siguiente comando: Import-Module BitsTransfer. Para obtener más información, escriba **Get-Help Start-BitsTransfer** en el símbolo del sistema de PowerShell.

> [!IMPORTANT]
>
> Si usa cmdlets [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) desde un proceso que se ejecuta en un contexto no interactivo, como un servicio de Windows, es posible que no pueda agregar archivos a trabajos de bits, lo que puede dar lugar a un estado suspendido. Para que el trabajo continúe, la identidad que se usó para crear un trabajo de transferencia debe iniciar sesión. Por ejemplo, al crear un trabajo de BITS en un script de PowerShell que se ejecutó como Programador de tareas trabajo, la transferencia de BITS nunca se completará a menos que la configuración de la tarea de Programador de tareas "ejecutar solo cuando el usuario haya iniciado sesión" esté habilitada.

 

-   [Para crear un trabajo de transferencia de BITS sincrónico](#to-create-a-synchronous-bits-transfer-job)
-   [Para crear un trabajo de transferencia de BITS sincrónico con varios archivos](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [Para crear un trabajo de transferencia de BITS sincrónico y especificar las credenciales de un servidor remoto](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [Para crear un trabajo de transferencia de BITS sincrónico desde un archivo CSV](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [Para crear un trabajo de transferencia de BITS asincrónico](#to-create-an-asynchronous-bits-transfer-job)
-   [Para administrar sesiones remotas de PowerShell](#to-manage-powershell-remote-sessions)
-   [Temas relacionados](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>Para crear un trabajo de transferencia de BITS sincrónico


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> El carácter de acento grave ( \` ) se usa para indicar un salto de línea.

 

En el ejemplo anterior, los nombres locales y remotos del archivo se especifican en los parámetros de *origen* y de *destino* , respectivamente. El símbolo del sistema vuelve a aparecer cuando la transferencia del archivo se completa o bien entra en un estado de error.

El tipo de transferencia predeterminado es download. Cuando se cargan archivos en una ubicación HTTP, el parámetro *TransferType* debe establecerse en Upload.

Dado que la posición del parámetro se aplica al cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , no es necesario especificar los nombres de parámetro para los parámetros de origen y de destino. Por lo tanto, este comando se puede simplificar como se indica a continuación.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>Para crear un trabajo de transferencia de BITS sincrónico con varios archivos


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



En el ejemplo anterior, el comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuevo trabajo de transferencia de bits. Todos los archivos se agregan a este trabajo y se transfieren secuencialmente al cliente.

> [!Note]  
> La ruta de acceso de destino no puede usar caracteres comodín. La ruta de acceso de destino admite directorios relativos, rutas de acceso raíz o directorios implícitos (es decir, el directorio actual). No se puede cambiar el nombre de los archivos de destino mediante un carácter comodín. Además, las direcciones URL HTTP y HTTPS no funcionan con caracteres comodín. Los caracteres comodín solo son válidos para rutas UNC y directorios locales.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>Para crear un trabajo de transferencia de BITS sincrónico y especificar las credenciales de un servidor remoto


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



En el ejemplo anterior, un usuario crea un trabajo de transferencia de BITS para descargar un archivo de un servidor que requiere autenticación. Al usuario se le piden las credenciales y el parámetro *Credential* pasa un objeto Credential al cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . El usuario establece un Proxy explícito y el trabajo de transferencia de BITS solo usa los proxies definidos por el parámetro *ProxyList* . El parámetro *displayName* proporciona un nombre para mostrar único al trabajo de transferencia de bits.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>Para crear un trabajo de transferencia de BITS sincrónico desde un archivo CSV


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> " \| " Es el carácter de barra vertical.

 

En el ejemplo anterior, un usuario crea un trabajo de transferencia de BITS que carga varios archivos desde un cliente. El cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa las ubicaciones de los archivos de origen y de destino, y los canaliza al comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . El comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuevo trabajo de transferencia de bits para cada archivo, agrega los archivos al trabajo y, a continuación, los transfiere secuencialmente al servidor.

El contenido del archivo Filelist.txt debe tener el formato siguiente:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>Para crear un trabajo de transferencia de BITS asincrónico


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



En el ejemplo anterior, el trabajo de transferencia de BITS se asignó a la variable $Job. Los archivos se descargan secuencialmente. Una vez completado el trabajo de transferencia, los archivos estarán disponibles de inmediato. Si $Job. JobState devuelve "transfiriendo", el objeto de $Job se envía al cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .

Si $Job. JobState devuelve "error", el objeto de $Job se envía al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) para mostrar los errores.

## <a name="to-manage-powershell-remote-sessions"></a>Para administrar sesiones remotas de PowerShell

A partir de Windows 10, versión 1607, puede ejecutar cmdlets de PowerShell, BITSAdmin u otras aplicaciones que usan las [interfaces](bits-interfaces.md) de bits desde una línea de comandos remota de PowerShell conectada a otra máquina (física o virtual). Esta funcionalidad no está disponible cuando se usa una línea de comandos de [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para una máquina virtual en la misma máquina física y no está disponible cuando se usan los cmdlets de WinRM.

Un trabajo de BITS creado desde una sesión remota de PowerShell se ejecuta en el contexto de la cuenta de usuario de la sesión y solo realizará el progreso cuando haya al menos una sesión de inicio de sesión local activa o una sesión de PowerShell remota asociada con esa cuenta de usuario. Puede usar PSSessions persistentes de PowerShell para ejecutar comandos remotos sin necesidad de mantener abierta una ventana de PowerShell para que cada trabajo siga progresando, como se describe en [conceptos básicos de PowerShell: administración remota](https://techgenix.com/remote-management-powershell-part1/).

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crea una sesión de PowerShell remota persistente. Una vez creados, los objetos PSSession se conservan en el equipo remoto hasta que se eliminan explícitamente. Los trabajos de BITS iniciados en una sesión activa realizarán la transferencia de datos, incluso después de que el cliente se haya desconectado de la sesión.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) desconecta el equipo cliente de una sesión remota de PowerShell y el estado de la sesión continúa siendo mantenido por el equipo remoto. Lo más importante es que los procesos de la sesión remota seguirán ejecutándose y los trabajos de BITS seguirán progresando. El equipo cliente puede incluso reiniciarse o desactivarse después de llamar a Disconnect-PSSession.
-   [Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) vuelve a conectar el equipo cliente a una sesión remota activa de PowerShell.
-   [Remove-PSSession anula](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) una sesión remota de PowerShell.

En el ejemplo siguiente se muestra cómo usar PowerShell Remote para trabajar con trabajos de transferencia de BITS asincrónicos de un modo que permita al trabajo continuar progresando incluso cuando no esté conectado activamente a la sesión remota.


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
