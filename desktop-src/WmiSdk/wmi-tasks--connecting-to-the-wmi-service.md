---
description: Para obtener datos de WMI, en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un espacio de nombres específico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Tareas WMI: conectarse al servicio WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706149"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="d829c-103">Tareas WMI: conectarse al servicio WMI</span><span class="sxs-lookup"><span data-stu-id="d829c-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="d829c-104">Para obtener datos de WMI, en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un [*espacio de nombres*](gloss-n.md)específico.</span><span class="sxs-lookup"><span data-stu-id="d829c-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="d829c-105">En la mayoría de los casos, puede usar la conexión de [moniker](creating-a-wmi-script.md) abreviada o la conexión del [**localizador**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="d829c-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="d829c-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d829c-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="d829c-107">Las conexiones remotas requieren una configuración adecuada para el Firewall de Windows y DCOM.</span><span class="sxs-lookup"><span data-stu-id="d829c-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="d829c-108">Para obtener más información, vea [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) y [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="d829c-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="d829c-109">A partir de Windows Vista, el control de cuentas de usuario (UAC) puede afectar al acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="d829c-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="d829c-110">Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d829c-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="d829c-111">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="d829c-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="d829c-112">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d829c-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="d829c-113">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="d829c-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="d829c-114">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="d829c-114">**To run a script**</span></span>

1.  <span data-ttu-id="d829c-115">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="d829c-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="d829c-116">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="d829c-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="d829c-117">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="d829c-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="d829c-118">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="d829c-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="d829c-119">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="d829c-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="d829c-120">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="d829c-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="d829c-121">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="d829c-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="d829c-122">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="d829c-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="d829c-123">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="d829c-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="d829c-124">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="d829c-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d829c-125">Cómo...</span><span class="sxs-lookup"><span data-stu-id="d829c-125">How do I...</span></span></th>
<th><span data-ttu-id="d829c-126">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="d829c-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d829c-127">... ¿conectarse a un equipo remoto mediante WMI?</span><span class="sxs-lookup"><span data-stu-id="d829c-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="d829c-128">Especifique una de las siguientes como parte de la cadena de conexión de <a href="constructing-a-moniker-string.md">moniker</a> :</span><span class="sxs-lookup"><span data-stu-id="d829c-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="d829c-129">Un nombre de equipo NetBIOS, como &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="d829c-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="d829c-130">Un nombre de dominio completo, como &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="d829c-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="d829c-131">Una dirección IPv4, como &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="d829c-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="d829c-132">A partir de Windows Vista, puede especificar una dirección IPv6 si el equipo de destino y el equipo desde el que está realizando la conexión ejecutan IPv6.</span><span class="sxs-lookup"><span data-stu-id="d829c-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="d829c-133">Para obtener más información, vea <a href="connecting-to-wmi-on-a-remote-computer.md">conectarse a WMI en un equipo remoto</a> y <a href="ipv6-and-ipv4-support-in-wmi.md">compatibilidad con IPv6 e IPv4 en WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="d829c-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d829c-134">VB</span><span class="sxs-lookup"><span data-stu-id="d829c-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d829c-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d829c-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d829c-136">... ¿ejecutar un script de WMI en credenciales alternativas?</span><span class="sxs-lookup"><span data-stu-id="d829c-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="d829c-137">Use el método <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> o <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> en C++ e incluya el nombre de usuario y la contraseña adecuados.</span><span class="sxs-lookup"><span data-stu-id="d829c-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="d829c-138">No se pueden cambiar las credenciales al conectarse al equipo local.</span><span class="sxs-lookup"><span data-stu-id="d829c-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="d829c-139">Para obtener más información, vea <a href="creating-a-wmi-script.md">crear un script WMI</a> y <a href="connecting-to-wmi-on-a-remote-computer.md">conectarse a WMI en un equipo remoto</a>.</span><span class="sxs-lookup"><span data-stu-id="d829c-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d829c-140">VB</span><span class="sxs-lookup"><span data-stu-id="d829c-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d829c-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d829c-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d829c-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d829c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d829c-143">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d829c-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="d829c-144">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="d829c-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="d829c-145">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="d829c-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
