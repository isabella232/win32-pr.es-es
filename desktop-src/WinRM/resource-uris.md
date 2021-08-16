---
title: URI de recursos
description: Un URI de recurso es un identificador para un tipo distinto de operación de administración o valor que usan los servicios de administración que implementan el WS-Management administración.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f13e18abd7ea452b84043dfef3d6bf6b18be6c476c0dfff9a34e42e45dbc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323733"
---
# <a name="resource-uris"></a>URI de recursos

Un [*URI de*](windows-remote-management-glossary.md) recurso es un identificador para un tipo distinto de operación de administración o valor utilizado por los servicios de administración que implementan el WS-Management de administración. Un valor de administración podría ser la temperatura dentro de un equipo. Un ejemplo de una operación de administración es iniciar un servicio detenido o establecer una cuota de usuario de volumen de disco.

## <a name="resource-uri-format"></a>Formato de URI de recurso

Un URI consta de un prefijo y una ruta de acceso a un recurso como se muestra en el ejemplo siguiente:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Esta especificación de esquema indica que el URI se basa en la versión 1 del protocolo WS-Management oficial y que el recurso es un disco lógico [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres \\ "root cimv2" del repositorio WMI. Los prefijos URI contienen una especificación de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" y un tipo específico de recurso, como **\_ Win32 LogicalDisk**. Para obtener más información sobre cómo identificar una instancia específica de una clase WMI, [vea Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

Para obtener más información, vea [Prefijos URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipos de URI de recursos

Aunque [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) es el origen principal de datos de administración para sistemas operativos basados en Windows, también existen otros orígenes de esquema de administración.

En la lista siguiente se describen varios tipos de URI de recursos que Windows administración remota:

-   URI de WMI

    Este grupo de URI representa una ruta de [*acceso Modelo de información común*](/windows/desktop/WmiSdk/gloss-c) clase que incluye el espacio de nombres y la clase .

    Los URI de WMI se pueden usar en:

    -   [**Métodos de**](session.md) sesión
    -   [**Métodos IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   [**Métodos WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) [**o IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   [**Métodos ResourceLocator**](resourcelocator.md) [**o IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI de IPMI

    Este grupo de URI representa los URI estándar del sector basados en la versión 2.9 de CIM. Los URI de IPMI se pueden usar en los métodos [**de**](session.md) sesión [**Get**](session-get.md), [**Put,**](session-put.md) [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Un ejemplo es https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Este recurso se define según el esquema [DMTF.org](https://www.dmtf.org/home) CIM.

-   URI de configuración de WinRM

    Este grupo de URI son operaciones de configuración para la configuración del agente de [*escucha de*](windows-remote-management-glossary.md) WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener se puede usar en [**los métodos de**](session.md) [**sesión Get**](session-get.md), [**Put,**](session-put.md) [**Create,**](session-create.md) [**Delete**](session-delete.md)y [**Enumerate**](session-enumerate.md).

-   [*URI del registro de*](windows-remote-management-glossary.md) eventos del sistema (SEL)

    Este grupo de URI se suscribe a eventos del recopilador de eventos desde el BMC. Puede suscribirse a estos eventos mediante la herramienta de línea de comandos **Wevtutil.** Para obtener más información, vea https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Distinción entre mayúsculas y minúsculas

El [*complemento WMI conserva el*](windows-remote-management-glossary.md) caso del URI del recurso recibido en una solicitud. Sin embargo, para garantizar la interoperabilidad con otras implementaciones del WS-Management, use el caso correcto para el recurso solicitado en el URI de recurso. El caso correcto es la ortografía definida por el proveedor de recursos.

Aunque los URI de recursos no requieren la confidencialidad de mayúsculas y minúsculas, el XML [*de*](windows-remote-management-glossary.md) fragmento sí lo hace. Un fragmento especifica solo una propiedad, en lugar de todo el conjunto de propiedades de un recurso. En el caso de los recursos WMI, la sintaxis de fragmentos obtiene una propiedad de una instancia de recurso. Por ejemplo, para obtener solo **la propiedad Version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) es necesario usar un fragmento. Para obtener más información sobre los fragmentos, vea "Adding a selector to a ResourceLocator or IWSManResourceLocator object" (Agregar un selector a un objeto ResourceLocator o IWSManResourceLocator) en Windows Administración remota y [WMI.](windows-remote-management-and-wmi.md)

Siguiendo los estándares XML y [*XPath,*](windows-remote-management-glossary.md) el complemento [*WMI*](windows-remote-management-glossary.md) aplica la confidencialidad de mayúsculas y minúsculas para los fragmentos y XML que define los parámetros de entrada de un método. Se requiere la confidencialidad de mayúsculas y minúsculas para admitir el estándar XPath 1.0/Nivel 1. Para obtener datos WMI a través de WinRM, la confidencialidad de mayúsculas y minúsculas significa que los nombres de clases, propiedades y métodos WMI deben coincidir con el caso del nombre que se encuentra en el repositorio WMI.

Para obtener más información, vea [Sintaxis XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Ejemplos de confidencialidad de mayúsculas y minúsculas

Por ejemplo, un script que obtiene la propiedad **\_ DESCRIPTOR** DE SEGURIDAD de una instancia de la clase de servicio [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI no puede usar mayúsculas para los nombres de la ruta de acceso del fragmento, solo el URI. El complemento [*WMI*](windows-remote-management-glossary.md) de WinRM devuelve un error para el siguiente ejemplo de VBScript porque el XML XPath proporcionado para **FragmentPath** no usa el caso correcto. En el repositorio WMI, la clase se escribe como "Servicio \_ Win32".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



En la versión siguiente del mismo ejemplo se muestra el uso correcto de case para la clase de [**servicio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service) y la **propiedad DESCRIPTOR \_ DE** SEGURIDAD.


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Administración remota de hardware](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 