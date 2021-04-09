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
# <a name="scripting-in-windows-remote-management"></a>Scripting en Administración remota de Windows

La [API de scripting en WinRM](winrm-scripting-api.md) y la API com adjunta para C++ están diseñadas para reflejar de cerca las operaciones del protocolo de WS-Management.

La API de scripting de WinRM en Administración remota de Windows admite todas las operaciones de protocolo de WS-Management, excepto una. No permite suscripciones a eventos. Para suscribirse a eventos del registro de eventos del sistema BMC, debe usar las herramientas de línea de comandos Wecutil o wevtutil. Para más información, vea [Eventos](events.md).

Winrm.vbs, una herramienta de línea de comandos, que se escribe en Visual Basic Scripting Edition (VBScript), llama a la API de scripting de WinRM. Winrm.vbs proporciona ejemplos de cómo usar la [API de scripting de WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Usar WSman en comparación con el uso de scripting de WMI

WMI se conecta a equipos remotos a través de DCOM, que requiere la configuración descrita en [conexión a WMI en un equipo remoto](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer). WinRM no usa DCOM para conectarse a un equipo remoto. En su lugar, el protocolo WS-Management envía mensajes SOAP y el servicio utiliza un único puerto para HTTP y un puerto para el transporte HTTPS.

A diferencia de la herramienta de línea de comandos de **WinRM** , los scripts deben proporcionar el XML necesario para pasar a los mensajes de protocolo WS-Management. También deben proporcionar URI. Para obtener más información, vea [URI de recursos](resource-uris.md) y [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

La API de scripting de WMI funciona con objetos, como instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que representan recursos de un equipo. Esta clase WMI se define en archivos de [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) , que se almacenan en formato binario en el repositorio WMI. En WMI, una operación Get para un único recurso o una consulta para varias instancias devuelve objetos WMI.

Un script WinRM no devuelve objetos, sino secuencias de texto XML. Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

## <a name="displaying-xml-output-from-winrm-scripts"></a>Mostrar la salida XML de los scripts de WinRM

La API de scripting de WinRM obtiene y recibe cadenas XML que describen los recursos. El XML resultante está en forma de una secuencia de texto y requiere que se muestre una transformación XML de otra manera.

El siguiente script WinRM genera una salida XML sin formato.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



En el siguiente bloque de texto se muestra la salida XML del script WinRM.


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



Los scripts pueden usar una transformación XML para que esta salida sea más legible. Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).

La siguiente versión del script da formato al XML en una salida legible.


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



La transformación XSL crea el siguiente resultado.


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



## <a name="winrm-script-and-winrmcmd-output"></a>Script de WinRM y salida de WinRM. cmd

La salida de un script de WinRM se codifica en Unicode. Si crea un [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) y escribe un archivo desde el script, el archivo resultante es Unicode. Sin embargo, si redirige la salida a un archivo, la codificación es ANSI. Si redirige la salida a un archivo XML y hay caracteres Unicode en la salida, el XML no será válido. Tenga en cuenta que la herramienta de línea de comandos de **WinRM** genera ANSI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Referencia de DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 