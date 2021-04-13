---
title: Establecer el nivel de seguridad de proceso predeterminado con VBScript
description: Un script puede usar la configuración de suplantación y la autenticación WMI predeterminada. Sin embargo, el script puede necesitar una conexión con más seguridad o puede conectarse a un espacio de nombres que requiera una conexión cifrada.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279118"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="e838d-104">Establecer el nivel de seguridad de proceso predeterminado con VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="e838d-105">Un script puede usar la configuración de suplantación y la autenticación WMI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e838d-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="e838d-106">Sin embargo, el script puede necesitar una conexión con más seguridad o puede conectarse a un espacio de nombres que requiera una conexión cifrada.</span><span class="sxs-lookup"><span data-stu-id="e838d-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="e838d-107">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md) y solicitud de [una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e838d-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="e838d-108">En el caso más simple, un script puede usar la configuración predeterminada de autenticación y suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="e838d-109">Normalmente, WMI se ejecuta en un host de servicio compartido y comparte la misma autenticación que otros procesos del host.</span><span class="sxs-lookup"><span data-stu-id="e838d-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="e838d-110">Si desea ejecutar el proceso WMI con un nivel de autenticación diferente, ejecute WMI con el comando [**WinMgmt**](winmgmt.md) con el modificador **/standalonehost** y establezca el nivel de autenticación para WMI en general.</span><span class="sxs-lookup"><span data-stu-id="e838d-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="e838d-111">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="e838d-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="e838d-112">El siguiente script utiliza la configuración predeterminada para los niveles de suplantación y autenticación.</span><span class="sxs-lookup"><span data-stu-id="e838d-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="e838d-113">También puede utilizar un [moniker](constructing-a-moniker-string.md) en una llamada a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), y establecer la configuración de seguridad predeterminada, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e838d-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="e838d-114">Para obtener más información acerca de cómo establecer distintos niveles de suplantación o autenticación en un script, o para establecer los valores predeterminados de un equipo, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e838d-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="e838d-115">Cambiar las credenciales de autenticación predeterminadas mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="e838d-116">Cambiar la configuración predeterminada de suplantación mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="e838d-117">Establecer el nivel de suplantación predeterminado mediante el registro</span><span class="sxs-lookup"><span data-stu-id="e838d-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="e838d-118">Acceso al objeto SWbemSecurity en VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="e838d-119">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e838d-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="e838d-120">Cambiar las credenciales de autenticación predeterminadas mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="e838d-121">Puede cambiar el nivel de autenticación en un script mediante una cadena de [moniker](constructing-a-moniker-string.md) y los objetos [**SWbemLocator**](swbemlocator.md) y [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="e838d-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="e838d-122">El nivel de autenticación debe establecerse según los requisitos del sistema operativo de destino al que se está conectando.</span><span class="sxs-lookup"><span data-stu-id="e838d-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="e838d-123">Para obtener más información, consulte [conexión entre distintos sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="e838d-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="e838d-124">En el ejemplo de código de VBScript siguiente se muestra cómo cambiar el nivel de autenticación en un script que obtiene los datos de espacio libre de un equipo remoto denominado "server1".</span><span class="sxs-lookup"><span data-stu-id="e838d-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="e838d-125">En el script moniker conexiones a WMI, use el nombre corto mostrado en la columna "nombre de moniker/Descripción" de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e838d-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="e838d-126">Por ejemplo, en el siguiente script, el nivel de autenticación se establece en **WbemAuthenticationLevelPktIntegrity**.</span><span class="sxs-lookup"><span data-stu-id="e838d-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="e838d-127">En la tabla siguiente se enumeran los niveles de autenticación que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="e838d-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="e838d-128">Estos niveles se definen en Wbemdisp. tlb en la enumeración [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="e838d-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="e838d-129">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="e838d-129">Name/value</span></span>                                                      | <span data-ttu-id="e838d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e838d-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e838d-131">**WbemAuthenticationLevelDefault**</span><span class="sxs-lookup"><span data-stu-id="e838d-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="e838d-132">0</span><span class="sxs-lookup"><span data-stu-id="e838d-132">0</span></span><br/>      | <span data-ttu-id="e838d-133">Moniker: predeterminado</span><span class="sxs-lookup"><span data-stu-id="e838d-133">Moniker: Default</span></span><br/> <span data-ttu-id="e838d-134">WMI utiliza la configuración de autenticación de Windows predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e838d-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="e838d-135">Esta es la configuración recomendada que permite a WMI negociar con el nivel requerido por el servidor que devuelve datos.</span><span class="sxs-lookup"><span data-stu-id="e838d-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="e838d-136">Sin embargo, si el espacio de nombres requiere cifrado, use **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="e838d-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="e838d-137">**WbemAuthenticationLevelNone**</span><span class="sxs-lookup"><span data-stu-id="e838d-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="e838d-138">1</span><span class="sxs-lookup"><span data-stu-id="e838d-138">1</span></span><br/>         | <span data-ttu-id="e838d-139">Moniker: ninguno</span><span class="sxs-lookup"><span data-stu-id="e838d-139">Moniker: None</span></span><br/> <span data-ttu-id="e838d-140">No utiliza autenticación.</span><span class="sxs-lookup"><span data-stu-id="e838d-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="e838d-141">**WbemAuthenticationLevelConnect**</span><span class="sxs-lookup"><span data-stu-id="e838d-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="e838d-142">2</span><span class="sxs-lookup"><span data-stu-id="e838d-142">2</span></span><br/>      | <span data-ttu-id="e838d-143">Moniker: conectar</span><span class="sxs-lookup"><span data-stu-id="e838d-143">Moniker: Connect</span></span><br/> <span data-ttu-id="e838d-144">Autentica las credenciales del cliente solo cuando el cliente establece una relación con el servidor.</span><span class="sxs-lookup"><span data-stu-id="e838d-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="e838d-145">**WbemAuthenticationLevelCall**</span><span class="sxs-lookup"><span data-stu-id="e838d-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="e838d-146">3</span><span class="sxs-lookup"><span data-stu-id="e838d-146">3</span></span><br/>         | <span data-ttu-id="e838d-147">Call</span><span class="sxs-lookup"><span data-stu-id="e838d-147">Call</span></span><br/> <span data-ttu-id="e838d-148">Solo se autentica al principio de cada llamada cuando el servidor recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e838d-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="e838d-149">**WbemAuthenticationLevelPkt**</span><span class="sxs-lookup"><span data-stu-id="e838d-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="e838d-150">4</span><span class="sxs-lookup"><span data-stu-id="e838d-150">4</span></span><br/>          | <span data-ttu-id="e838d-151">Moniker: PKT</span><span class="sxs-lookup"><span data-stu-id="e838d-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="e838d-152">Autentica que todos los datos recibidos provienen del cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="e838d-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="e838d-153">**WbemAuthenticationLevelPktIntegrity**</span><span class="sxs-lookup"><span data-stu-id="e838d-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="e838d-154">5</span><span class="sxs-lookup"><span data-stu-id="e838d-154">5</span></span><br/> | <span data-ttu-id="e838d-155">Moniker: PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="e838d-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="e838d-156">Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="e838d-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e838d-157">**WbemAuthenticationLevelPktPrivacy**</span><span class="sxs-lookup"><span data-stu-id="e838d-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="e838d-158">6</span><span class="sxs-lookup"><span data-stu-id="e838d-158">6</span></span><br/>   | <span data-ttu-id="e838d-159">Moniker: PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="e838d-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="e838d-160">Autentica todos los niveles de suplantación anteriores y cifra el valor del argumento de cada llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="e838d-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="e838d-161">Utilice esta opción si el espacio de nombres al que se está conectando requiere una conexión cifrada.</span><span class="sxs-lookup"><span data-stu-id="e838d-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="e838d-162">Para determinar si la llamada se realiza correctamente, compruebe el valor devuelto después de cambiar el nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="e838d-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="e838d-163">Por ejemplo, dado que las conexiones locales siempre tienen un nivel de autenticación de **wbemAuthenticationLevelPktPrivacy**, en el siguiente ejemplo se produce un error al establecer el nivel de autenticación porque se conecta al equipo local.</span><span class="sxs-lookup"><span data-stu-id="e838d-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="e838d-164">Un proveedor puede establecer la seguridad en un espacio de nombres para que no se devuelvan datos a menos que se use la privacidad de paquetes (PktPrivacy) en la conexión a ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e838d-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="e838d-165">Esto garantiza que los datos se cifren a medida que atraviesan la red.</span><span class="sxs-lookup"><span data-stu-id="e838d-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="e838d-166">Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="e838d-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="e838d-167">Para obtener más información, vea [proteger los espacios de nombres WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="e838d-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="e838d-168">Cambiar los niveles de suplantación predeterminados mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="e838d-169">Al realizar llamadas a la API de scripting para WMI, se recomienda usar los valores predeterminados que WMI proporciona para el nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="e838d-170">Las llamadas remotas y algunos proveedores con más de un salto de red requieren un nivel de suplantación superior al de WMI.</span><span class="sxs-lookup"><span data-stu-id="e838d-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="e838d-171">Si el nivel de suplantación no es suficiente, un proveedor podría rechazar una solicitud o proporcionar información incompleta.</span><span class="sxs-lookup"><span data-stu-id="e838d-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="e838d-172">Si no establece el nivel de suplantación en un moniker o estableciendo [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) en un objeto protegible, establezca el nivel de suplantación DCOM predeterminado para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e838d-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="e838d-173">El nivel de suplantación debe establecerse según los requisitos del sistema operativo de destino al que se está conectando.</span><span class="sxs-lookup"><span data-stu-id="e838d-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="e838d-174">Para obtener más información, consulte [conexión entre distintos sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="e838d-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="e838d-175">En el ejemplo de código de VBScript siguiente se muestra cómo cambiar el nivel de suplantación en el mismo script que se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e838d-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="e838d-176">En la tabla siguiente se enumeran los niveles de autenticación de [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) que usan.</span><span class="sxs-lookup"><span data-stu-id="e838d-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="e838d-177">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="e838d-177">Name/value</span></span>                                                    | <span data-ttu-id="e838d-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="e838d-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e838d-179">**wbemImpersonationLevelAnonymous**</span><span class="sxs-lookup"><span data-stu-id="e838d-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="e838d-180">1</span><span class="sxs-lookup"><span data-stu-id="e838d-180">1</span></span><br/>   | <span data-ttu-id="e838d-181">Moniker: anónimo</span><span class="sxs-lookup"><span data-stu-id="e838d-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="e838d-182">Oculta las credenciales de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="e838d-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="e838d-183">Las llamadas a WMI pueden dar error con este nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="e838d-184">**wbemImpersonationLevelIdentify**</span><span class="sxs-lookup"><span data-stu-id="e838d-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="e838d-185">2</span><span class="sxs-lookup"><span data-stu-id="e838d-185">2</span></span><br/>    | <span data-ttu-id="e838d-186">Moniker: identificar</span><span class="sxs-lookup"><span data-stu-id="e838d-186">Moniker: Identify</span></span><br/> <span data-ttu-id="e838d-187">permite que los objetos consulten las credenciales de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="e838d-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="e838d-188">Las llamadas a WMI pueden dar error con este nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="e838d-189">**wbemImpersonationLevelImpersonate**</span><span class="sxs-lookup"><span data-stu-id="e838d-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="e838d-190">3</span><span class="sxs-lookup"><span data-stu-id="e838d-190">3</span></span><br/> | <span data-ttu-id="e838d-191">Moniker: Impersonate</span><span class="sxs-lookup"><span data-stu-id="e838d-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="e838d-192">permite que los objetos usen las credenciales de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="e838d-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="e838d-193">Este es el nivel de suplantación recomendado para las llamadas de API de scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="e838d-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="e838d-194">**wbemImpersonationLevelDelegate**</span><span class="sxs-lookup"><span data-stu-id="e838d-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="e838d-195">4</span><span class="sxs-lookup"><span data-stu-id="e838d-195">4</span></span><br/>    | <span data-ttu-id="e838d-196">Moniker: delegado</span><span class="sxs-lookup"><span data-stu-id="e838d-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="e838d-197">Permite que los objetos dejen que otros objetos usen las credenciales de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="e838d-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="e838d-198">Esta suplantación funcionará con la API de scripting para las llamadas WMI, pero puede constituir un riesgo de seguridad innecesario.</span><span class="sxs-lookup"><span data-stu-id="e838d-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="e838d-199">En el ejemplo siguiente se muestra cómo establecer la suplantación en una cadena de moniker al obtener una instancia concreta del [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="e838d-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="e838d-200">Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="e838d-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="e838d-201">Establecer el nivel de suplantación predeterminado mediante el registro</span><span class="sxs-lookup"><span data-stu-id="e838d-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="e838d-202">Si tiene acceso al registro, también puede establecer la clave del registro del nivel de suplantación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e838d-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="e838d-203">Esta clave especifica el nivel de suplantación que utiliza la API de scripting para WMI, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e838d-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="e838d-204">La ruta de acceso siguiente identifica la ruta de acceso del registro.</span><span class="sxs-lookup"><span data-stu-id="e838d-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="e838d-205">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **predeterminado nivel de suplantación**</span><span class="sxs-lookup"><span data-stu-id="e838d-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="e838d-206">De forma predeterminada, la clave del registro se establece en 3, lo que especifica el nivel de suplantación de suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="e838d-207">Algunos proveedores pueden requerir un mayor nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="e838d-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="e838d-208">Acceso al objeto SWbemSecurity en VBScript</span><span class="sxs-lookup"><span data-stu-id="e838d-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="e838d-209">La otra forma de establecer el nivel de suplantación es desde el objeto de seguridad [**SWbemSecurity**](swbemsecurity.md) , que aparece como la propiedad [**Security \_**](swbemservices-security-.md) de los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e838d-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="e838d-210">WMI pasa la configuración de seguridad de un objeto primario a los descendientes del objeto original.</span><span class="sxs-lookup"><span data-stu-id="e838d-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="e838d-211">Por lo tanto, puede establecer el nivel de suplantación de un objeto [**SWbemServices**](swbemservices.md) después de iniciar sesión en WMI y las llamadas API mediante este objeto u objetos creados a partir de él, como los objetos de tipo [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="e838d-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e838d-212">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e838d-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e838d-213">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="e838d-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="e838d-214">Protección de los clientes de scripting</span><span class="sxs-lookup"><span data-stu-id="e838d-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

