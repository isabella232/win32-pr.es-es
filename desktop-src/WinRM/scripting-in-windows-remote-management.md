---
title: Scripting en Administración remota de Windows
description: La API de scripting en WinRM y la API COM adjunta para C++ están diseñadas para reflejar de cerca las operaciones del Protocolo de WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Scripting en Administración remota de Windows
- Administración remota de Windows, scripting en
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149291"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="dca7c-105">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="dca7c-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="dca7c-106">La [API de scripting en WinRM](winrm-scripting-api.md) y la API com adjunta para C++ están diseñadas para reflejar de cerca las operaciones del protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="dca7c-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="dca7c-107">La API de scripting de WinRM en Administración remota de Windows admite todas las operaciones de protocolo de WS-Management, excepto una.</span><span class="sxs-lookup"><span data-stu-id="dca7c-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="dca7c-108">No permite suscripciones a eventos.</span><span class="sxs-lookup"><span data-stu-id="dca7c-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="dca7c-109">Para suscribirse a eventos del registro de eventos del sistema BMC, debe usar las herramientas de línea de comandos Wecutil o wevtutil.</span><span class="sxs-lookup"><span data-stu-id="dca7c-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="dca7c-110">Para más información, vea [Eventos](events.md).</span><span class="sxs-lookup"><span data-stu-id="dca7c-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="dca7c-111">Winrm.vbs, una herramienta de línea de comandos, que se escribe en Visual Basic Scripting Edition (VBScript), llama a la API de scripting de WinRM.</span><span class="sxs-lookup"><span data-stu-id="dca7c-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="dca7c-112">Winrm.vbs proporciona ejemplos de cómo usar la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dca7c-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="dca7c-113">Usar WSman en comparación con el uso de scripting de WMI</span><span class="sxs-lookup"><span data-stu-id="dca7c-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="dca7c-114">WMI se conecta a equipos remotos a través de DCOM, que requiere la configuración descrita en [conexión a WMI en un equipo remoto](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="dca7c-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="dca7c-115">WinRM no usa DCOM para conectarse a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="dca7c-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="dca7c-116">En su lugar, el protocolo WS-Management envía mensajes SOAP y el servicio utiliza un único puerto para HTTP y un puerto para el transporte HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dca7c-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="dca7c-117">A diferencia de la herramienta de línea de comandos de **WinRM** , los scripts deben proporcionar el XML necesario para pasar a los mensajes de protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="dca7c-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="dca7c-118">También deben proporcionar URI.</span><span class="sxs-lookup"><span data-stu-id="dca7c-118">They must also provide URIs.</span></span> <span data-ttu-id="dca7c-119">Para obtener más información, vea [URI de recursos](resource-uris.md) y [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dca7c-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="dca7c-120">La API de scripting de WMI funciona con objetos, como instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que representan recursos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="dca7c-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="dca7c-121">Esta clase WMI se define en archivos de [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) , que se almacenan en formato binario en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="dca7c-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="dca7c-122">En WMI, una operación Get para un único recurso o una consulta para varias instancias devuelve objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="dca7c-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="dca7c-123">Un script WinRM no devuelve objetos, sino secuencias de texto XML.</span><span class="sxs-lookup"><span data-stu-id="dca7c-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="dca7c-124">Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dca7c-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="dca7c-125">Mostrar la salida XML de los scripts de WinRM</span><span class="sxs-lookup"><span data-stu-id="dca7c-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="dca7c-126">La API de scripting de WinRM obtiene y recibe cadenas XML que describen los recursos.</span><span class="sxs-lookup"><span data-stu-id="dca7c-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="dca7c-127">El XML resultante está en forma de una secuencia de texto y requiere que se muestre una transformación XML de otra manera.</span><span class="sxs-lookup"><span data-stu-id="dca7c-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="dca7c-128">El siguiente script WinRM genera una salida XML sin formato.</span><span class="sxs-lookup"><span data-stu-id="dca7c-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="dca7c-129">En el siguiente bloque de texto se muestra la salida XML del script WinRM.</span><span class="sxs-lookup"><span data-stu-id="dca7c-129">The following block of text shows the XML output from the WinRM script.</span></span>


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



<span data-ttu-id="dca7c-130">Los scripts pueden usar una transformación XML para que esta salida sea más legible.</span><span class="sxs-lookup"><span data-stu-id="dca7c-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="dca7c-131">Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="dca7c-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="dca7c-132">La siguiente versión del script da formato al XML en una salida legible.</span><span class="sxs-lookup"><span data-stu-id="dca7c-132">The following version of the script formats the XML into human-readable output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



<span data-ttu-id="dca7c-133">La transformación XSL crea el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="dca7c-133">The XSL transform creates the following output.</span></span>


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="dca7c-134">Script de WinRM y salida de WinRM. cmd</span><span class="sxs-lookup"><span data-stu-id="dca7c-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="dca7c-135">La salida de un script de WinRM se codifica en Unicode.</span><span class="sxs-lookup"><span data-stu-id="dca7c-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="dca7c-136">Si crea un [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) y escribe un archivo desde el script, el archivo resultante es Unicode.</span><span class="sxs-lookup"><span data-stu-id="dca7c-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="dca7c-137">Sin embargo, si redirige la salida a un archivo, la codificación es ANSI.</span><span class="sxs-lookup"><span data-stu-id="dca7c-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="dca7c-138">Si redirige la salida a un archivo XML y hay caracteres Unicode en la salida, el XML no será válido.</span><span class="sxs-lookup"><span data-stu-id="dca7c-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="dca7c-139">Tenga en cuenta que la herramienta de línea de comandos de **WinRM** genera ANSI.</span><span class="sxs-lookup"><span data-stu-id="dca7c-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dca7c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dca7c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dca7c-141">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="dca7c-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="dca7c-142">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="dca7c-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="dca7c-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dca7c-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="dca7c-144">[Referencia de DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dca7c-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 