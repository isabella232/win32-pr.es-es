---
description: Conexión a WMI de forma remota con PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Conexión a WMI de forma remota con PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812662"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="124fc-103">Conexión a WMI de forma remota con PowerShell</span><span class="sxs-lookup"><span data-stu-id="124fc-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="124fc-104">Windows PowerShell proporciona un mecanismo sencillo para conectarse a Instrumental de administración de Windows (WMI) en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="124fc-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="124fc-105">Las conexiones remotas en WMI se ven afectadas por el [firewall de Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), la configuración de DCOM y el control de [cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="124fc-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="124fc-106">Para obtener más información acerca de la configuración de conexiones remotas, consulte [conectarse a WMI de forma remota a partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="124fc-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="124fc-107">Los ejemplos de este tema se basan en los VBScripts de la [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="124fc-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="124fc-108">En todos los ejemplos de este tema se usa el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="124fc-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="124fc-109">Para obtener más información, vea [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="124fc-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="124fc-110">Ejemplos de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="124fc-110">Windows PowerShell examples</span></span>

<span data-ttu-id="124fc-111">Al crear una conexión a un equipo remoto, un usuario puede especificar la información de conexión, como el nombre del equipo remoto, las credenciales y el nivel de autenticación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="124fc-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="124fc-112">En los siguientes ejemplos se muestra cómo conectarse a un equipo remoto mediante el uso de diferentes conjuntos de credenciales y cómo obtener acceso a la información de WMI.</span><span class="sxs-lookup"><span data-stu-id="124fc-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="124fc-113">En el siguiente ejemplo de Windows PowerShell se muestra cómo establecer el nivel de suplantación:</span><span class="sxs-lookup"><span data-stu-id="124fc-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="124fc-114">En el ejemplo anterior, el usuario se conecta a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con las que han iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="124fc-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="124fc-115">El usuario también solicitó el uso de la suplantación.</span><span class="sxs-lookup"><span data-stu-id="124fc-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="124fc-116">A diferencia del ejemplo de VBScript original, no se necesita una cadena de moniker porque el nivel de suplantación se establece mediante la propiedad "Impersonation".</span><span class="sxs-lookup"><span data-stu-id="124fc-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="124fc-117">De forma predeterminada, el nivel de suplantación se establece en 3 (suplantar).</span><span class="sxs-lookup"><span data-stu-id="124fc-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="124fc-118">En el ejemplo se enumeran todas las instancias de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que se ejecutan en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="124fc-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="124fc-119">Debe especificar el espacio de nombres WMI al que se conectará en el equipo remoto porque es posible que el espacio de nombres predeterminado no sea el mismo en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="124fc-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="124fc-120">En el siguiente ejemplo de Windows PowerShell se muestra cómo conectarse a un equipo remoto con credenciales diferentes y establecer el nivel de suplantación en 3, que es suplantar:</span><span class="sxs-lookup"><span data-stu-id="124fc-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="124fc-121">En el ejemplo anterior, el nombre del equipo se asignó a la variable $Computer.</span><span class="sxs-lookup"><span data-stu-id="124fc-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="124fc-122">El usuario se conecta a un equipo remoto mediante el uso de credenciales específicas (dominio y nombre de usuario) y solicita la suplantación para el nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="124fc-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="124fc-123">El carácter de acento grave ( \` ) se usa para indicar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="124fc-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="124fc-124">Es equivalente al carácter de subrayado ( \_ ) en VBScript.</span><span class="sxs-lookup"><span data-stu-id="124fc-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="124fc-125">El siguiente ejemplo de Windows PowerShell se conecta a un grupo de equipos remotos en el mismo dominio mediante la creación de una matriz de nombres de equipo remoto y, a continuación, la visualización de los nombres de los dispositivos Plug and Play (instancias de [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) en cada equipo:</span><span class="sxs-lookup"><span data-stu-id="124fc-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> <span data-ttu-id="124fc-126">Para ejecutar el script de Windows PowerShell anterior, debe ser administrador en los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="124fc-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="124fc-127">Además, en relación con el ejemplo anterior, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="124fc-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="124fc-128">Los nombres de equipo de la matriz deben ir entre comillas porque son cadenas.</span><span class="sxs-lookup"><span data-stu-id="124fc-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="124fc-129">Los objetos devueltos por [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) se asignan a la variable $ColItems.</span><span class="sxs-lookup"><span data-stu-id="124fc-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="124fc-130">El operador \[ \] de intervalo limita la lista de dispositivos Plug and Play a instancias 48.</span><span class="sxs-lookup"><span data-stu-id="124fc-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="124fc-131">Para obtener más información, vea [About \_ Operators](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="124fc-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="124fc-132">" \| " Es el carácter de canalización.</span><span class="sxs-lookup"><span data-stu-id="124fc-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="124fc-133">El objeto devuelto por ColItems se envía al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="124fc-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="124fc-134">El siguiente ejemplo de Windows PowerShell le permite conectarse a un equipo remoto en un dominio diferente.</span><span class="sxs-lookup"><span data-stu-id="124fc-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="124fc-135">En este ejemplo también se muestran los nombres de los procesos de las instancias del [**\_ proceso Win32**](/windows/desktop/CIMWin32Prov/win32-process) en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="124fc-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> <span data-ttu-id="124fc-136">Para ejecutar el script de Windows PowerShell anterior, debe ser administrador en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="124fc-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="124fc-137">En el ejemplo anterior, el usuario se conecta a un equipo remoto en un dominio diferente y especifica una configuración regional preferida.</span><span class="sxs-lookup"><span data-stu-id="124fc-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="124fc-138">El comando [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario y asigna las credenciales a un objeto.</span><span class="sxs-lookup"><span data-stu-id="124fc-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="124fc-139">En el ejemplo también se enumeran los nombres de las instancias de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que se ejecutan en el equipo.</span><span class="sxs-lookup"><span data-stu-id="124fc-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="124fc-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="124fc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="124fc-141">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="124fc-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
