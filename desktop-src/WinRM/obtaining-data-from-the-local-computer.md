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
# <a name="obtaining-data-from-the-local-computer"></a>Obtención de datos del equipo local

Aunque Administración remota de Windows y WS-Management protocolo están diseñados explícitamente para la comunicación remota, el establecimiento de una sesión en el equipo local es el caso más simple. Algunos scripts pueden requerir datos de acceso en el equipo local, así como en equipos remotos.

**Versión de WinRM 2,0:  **

Todas las operaciones se consideran remotas y el servicio WinRM debe iniciarse antes de que se realice cualquier operación. Si no se especifica un destino remoto, se usa de forma predeterminada el localhost y todas las operaciones se enviarán al servicio WinRM local. Para obtener más información acerca de cómo iniciar el servicio WinRM, consulte [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

Al usar el servicio WinRM para las operaciones locales, deben tenerse en cuenta los siguientes factores:

-   La configuración de WinRM local solo la pueden leer los administradores.
-   Los espacios de nombres WMI deben tener establecidos permisos de habilitación remota. Para obtener más información, consulte [protección de una conexión WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).
-   Si no se crea un [*agente de escucha*](windows-remote-management-glossary.md) de WinRM, el servicio WinRM escucha las solicitudes locales en el puerto 47001.

Cada script de WinRM debe comenzar estableciendo una sesión o una conexión a un equipo mediante la creación de un objeto de [**sesión**](session.md) . Una vez creada la sesión, puede usar los métodos de objeto de **sesión** , como [**Session. Enumerate**](session-enumerate.md) o [**Session. Invoke**](session-invoke.md) para obtener datos o para ejecutar métodos.

La creación de una sesión es algo similar a la [conexión](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) a un espacio de nombres de instrumental de administración de Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)). La sesión es esencialmente una capa que le permite enviar y recibir datos a través de mensajes [*SOAP*](windows-remote-management-glossary.md) y el protocolo WS-Management. Para obtener más información, vea [protocolo WS-Management](ws-management-protocol.md).

Al llamar al método [**WSMan. createSession**](wsman-createsession.md) para crear un objeto de [**sesión**](session.md) , se iniciará una [*sesión*](windows-remote-management-glossary.md) que se conecta al WinRM local.

**Para crear una sesión WSMan y obtener datos**

1.  Cree un objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Cree una sesión mediante una llamada al método [**WSMan. createSession**](wsman-createsession.md) . Esta sesión se ejecuta con el nombre de usuario y la contraseña de inicio de sesión y puede obtener datos a través del WinRM local.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Cree un [*URI*](windows-remote-management-glossary.md) de recurso para identificar el [*recurso*](windows-remote-management-glossary.md) que desea administrar o para el que desea obtener los datos. Para obtener más información sobre cómo dar formato a un URI, vea [URI de recursos](resource-uris.md). Este URI de recurso es para una instancia específica de la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI, el servicio WinMgmt. Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Llamar a métodos de [**sesión**](session.md) que obtienen o enumeran datos mediante el URI de recurso. Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Para obtener o administrar datos de otro equipo o usar diferentes métodos de autenticación, consulte [obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md).

En el siguiente ejemplo de código de VBScript se muestra el script completo que obtiene la instancia específica [**del \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI denominado "WinMgmt".


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



En el siguiente ejemplo de código de VBScript se muestra el script completo con la transformación de datos. Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).


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

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 