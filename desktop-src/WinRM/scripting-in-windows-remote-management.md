---
title: Scripting en Windows administración remota
description: La API de scripting de WinRM y la API COM que lo acompaña para C++ están diseñadas para reflejar estrechamente las operaciones del WS-Management protocolo.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Scripting en Windows administración remota
- Windows Administración remota, scripting en
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795435"
---
# <a name="scripting-in-windows-remote-management"></a>Scripting en Windows administración remota

La [API de scripting de WinRM](winrm-scripting-api.md) y la API COM que lo acompaña para C++ están diseñadas para reflejar estrechamente las operaciones del WS-Management protocolo.

WinRM Scripting API en Windows Remote Management admite todas las operaciones WS-Management protocolo, excepto una. No permite suscripciones a eventos. Para suscribirse a eventos del registro de eventos del sistema BMC, debe usar las herramientas de línea de comandos Wecutil o Wevtutil. Para más información, vea [Eventos](events.md).

La API de scripting de WinRM se llama mediante Winrm.vbs, una herramienta de línea de comandos, que se escribe en Visual Basic Scripting Edition (VBScript). Winrm.vbs proporciona ejemplos de cómo usar [La API de scripting de WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Uso de WSman en comparación con el uso de scripting WMI

WMI se conecta a equipos remotos a través de DCOM, que requiere la configuración descrita en [Conexión a WMI en un equipo remoto.](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer) WinRM no usa DCOM para conectarse a un equipo remoto. En su lugar, WS-Management protocolo envía mensajes SOAP y el servicio usa un único puerto para HTTP y un puerto para el transporte HTTPS.

A diferencia de la herramienta de línea de comandos **winrm,** los scripts deben proporcionar el XML necesario para pasar al WS-Management protocolo. También deben proporcionar URI. Para obtener más información, vea [Identificadores URI de](resource-uris.md) [recursos Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

Wmi Scripting API funciona con objetos, como instancias de [**\_ LogicalDisk de Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)que representan recursos en un equipo. Esta clase WMI se define en [*Managed Object Format (MOF),*](/windows/desktop/WmiSdk/gloss-m) que se almacenan en formato binario en el repositorio WMI. En WMI, una operación Get para un único recurso o una consulta para varias instancias devuelve objetos WMI.

Un script WinRM no devuelve objetos, sino secuencias de texto XML. Para obtener más información, [vea Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

## <a name="displaying-xml-output-from-winrm-scripts"></a>Mostrar la salida XML de scripts WinRM

WinRM Scripting API obtiene y recibe cadenas XML que describen los recursos. El XML resultante tiene el formato de una secuencia de texto y requiere que se muestre una transformación XML de alguna otra manera.

El siguiente script de WinRM genera una salida XML sin formato.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



El siguiente bloque de texto muestra la salida XML del script WinRM.


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



Los scripts pueden usar una transformación XML para que esta salida sea más legible. Para obtener más información, vea [Mostrar la salida XML de scripts winRM.](displaying-xml-output-from-winrm-scripts.md)

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



La transformación XSL crea la salida siguiente.


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



## <a name="winrm-script-and-winrmcmd-output"></a>Salida del script WinRM y Winrm.cmd

La salida de un script WinRM está codificada en Unicode. Si crea un [objeto FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) y escribe un archivo desde el script, el archivo resultante es Unicode. Sin embargo, si redirige la salida a un archivo, la codificación es ANSI. Si redirige la salida a un archivo XML y hay caracteres Unicode en la salida, el XML no será válido. Tenga en cuenta que la herramienta de línea de comandos **Winrm** genera ANSI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Msxsl](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Referencia de DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 