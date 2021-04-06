---
title: Obtención de datos de un equipo remoto
description: Puede obtener datos o administrar recursos en equipos remotos, así como en el equipo local. La conexión a un equipo remoto en un script Administración remota de Windows es muy similar a establecer una conexión local.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904616"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="37ed8-104">Obtención de datos de un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="37ed8-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="37ed8-105">Puede obtener datos o administrar recursos en equipos remotos, así como en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="37ed8-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="37ed8-106">La conexión a un equipo remoto en un script Administración remota de Windows es muy similar a establecer una conexión local.</span><span class="sxs-lookup"><span data-stu-id="37ed8-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="37ed8-107">Los datos de la instancia de WMI están disponibles y, si el equipo remoto tiene hardware de BMC que se puede comunicar mediante el protocolo WS-Management, también están disponibles los datos de la [interfaz de administración de plataforma inteligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) .</span><span class="sxs-lookup"><span data-stu-id="37ed8-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="37ed8-108">Para obtener más información, consulte [administración remota de Windows y WMI](windows-remote-management-and-wmi.md) y [administración remota de hardware](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="37ed8-109">Es posible que tenga que crear un objeto [**ConnectionOptions**](connectionoptions.md) para especificar información sobre el tipo de autenticación solicitado para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="37ed8-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="37ed8-110">Si la cuenta del equipo remoto tiene el mismo nombre de usuario y contraseña de inicio de sesión, la única información adicional que necesita es el transporte, el nombre de dominio y el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="37ed8-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="37ed8-111">Debido a un [control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), la cuenta remota debe ser una cuenta de dominio y un miembro del grupo administradores del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="37ed8-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="37ed8-112">Si la cuenta es miembro del equipo local del grupo administradores, UAC no permite el acceso al servicio WinRM.</span><span class="sxs-lookup"><span data-stu-id="37ed8-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="37ed8-113">Para tener acceso a un servicio WinRM remoto en un grupo de trabajo, el filtrado de UAC para cuentas locales debe estar deshabilitado mediante la creación de la siguiente entrada de registro DWORD y el establecimiento de su valor en 1: **\[ HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="37ed8-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="37ed8-114">**Para conectarse a un equipo remoto con el nombre de usuario y la contraseña de inicio de sesión**</span><span class="sxs-lookup"><span data-stu-id="37ed8-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="37ed8-115">Especifique el equipo de destino con un nombre de dominio completo o una dirección IP y asígnelo a una constante.</span><span class="sxs-lookup"><span data-stu-id="37ed8-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="37ed8-116">Si se especifica una dirección IPv6, la dirección debe ir entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="37ed8-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="37ed8-117">Cree un objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="37ed8-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="37ed8-118">Cree la sesión, especificando el transporte, HTTP o HTTPS, y concatene con la constante que representa el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="37ed8-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="37ed8-119">En el siguiente ejemplo de código VBScript se muestra el script completo.</span><span class="sxs-lookup"><span data-stu-id="37ed8-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="37ed8-120">El script incluye una subrutina para transformar los datos de XML sin formato al formato legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="37ed8-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="37ed8-121">Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="37ed8-122">**Para conectarse a un equipo remoto con una cuenta diferente**</span><span class="sxs-lookup"><span data-stu-id="37ed8-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="37ed8-123">Especifique el equipo de destino con un nombre de dominio completo o una dirección IP y asígnelo a una constante.</span><span class="sxs-lookup"><span data-stu-id="37ed8-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="37ed8-124">Si se especifica una dirección IPv6, la dirección debe ir entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="37ed8-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="37ed8-125">Cree un objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="37ed8-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="37ed8-126">Llame al método [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) para crear un objeto [**ConnectionOptions**](connectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="37ed8-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="37ed8-127">La cuenta del equipo remoto debe ser miembro del grupo administradores del equipo local.</span><span class="sxs-lookup"><span data-stu-id="37ed8-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="37ed8-128">En la llamada [**WSman. createSession**](wsman-createsession.md) , especifique las marcas de conexión de sesión adecuadas en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="37ed8-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="37ed8-129">Para obtener más información, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="37ed8-130">Especifique el equipo de destino con un nombre de equipo completo o una dirección IP y el transporte (http o https).</span><span class="sxs-lookup"><span data-stu-id="37ed8-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="37ed8-131">Este script solicita la autenticación [*Kerberos*](windows-remote-management-glossary.md) desde el servicio WinRM remoto.</span><span class="sxs-lookup"><span data-stu-id="37ed8-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="37ed8-132">A diferencia de los scripts de WMI, puede utilizar varios métodos de autenticación en los scripts de WinRM.</span><span class="sxs-lookup"><span data-stu-id="37ed8-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="37ed8-133">Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="37ed8-134">Una vez que el objeto de sesión esté disponible, puede llamar a cualquiera de los métodos del objeto de [**sesión**](session.md) para obtener datos de un recurso.</span><span class="sxs-lookup"><span data-stu-id="37ed8-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="37ed8-135">Puede obtener datos de cualquier recurso que esté disponible en el equipo en el que se ejecuta la sesión.</span><span class="sxs-lookup"><span data-stu-id="37ed8-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="37ed8-136">Para obtener más información, consulte [obtener datos del equipo local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="37ed8-137">En el siguiente ejemplo de código VBScript se muestra el script completo.</span><span class="sxs-lookup"><span data-stu-id="37ed8-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="37ed8-138">El script incluye una subrutina para transformar los datos de XML sin formato al formato legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="37ed8-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="37ed8-139">Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="37ed8-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="37ed8-140">El script especifica la autenticación Kerberos, pero si el equipo remoto se encuentra en un grupo de trabajo y no en un dominio, la especificación de Kerberos genera un error.</span><span class="sxs-lookup"><span data-stu-id="37ed8-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="37ed8-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37ed8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ed8-142">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="37ed8-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="37ed8-143">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="37ed8-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="37ed8-144">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="37ed8-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 