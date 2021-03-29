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
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="22e96-103">Utilizar Windows PowerShell para crear trabajos de transferencia de BITS</span><span class="sxs-lookup"><span data-stu-id="22e96-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="22e96-104">Puede usar cmdlets de PowerShell para crear trabajos de transferencia de Servicio de transferencia inteligente en segundo plano (BITS) sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="22e96-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="22e96-105">En todos los ejemplos de este tema se usa el cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="22e96-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="22e96-106">Para usar el cmdlet, asegúrese de importar primero el módulo.</span><span class="sxs-lookup"><span data-stu-id="22e96-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="22e96-107">Para instalar el módulo, ejecute el siguiente comando: Import-Module BitsTransfer.</span><span class="sxs-lookup"><span data-stu-id="22e96-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="22e96-108">Para obtener más información, escriba **Get-Help Start-BitsTransfer** en el símbolo del sistema de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="22e96-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="22e96-109">Si usa cmdlets [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) desde un proceso que se ejecuta en un contexto no interactivo, como un servicio de Windows, es posible que no pueda agregar archivos a trabajos de bits, lo que puede dar lugar a un estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="22e96-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="22e96-110">Para que el trabajo continúe, la identidad que se usó para crear un trabajo de transferencia debe iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="22e96-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="22e96-111">Por ejemplo, al crear un trabajo de BITS en un script de PowerShell que se ejecutó como Programador de tareas trabajo, la transferencia de BITS nunca se completará a menos que la configuración de la tarea de Programador de tareas "ejecutar solo cuando el usuario haya iniciado sesión" esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="22e96-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="22e96-112">Para crear un trabajo de transferencia de BITS sincrónico</span><span class="sxs-lookup"><span data-stu-id="22e96-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="22e96-113">Para crear un trabajo de transferencia de BITS sincrónico con varios archivos</span><span class="sxs-lookup"><span data-stu-id="22e96-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="22e96-114">Para crear un trabajo de transferencia de BITS sincrónico y especificar las credenciales de un servidor remoto</span><span class="sxs-lookup"><span data-stu-id="22e96-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="22e96-115">Para crear un trabajo de transferencia de BITS sincrónico desde un archivo CSV</span><span class="sxs-lookup"><span data-stu-id="22e96-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="22e96-116">Para crear un trabajo de transferencia de BITS asincrónico</span><span class="sxs-lookup"><span data-stu-id="22e96-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="22e96-117">Para administrar sesiones remotas de PowerShell</span><span class="sxs-lookup"><span data-stu-id="22e96-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="22e96-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22e96-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="22e96-119">Para crear un trabajo de transferencia de BITS sincrónico</span><span class="sxs-lookup"><span data-stu-id="22e96-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="22e96-120">El carácter de acento grave ( \` ) se usa para indicar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="22e96-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="22e96-121">En el ejemplo anterior, los nombres locales y remotos del archivo se especifican en los parámetros de *origen* y de *destino* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="22e96-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="22e96-122">El símbolo del sistema vuelve a aparecer cuando la transferencia del archivo se completa o bien entra en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="22e96-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="22e96-123">El tipo de transferencia predeterminado es download.</span><span class="sxs-lookup"><span data-stu-id="22e96-123">The default transfer type is Download.</span></span> <span data-ttu-id="22e96-124">Cuando se cargan archivos en una ubicación HTTP, el parámetro *TransferType* debe establecerse en Upload.</span><span class="sxs-lookup"><span data-stu-id="22e96-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="22e96-125">Dado que la posición del parámetro se aplica al cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , no es necesario especificar los nombres de parámetro para los parámetros de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="22e96-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="22e96-126">Por lo tanto, este comando se puede simplificar como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="22e96-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="22e96-127">Para crear un trabajo de transferencia de BITS sincrónico con varios archivos</span><span class="sxs-lookup"><span data-stu-id="22e96-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="22e96-128">En el ejemplo anterior, el comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuevo trabajo de transferencia de bits.</span><span class="sxs-lookup"><span data-stu-id="22e96-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="22e96-129">Todos los archivos se agregan a este trabajo y se transfieren secuencialmente al cliente.</span><span class="sxs-lookup"><span data-stu-id="22e96-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="22e96-130">La ruta de acceso de destino no puede usar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="22e96-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="22e96-131">La ruta de acceso de destino admite directorios relativos, rutas de acceso raíz o directorios implícitos (es decir, el directorio actual).</span><span class="sxs-lookup"><span data-stu-id="22e96-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="22e96-132">No se puede cambiar el nombre de los archivos de destino mediante un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="22e96-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="22e96-133">Además, las direcciones URL HTTP y HTTPS no funcionan con caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="22e96-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="22e96-134">Los caracteres comodín solo son válidos para rutas UNC y directorios locales.</span><span class="sxs-lookup"><span data-stu-id="22e96-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="22e96-135">Para crear un trabajo de transferencia de BITS sincrónico y especificar las credenciales de un servidor remoto</span><span class="sxs-lookup"><span data-stu-id="22e96-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="22e96-136">En el ejemplo anterior, un usuario crea un trabajo de transferencia de BITS para descargar un archivo de un servidor que requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="22e96-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="22e96-137">Al usuario se le piden las credenciales y el parámetro *Credential* pasa un objeto Credential al cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="22e96-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="22e96-138">El usuario establece un Proxy explícito y el trabajo de transferencia de BITS solo usa los proxies definidos por el parámetro *ProxyList* .</span><span class="sxs-lookup"><span data-stu-id="22e96-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="22e96-139">El parámetro *displayName* proporciona un nombre para mostrar único al trabajo de transferencia de bits.</span><span class="sxs-lookup"><span data-stu-id="22e96-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="22e96-140">Para crear un trabajo de transferencia de BITS sincrónico desde un archivo CSV</span><span class="sxs-lookup"><span data-stu-id="22e96-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="22e96-141">" \| " Es el carácter de barra vertical.</span><span class="sxs-lookup"><span data-stu-id="22e96-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="22e96-142">En el ejemplo anterior, un usuario crea un trabajo de transferencia de BITS que carga varios archivos desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="22e96-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="22e96-143">El cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa las ubicaciones de los archivos de origen y de destino, y los canaliza al comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="22e96-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="22e96-144">El comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) crea un nuevo trabajo de transferencia de bits para cada archivo, agrega los archivos al trabajo y, a continuación, los transfiere secuencialmente al servidor.</span><span class="sxs-lookup"><span data-stu-id="22e96-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="22e96-145">El contenido del archivo Filelist.txt debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="22e96-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="22e96-146">Para crear un trabajo de transferencia de BITS asincrónico</span><span class="sxs-lookup"><span data-stu-id="22e96-146">To create an asynchronous BITS transfer job</span></span>


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



