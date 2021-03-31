---
title: Obtención de datos del equipo local
description: Aunque Administración remota de Windows y WS-Management protocolo están diseñados explícitamente para la comunicación remota, el establecimiento de una sesión en el equipo local es el caso más simple.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791704"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="2ed98-103">Obtención de datos del equipo local</span><span class="sxs-lookup"><span data-stu-id="2ed98-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="2ed98-104">Aunque Administración remota de Windows y WS-Management protocolo están diseñados explícitamente para la comunicación remota, el establecimiento de una sesión en el equipo local es el caso más simple.</span><span class="sxs-lookup"><span data-stu-id="2ed98-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="2ed98-105">Algunos scripts pueden requerir datos de acceso en el equipo local, así como en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="2ed98-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="2ed98-106">**Versión de WinRM 2,0:  **</span><span class="sxs-lookup"><span data-stu-id="2ed98-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="2ed98-107">Todas las operaciones se consideran remotas y el servicio WinRM debe iniciarse antes de que se realice cualquier operación.</span><span class="sxs-lookup"><span data-stu-id="2ed98-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="2ed98-108">Si no se especifica un destino remoto, se usa de forma predeterminada el localhost y todas las operaciones se enviarán al servicio WinRM local.</span><span class="sxs-lookup"><span data-stu-id="2ed98-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="2ed98-109">Para obtener más información acerca de cómo iniciar el servicio WinRM, consulte [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="2ed98-110">Al usar el servicio WinRM para las operaciones locales, deben tenerse en cuenta los siguientes factores:</span><span class="sxs-lookup"><span data-stu-id="2ed98-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="2ed98-111">La configuración de WinRM local solo la pueden leer los administradores.</span><span class="sxs-lookup"><span data-stu-id="2ed98-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="2ed98-112">Los espacios de nombres WMI deben tener establecidos permisos de habilitación remota.</span><span class="sxs-lookup"><span data-stu-id="2ed98-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="2ed98-113">Para obtener más información, consulte [protección de una conexión WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="2ed98-114">Si no se crea un [*agente de escucha*](windows-remote-management-glossary.md) de WinRM, el servicio WinRM escucha las solicitudes locales en el puerto 47001.</span><span class="sxs-lookup"><span data-stu-id="2ed98-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="2ed98-115">Cada script de WinRM debe comenzar estableciendo una sesión o una conexión a un equipo mediante la creación de un objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed98-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="2ed98-116">Una vez creada la sesión, puede usar los métodos de objeto de **sesión** , como [**Session. Enumerate**](session-enumerate.md) o [**Session. Invoke**](session-invoke.md) para obtener datos o para ejecutar métodos.</span><span class="sxs-lookup"><span data-stu-id="2ed98-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="2ed98-117">La creación de una sesión es algo similar a la [conexión](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) a un espacio de nombres de instrumental de administración de Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)).</span><span class="sxs-lookup"><span data-stu-id="2ed98-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="2ed98-118">La sesión es esencialmente una capa que le permite enviar y recibir datos a través de mensajes [*SOAP*](windows-remote-management-glossary.md) y el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="2ed98-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="2ed98-119">Para obtener más información, vea [protocolo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="2ed98-120">Al llamar al método [**WSMan. createSession**](wsman-createsession.md) para crear un objeto de [**sesión**](session.md) , se iniciará una [*sesión*](windows-remote-management-glossary.md) que se conecta al WinRM local.</span><span class="sxs-lookup"><span data-stu-id="2ed98-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="2ed98-121">**Para crear una sesión WSMan y obtener datos**</span><span class="sxs-lookup"><span data-stu-id="2ed98-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="2ed98-122">Cree un objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed98-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="2ed98-123">Cree una sesión mediante una llamada al método [**WSMan. createSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed98-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="2ed98-124">Esta sesión se ejecuta con el nombre de usuario y la contraseña de inicio de sesión y puede obtener datos a través del WinRM local.</span><span class="sxs-lookup"><span data-stu-id="2ed98-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="2ed98-125">Cree un [*URI*](windows-remote-management-glossary.md) de recurso para identificar el [*recurso*](windows-remote-management-glossary.md) que desea administrar o para el que desea obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="2ed98-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="2ed98-126">Para obtener más información sobre cómo dar formato a un URI, vea [URI de recursos](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="2ed98-127">Este URI de recurso es para una instancia específica de la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI, el servicio WinMgmt.</span><span class="sxs-lookup"><span data-stu-id="2ed98-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="2ed98-128">Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="2ed98-129">Llamar a métodos de [**sesión**](session.md) que obtienen o enumeran datos mediante el URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="2ed98-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="2ed98-130">Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="2ed98-131">Para obtener o administrar datos de otro equipo o usar diferentes métodos de autenticación, consulte [obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="2ed98-132">En el siguiente ejemplo de código de VBScript se muestra el script completo que obtiene la instancia específica [**del \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI denominado "WinMgmt".</span><span class="sxs-lookup"><span data-stu-id="2ed98-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="2ed98-133">En el siguiente ejemplo de código de VBScript se muestra el script completo con la transformación de datos.</span><span class="sxs-lookup"><span data-stu-id="2ed98-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="2ed98-134">Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="2ed98-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="2ed98-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ed98-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed98-136">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="2ed98-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2ed98-137">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="2ed98-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2ed98-138">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="2ed98-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 