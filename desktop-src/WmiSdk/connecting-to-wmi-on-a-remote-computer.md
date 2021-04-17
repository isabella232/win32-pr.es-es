---
description: Describe cómo los scripts, las aplicaciones y los proveedores pueden establecer conexiones a WMI en equipos remotos para obtener datos o controlar el hardware y el software.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Conexión a WMI en un equipo remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678163"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="266e6-103">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="266e6-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="266e6-104">WMI se puede usar para administrar y tener acceso a los datos de WMI en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="266e6-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="266e6-105">Las conexiones remotas en WMI se ven afectadas por el [firewall de Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) y la configuración de DCOM.</span><span class="sxs-lookup"><span data-stu-id="266e6-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="266e6-106">El [control de cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)) también puede requerir cambios en algunas opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="266e6-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="266e6-107">Sin embargo, una vez que la configuración sea correcta, la llamada a un sistema remoto es muy similar a una llamada WMI local.</span><span class="sxs-lookup"><span data-stu-id="266e6-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="266e6-108">Sin embargo, puede optar por que sea más complejo, mediante el uso de credenciales diferentes, protocolos de autenticación alternativos y otras características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="266e6-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="266e6-109">Configuración de un equipo para una conexión remota</span><span class="sxs-lookup"><span data-stu-id="266e6-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="266e6-110">Para poder tener acceso a un sistema remoto con WMI, es posible que tenga que comprobar algunos valores de configuración de seguridad para confirmar que tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="266e6-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="266e6-111">De manera específica:</span><span class="sxs-lookup"><span data-stu-id="266e6-111">Specifically:</span></span>

