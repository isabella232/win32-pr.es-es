---
title: Obtener datos del equipo local
description: Aunque Windows administración remota y WS-Management protocolo están diseñados explícitamente para la comunicación remota, el caso más sencillo es establecer una sesión en el equipo local.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 311a5960fc1b2408532acdf1b8048f7146598857696b8f7aa653e457be8be3cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121755"
---
# <a name="obtaining-data-from-the-local-computer"></a>Obtener datos del equipo local

Aunque Windows administración remota y WS-Management protocolo están diseñados explícitamente para la comunicación remota, el caso más sencillo es establecer una sesión en el equipo local. Algunos scripts pueden requerir datos de acceso en el equipo local, así como en equipos remotos.

**WinRM versión 2.0: **

Todas las operaciones se consideran remotas y el servicio WinRM debe iniciarse antes de realizar cualquier operación. Si no se especifica un destino remoto, se usa localhost de forma predeterminada y todas las operaciones se enviarán al servicio WinRM local. Para obtener más información sobre cómo iniciar el servicio WinRM, vea [Instalación y configuración para Windows administración remota.](installation-and-configuration-for-windows-remote-management.md)

Al usar el servicio WinRM para las operaciones locales, se deben tener en cuenta los siguientes factores:

-   Los administradores solo pueden leer la configuración local de WinRM.
-   Los espacios de nombres WMI deben tener establecidos permisos de habilitación remota. Para obtener más información, [vea Proteger una conexión WMI remota.](../wmisdk/securing-a-remote-wmi-connection.md)
-   Si no se crea [*un agente*](windows-remote-management-glossary.md) de escucha de WinRM, el servicio WinRM escucha las solicitudes locales en el puerto 47001.

Cada script de WinRM debe empezar estableciendo una sesión o conexión a un equipo mediante la creación de un [**objeto Session.**](session.md) Una vez creada la sesión, puede usar los métodos de objeto **Session,** como [**Session.Enumerate**](session-enumerate.md) o [**Session.Invoke**](session-invoke.md) para obtener datos o ejecutar métodos.

La creación de una sesión [](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) es algo similar a conectarse a un espacio de nombres Windows Management Instrumentation[(WMI).](/windows/desktop/WmiSdk/wmi-start-page) La sesión es básicamente una capa que permite enviar y recibir datos a través de mensajes [*SOAP*](windows-remote-management-glossary.md) y el WS-Management protocolo. Para obtener más información, [vea protocolo WS-Management](ws-management-protocol.md).

Al llamar [**al método WSMan.CreateSession**](wsman-createsession.md) para [](windows-remote-management-glossary.md) crear un [**objeto Session,**](session.md) se iniciará una sesión que se conecta al WinRM local.

**Para crear una sesión de WSMan y obtener datos**

1.  Cree un [**objeto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Cree una sesión llamando al [**método WSMan.CreateSession.**](wsman-createsession.md) Esta sesión se ejecuta con el nombre de usuario y la contraseña de inicio de sesión y puede obtener datos a través de WinRM local.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Cree un [*URI de*](windows-remote-management-glossary.md) recurso para identificar [*el*](windows-remote-management-glossary.md) recurso que desea administrar o para el que desea obtener datos. Para obtener más información sobre cómo dar formato a un URI, vea [Uri de recursos.](resource-uris.md) Este URI de recurso es para una instancia específica de la clase servicio [**Win32 \_ de**](/windows/desktop/CIMWin32Prov/win32-service) WMI, el servicio Winmgmt. Para obtener más información, [vea Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Llame [**a métodos**](session.md) session que obtienen o enumeran datos mediante el URI del recurso. Para obtener más información, vea [WinRM Scripting API](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Para obtener o administrar datos de otro equipo o usar distintos métodos de autenticación, vea [Obtener datos de un equipo remoto.](obtaining-data-from-a-remote-computer.md)

En el siguiente ejemplo de código de VBScript se muestra el script completo que obtiene la instancia específica del servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) de WMI denominada "Winmgmt".


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



En el siguiente ejemplo de código de VBScript se muestra el script completo con la transformación de datos. Para obtener más información, vea [Mostrar la salida XML de scripts winRM.](displaying-xml-output-from-winrm-scripts.md)


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 