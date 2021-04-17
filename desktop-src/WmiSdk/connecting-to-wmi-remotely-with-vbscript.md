---
description: Puede crear una conexión remota a WMI con VBScript mediante la creación de un objeto de conexión. Este objeto contiene el nombre del equipo, el espacio de nombres WMI al que desea conectarse, así como las credenciales y los niveles de autenticación pertinentes.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Conectarse a WMI de forma remota con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715848"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="66319-104">Conectarse a WMI de forma remota con VBScript</span><span class="sxs-lookup"><span data-stu-id="66319-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="66319-105">Puede crear una conexión remota a WMI con VBScript mediante la creación de un objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="66319-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="66319-106">Este objeto contiene el nombre del equipo, el espacio de nombres WMI al que desea conectarse, así como las credenciales y los niveles de autenticación pertinentes.</span><span class="sxs-lookup"><span data-stu-id="66319-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="66319-107">**Para conectarse a un sistema remoto mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="66319-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="66319-108">Especifique la información de conexión, como el nombre del equipo remoto, las credenciales y el nivel de autenticación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="66319-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="66319-109">Si se va a conectar a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con la que ha iniciado sesión, puede especificar la información de conexión en un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), como se describe en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="66319-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="66319-110">Por lo general, debe especificar el espacio de nombres WMI al que se conectará en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="66319-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="66319-111">Esto se debe a que es posible que el espacio de nombres predeterminado no sea el mismo en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="66319-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="66319-112">Al especificar el espacio de nombres se garantiza que se conecte al mismo espacio de nombres en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="66319-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="66319-113">Para obtener más información sobre las constantes de VBScript y las cadenas de scripting para usar la conexión de moniker, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="66319-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="66319-114">Si se conecta a un equipo remoto en un dominio diferente o usa un nombre de usuario y una contraseña diferentes, debe usar el método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="66319-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="66319-115">Al igual que con un moniker, se usa **ConnectServer** para especificar las credenciales, el nivel de autenticación y el espacio de nombres para la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="66319-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="66319-116">En el ejemplo de código siguiente se describe el uso de ConnectServer para tener acceso a un equipo remoto mediante una cuenta de administrador y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="66319-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="66319-117">Al usar la función [**ConnectServer**](swbemlocator-connectserver.md) para las conexiones remotas, establezca la suplantación y la autenticación en el objeto de seguridad obtenido mediante una llamada a [**SWbemServices. Security**](swbemservices-security-.md).</span><span class="sxs-lookup"><span data-stu-id="66319-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="66319-118">Puede usar la enumeración [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) para especificar el nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="66319-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="66319-119">En el ejemplo de código siguiente se establece el nivel de suplantación para el ejemplo de código de VBScript anterior.</span><span class="sxs-lookup"><span data-stu-id="66319-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="66319-120">Tenga en cuenta que algunas conexiones requieren un nivel de autenticación específico.</span><span class="sxs-lookup"><span data-stu-id="66319-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="66319-121">Para obtener más información, consulte Configuración de la [seguridad de procesos de aplicación cliente](setting-client-application-process-security.md) y [protección de los clientes de scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="66319-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="66319-122">En concreto, debe establecer el nivel de autenticación en **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C o 6 Si el espacio de nombres al que se está conectando en el equipo remoto requiere una conexión cifrada antes de devolver los datos.</span><span class="sxs-lookup"><span data-stu-id="66319-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="66319-123">También puede usar este nivel de autenticación, incluso si el espacio de nombres no lo requiere.</span><span class="sxs-lookup"><span data-stu-id="66319-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="66319-124">Esto garantiza que los datos se cifren a medida que atraviesan la red.</span><span class="sxs-lookup"><span data-stu-id="66319-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="66319-125">Si intenta establecer un nivel de autenticación inferior al permitido, se devolverá un mensaje de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="66319-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="66319-126">Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="66319-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="66319-127">Una vez realizada la conexión, puede seguir teniendo acceso a los datos de WMI.</span><span class="sxs-lookup"><span data-stu-id="66319-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="66319-128">Para obtener más información, vea [tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="66319-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="66319-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="66319-129">Examples</span></span>

<span data-ttu-id="66319-130">Para obtener un ejemplo de VBScript más grande, consulte la sección ejemplos en la página de referencia de [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="66319-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="66319-131">El siguiente ejemplo de código de VBScript se conecta a un grupo de equipos remotos en el mismo dominio mediante la creación de una matriz de nombres de equipo remoto y, a continuación, la visualización de los nombres de los Plug and Play dispositivos (instancias de [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="66319-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="66319-132">Para ejecutar el siguiente script, debe ser administrador en los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="66319-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="66319-133">Tenga en cuenta que el \\ \\ script debe incluir "" antes del nombre del equipo remoto después de la configuración del nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="66319-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="66319-134">Para obtener más información sobre las rutas de acceso WMI, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="66319-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="66319-135">El siguiente ejemplo de código de VBScript le permite conectarse a un equipo remoto con credenciales diferentes.</span><span class="sxs-lookup"><span data-stu-id="66319-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="66319-136">Por ejemplo, un equipo remoto en un dominio diferente o que se conecta a un equipo remoto que requiere un nombre de usuario y una contraseña diferentes.</span><span class="sxs-lookup"><span data-stu-id="66319-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="66319-137">En este caso, use la conexión [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="66319-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="66319-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66319-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66319-139">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="66319-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
