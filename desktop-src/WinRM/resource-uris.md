---
title: URI de recursos
description: Un URI de recurso es un identificador de un tipo distinto de operación de administración o valor utilizado por los servicios de administración que implementan el protocolo WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533196"
---
# <a name="resource-uris"></a>URI de recursos

Un [*URI de recurso*](windows-remote-management-glossary.md) es un identificador de un tipo distinto de operación de administración o valor utilizado por los servicios de administración que implementan el protocolo WS-Management. Un valor de administración podría ser la temperatura dentro de un equipo. Un ejemplo de una operación de administración es iniciar un servicio detenido o establecer una cuota de usuario del volumen de disco.

## <a name="resource-uri-format"></a>Formato de URI de recurso

Un URI consta de un prefijo y una ruta de acceso a un recurso, tal como se muestra en el ejemplo siguiente:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Esta especificación del esquema indica que el URI se basa en la versión 1 del protocolo oficial WS-Management y que el recurso es [**un \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres "root cimv2" del repositorio WMI. Los prefijos de URI contienen una especificación de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" y un tipo específico de recurso, como el **\_ LogicalDisk de Win32**. Para obtener más información sobre cómo identificar una instancia específica de una clase WMI, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

Para obtener más información, vea [prefijos de URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipos de URI de recurso

Mientras [*instrumental de administración de Windows (WMI)*](windows-remote-management-glossary.md) es el origen principal de los datos de administración para los sistemas operativos basados en Windows, también existen otros orígenes de esquema de administración.

En la siguiente lista se describen varios tipos de URI de recursos usados por Administración remota de Windows:

-   URI de WMI

    Este grupo de URI representa una ruta de acceso de clase [*modelo de información común*](/windows/desktop/WmiSdk/gloss-c) que incluye el espacio de nombres y la clase.

    Los URI de WMI se pueden usar en:

    -   Métodos de [**sesión**](session.md)
    -   Métodos [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   Métodos [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) o [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   Métodos [**ResourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI de IPMI

    Este grupo de URI representan los URI estándar del sector basados en la versión 2,9 de CIM. Los URI de IPMI se pueden usar en métodos de [**sesión**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Un ejemplo es https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Este recurso se define según el esquema CIM de [DMTF.org](https://www.dmtf.org/home) .

-   URI de configuración de WinRM

    Este grupo de URI son operaciones de configuración para la configuración del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener se puede usar en métodos de [**sesión**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)y [**Enumerate**](session-enumerate.md).

-   Uri [*del registro de eventos del sistema*](windows-remote-management-glossary.md) (SEL)

    Este grupo de URI se suscribe a eventos del recopilador de eventos desde el BMC. Puede suscribirse a estos eventos mediante la herramienta de línea de comandos **wevtutil** . Para más información, consulte https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Distinción entre mayúsculas y minúsculas

El [*complemento WMI*](windows-remote-management-glossary.md) conserva el caso del URI de recurso recibido en una solicitud. Sin embargo, para garantizar la interoperabilidad con otras implementaciones del protocolo WS-Management, use el caso correcto para el recurso solicitado en el URI del recurso. El caso correcto es el corrector ortográfico definido por el proveedor de recursos.

Aunque los URI de recursos no requieren distinción de mayúsculas y minúsculas, XML de [*fragmento*](windows-remote-management-glossary.md) sí. Un fragmento especifica solo una propiedad, en lugar del conjunto completo de propiedades de un recurso. En el caso de los recursos WMI, la sintaxis de fragmentos obtiene una propiedad de una instancia de recurso. Por ejemplo, la obtención de la propiedad **version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiere el uso de un fragmento. Para obtener más información acerca de los fragmentos, vea "agregar un selector a un objeto ResourceLocator o IWSManResourceLocator" en [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

En los siguientes estándares XML y [*XPath*](windows-remote-management-glossary.md) , el [*complemento WMI*](windows-remote-management-glossary.md) aplica la distinción de mayúsculas y minúsculas para los fragmentos y XML que define los parámetros de entrada de un método. La distinción de mayúsculas y minúsculas es necesaria para admitir el estándar XPath 1.0/nivel 1. Para obtener datos de WMI a través de WinRM, la distinción de mayúsculas y minúsculas significa que los nombres de las clases, las propiedades y los métodos de WMI deben coincidir con las mayúsculas y minúsculas del nombre que se encuentra en el repositorio WMI.

Para obtener más información, vea [Sintaxis de XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Ejemplos de mayúsculas y minúsculas

Por ejemplo, un script que obtiene la propiedad **del \_ descriptor de seguridad** de una instancia de la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI no puede usar mayúsculas para los nombres de la ruta de acceso del fragmento, solo el URI. El [*complemento de WMI*](windows-remote-management-glossary.md) de WinRM devuelve un error para el siguiente ejemplo de VBScript porque el XML de XPath proporcionado para **FragmentPath** no utiliza las mayúsculas y minúsculas correctas. En el repositorio WMI, la clase está escrita como " \_ servicio Win32".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



La siguiente versión del mismo ejemplo muestra el uso correcto de Case para la clase [**de \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) y la propiedad **\_ descriptor de seguridad** .


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

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Administración remota de hardware](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 