-   <span data-ttu-id="266e6-112">Windows contiene una serie de características de seguridad que pueden bloquear el acceso a los scripts en sistemas remotos.</span><span class="sxs-lookup"><span data-stu-id="266e6-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="266e6-113">Por lo tanto, es posible que tenga que modificar la configuración del sistema de Active Directory y del firewall de Windows antes de efectuar una llamada WMI.</span><span class="sxs-lookup"><span data-stu-id="266e6-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="266e6-114">Para obtener más información, consulte [configuración de una conexión WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) y [solución de problemas de una conexión WMI remota](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="266e6-115">La configuración de DCOM correcta debe estar habilitada para que funcione una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="266e6-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="266e6-116">Cambiar la configuración de DCOM puede permitir que los usuarios con derechos reducidos tengan acceso a un equipo para una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="266e6-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="266e6-117">Para obtener más información, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="266e6-118">Además, puede haber algunas circunstancias en las que desee ejecutar WMI a través de un puerto fijo.</span><span class="sxs-lookup"><span data-stu-id="266e6-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="266e6-119">Para ello, también tendrá que cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="266e6-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="266e6-120">Para obtener más información, consulte [configuración de un puerto fijo para WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="266e6-121">Connecting to a Remote Computer</span><span class="sxs-lookup"><span data-stu-id="266e6-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="266e6-122">En esencia, la conexión a un sistema remoto con WMI consiste en asegurarse de que dispone de los permisos adecuados para obtener acceso al sistema y de que la conexión está configurada correctamente.</span><span class="sxs-lookup"><span data-stu-id="266e6-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="266e6-123">Una vez que tiene esos dos elementos, la propia conexión es relativamente sencilla.</span><span class="sxs-lookup"><span data-stu-id="266e6-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="266e6-124">Por ejemplo, si usa las credenciales de seguridad predeterminadas, puede tener acceso a WMI en un sistema remoto mediante el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="266e6-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="266e6-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Conexión a WMI de forma remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="266e6-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="266e6-126">Use el parámetro *-ComputerName* común a la mayoría de los cmdlets de WMI, como [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="266e6-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="266e6-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Conectarse a WMI de forma remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="266e6-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="266e6-128">Use un moniker que contenga el nombre del sistema remoto en la llamada a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="266e6-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="266e6-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conexión a WMI de forma remota con C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="266e6-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="266e6-130">Para la versión actual de la interfaz administrada de WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use el objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) para representar una conexión a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="266e6-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="266e6-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conexión a WMI de forma remota con C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="266e6-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="266e6-132">Para la versión V1 de la interfaz administrada de WMI ([System. Management](/dotnet/api/system.management)), use el objeto [ManagementScope](/dotnet/api/system.management.managementscope) para representar una conexión a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="266e6-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="266e6-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Ejemplo: obtener datos WMI desde un equipo remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="266e6-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="266e6-134">Use el método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para especificar el nombre del equipo remoto en el parámetro *strNetworkResource* .</span><span class="sxs-lookup"><span data-stu-id="266e6-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

<span data-ttu-id="266e6-135">Los ejemplos de código anteriores son posiblemente la conexión remota más básica que se puede realizar con WMI.</span><span class="sxs-lookup"><span data-stu-id="266e6-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="266e6-136">En concreto, en los ejemplos se da por hecho lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="266e6-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="266e6-137">Usted es un administrador del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="266e6-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="266e6-138">Debido al [control de cuentas de usuario](/previous-versions/aa905108(v=msdn.10)), la cuenta del sistema remoto debe ser una cuenta de dominio del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="266e6-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="266e6-139">Para obtener más información, vea control de cuentas de usuario y WMI.</span><span class="sxs-lookup"><span data-stu-id="266e6-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="266e6-140">La contraseña del equipo local actual no está en blanco.</span><span class="sxs-lookup"><span data-stu-id="266e6-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="266e6-141">En esencia, se trata de un requisito de seguridad de Windows que debe haber iniciado sesión en el sistema con una contraseña.</span><span class="sxs-lookup"><span data-stu-id="266e6-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="266e6-142">Los equipos locales y remotos están en el mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="266e6-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="266e6-143">Si necesita cruzar los límites del dominio, deberá proporcionar información adicional o usar un modelo de programación ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="266e6-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="266e6-144">Está usando su propia cuenta para tener acceso a la máquina remota.</span><span class="sxs-lookup"><span data-stu-id="266e6-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="266e6-145">Si intenta obtener acceso a una cuenta diferente, deberá proporcionar credenciales adicionales.</span><span class="sxs-lookup"><span data-stu-id="266e6-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="266e6-146">(Tenga en cuenta que no se permite el acceso a WMI localmente con credenciales distintas de la cuenta actual).</span><span class="sxs-lookup"><span data-stu-id="266e6-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="266e6-147">Ambos equipos ejecutan IPv6.</span><span class="sxs-lookup"><span data-stu-id="266e6-147">Both computers are running IPv6.</span></span> <span data-ttu-id="266e6-148">WMI admite conexiones a equipos que ejecutan IPv6.</span><span class="sxs-lookup"><span data-stu-id="266e6-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="266e6-149">Sin embargo, tanto el equipo local como el "equipo \_ B" deben ejecutar IPv6.</span><span class="sxs-lookup"><span data-stu-id="266e6-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="266e6-150">Cualquiera de los equipos también puede ejecutar IPv4.</span><span class="sxs-lookup"><span data-stu-id="266e6-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="266e6-151">Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="266e6-152">No es necesario que el script delegue, es decir, no necesita tener acceso a los equipos remotos adicionales a través del equipo remoto de destino.</span><span class="sxs-lookup"><span data-stu-id="266e6-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="266e6-153">Para obtener más información, consulte [delegar con WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="266e6-154">Está intentando realizar una llamada específica, en lugar de crear un proceso remoto.</span><span class="sxs-lookup"><span data-stu-id="266e6-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="266e6-155">Para obtener más información, vea [crear procesos de forma remota mediante WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="266e6-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="266e6-156">Teniendo en cuenta estas restricciones, una llamada WMI remota es muy similar a una llamada WMI local, la única diferencia es que debe especificar el nombre del sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="266e6-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="266e6-157">Sin embargo, puede optar por cambiar muchas de esas características: usar credenciales diferentes o enrutar la llamada a través de un equipo de terceros o tener acceso a un dominio diferente.</span><span class="sxs-lookup"><span data-stu-id="266e6-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