<span data-ttu-id="22e96-147">En el ejemplo anterior, el trabajo de transferencia de BITS se asignó a la variable $Job.</span><span class="sxs-lookup"><span data-stu-id="22e96-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="22e96-148">Los archivos se descargan secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="22e96-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="22e96-149">Una vez completado el trabajo de transferencia, los archivos estarán disponibles de inmediato.</span><span class="sxs-lookup"><span data-stu-id="22e96-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="22e96-150">Si $Job. JobState devuelve "transfiriendo", el objeto de $Job se envía al cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="22e96-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="22e96-151">Si $Job. JobState devuelve "error", el objeto de $Job se envía al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) para mostrar los errores.</span><span class="sxs-lookup"><span data-stu-id="22e96-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="22e96-152">Para administrar sesiones remotas de PowerShell</span><span class="sxs-lookup"><span data-stu-id="22e96-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="22e96-153">A partir de Windows 10, versión 1607, puede ejecutar cmdlets de PowerShell, BITSAdmin u otras aplicaciones que usan las [interfaces](bits-interfaces.md) de bits desde una línea de comandos remota de PowerShell conectada a otra máquina (física o virtual).</span><span class="sxs-lookup"><span data-stu-id="22e96-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="22e96-154">Esta funcionalidad no está disponible cuando se usa una línea de comandos de [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para una máquina virtual en la misma máquina física y no está disponible cuando se usan los cmdlets de WinRM.</span><span class="sxs-lookup"><span data-stu-id="22e96-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="22e96-155">Un trabajo de BITS creado desde una sesión remota de PowerShell se ejecuta en el contexto de la cuenta de usuario de la sesión y solo realizará el progreso cuando haya al menos una sesión de inicio de sesión local activa o una sesión de PowerShell remota asociada con esa cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="22e96-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="22e96-156">Puede usar PSSessions persistentes de PowerShell para ejecutar comandos remotos sin necesidad de mantener abierta una ventana de PowerShell para que cada trabajo siga progresando, como se describe en [conceptos básicos de PowerShell: administración remota](https://techgenix.com/remote-management-powershell-part1/).</span><span class="sxs-lookup"><span data-stu-id="22e96-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="22e96-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) crea una sesión de PowerShell remota persistente.</span><span class="sxs-lookup"><span data-stu-id="22e96-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="22e96-158">Una vez creados, los objetos PSSession se conservan en el equipo remoto hasta que se eliminan explícitamente.</span><span class="sxs-lookup"><span data-stu-id="22e96-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="22e96-159">Los trabajos de BITS iniciados en una sesión activa realizarán la transferencia de datos, incluso después de que el cliente se haya desconectado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="22e96-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="22e96-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) desconecta el equipo cliente de una sesión remota de PowerShell y el estado de la sesión continúa siendo mantenido por el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="22e96-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="22e96-161">Lo más importante es que los procesos de la sesión remota seguirán ejecutándose y los trabajos de BITS seguirán progresando.</span><span class="sxs-lookup"><span data-stu-id="22e96-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="22e96-162">El equipo cliente puede incluso reiniciarse o desactivarse después de llamar a Disconnect-PSSession.</span><span class="sxs-lookup"><span data-stu-id="22e96-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="22e96-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) vuelve a conectar el equipo cliente a una sesión remota activa de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="22e96-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="22e96-164">[Remove-PSSession anula](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) una sesión remota de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="22e96-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="22e96-165">En el ejemplo siguiente se muestra cómo usar PowerShell Remote para trabajar con trabajos de transferencia de BITS asincrónicos de un modo que permita al trabajo continuar progresando incluso cuando no esté conectado activamente a la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="22e96-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="22e96-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22e96-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22e96-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="22e96-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="22e96-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="22e96-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
