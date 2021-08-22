---
title: Windows Administración remota y WMI
description: Windows La administración remota se puede usar para recuperar los datos expuestos por Windows Management Instrumentation.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642475"
---
# <a name="windows-remote-management-and-wmi"></a>Windows Administración remota y WMI

Windows La administración remota se puede usar para recuperar los datos expuestos por Windows Management Instrumentation[(WMI](/windows/desktop/WmiSdk/wmi-start-page) y [MI).](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) Puede obtener datos WMI con scripts o aplicaciones que usan [WinRM Scripting API](winrm-scripting-api.md) o a través de la herramienta de línea de comandos **Winrm.**

WinRM admite la mayoría de las operaciones y clases WMI conocidas, incluidos los objetos incrustados. WinRM puede aprovechar WMI para recopilar datos [*sobre*](windows-remote-management-glossary.md) los recursos o para administrar recursos en un Windows operativo basado en datos. Esto significa que puede obtener datos sobre objetos como discos, adaptadores de red, servicios o procesos de su empresa a través del conjunto existente de [clases WMI](/windows/desktop/WmiSdk/wmi-classes). También puede acceder a los datos de hardware que están disponibles en el proveedor [DE IPMI WMI estándar.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

## <a name="identifying-a-wmi-resource"></a>Identificación de un recurso WMI

Puede hacer referencia a [](windows-remote-management-glossary.md) una clase WMI como un recurso en WinRM y en el protocolo WS-Management: un tipo de entidad administrada, como un servicio o un disco.

Una clase o método WMI se identifica mediante un [*URI*](windows-remote-management-glossary.md), igual que cualquier otro recurso cuando se usa el protocolo WS-Management datos. El URI puede especificar un recurso WMI (clase), una acción WMI (método) o identificar una instancia específica de una clase en los mensajes enviados a través de una red. [](windows-remote-management-glossary.md) Para más información, consulte URI [de recursos.](resource-uris.md)

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Construcción del prefijo URI para clases WMI

El prefijo URI contiene una parte fija y el espacio de nombres WMI. Por ejemplo, el prefijo URI de Windows Server que contiene la parte fija del prefijo es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Esto permite generar el prefijo URI para cualquier espacio de nombres WMI. Por ejemplo, para acceder al espacio de nombres WMI **\\ predeterminado** raíz, use el siguiente prefijo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

La mayoría de las clases WMI para la administración están en el **espacio de \\ nombres cimv2** raíz. Para acceder a las clases e instancias del espacio **de \\ nombres cimv2** raíz, use el prefijo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Para más información, consulte URI [de recursos.](resource-uris.md)

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Generar un URI completo para clases WMI

El URI que se proporciona, ya sea a la herramienta de línea de comandos **Winrm** o a un script, consta del prefijo más la especificación del recurso.

En el procedimiento siguiente se describe cómo generar un URI de recurso para obtener una clase WMI o para usarlo en una operación de enumeración.

**Para generar un URI de recurso para una clase WMI**

1.  Comience con el prefijo que indica el WS-Management se debe usar el esquema de protocolo.

    https://schemas.microsoft.com/wbem/wsman/1

    El prefijo uri de recurso para las clases WMI siempre es el mismo. Para obtener más información, vea [Prefijos URI](uri-prefixes.md).

2.  Agregue el espacio de nombres WMI al prefijo .

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Agregue el nombre de clase.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Para establecer el valor de una propiedad o para invocar un método específico, agregue el valor de clave o los valores necesarios para la clase.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Si deja el valor de clave en blanco, no modificará el valor de propiedad original.

    > [!Note]  
    > Si deja el valor de clave en blanco, el valor de la propiedad se **establece en NULL.**

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Buscar un recurso WMI con WinRM

Puede obtener datos WMI a través de la herramienta de línea de comandos, **Winrm** o a través de un script Visual Basic que usa la API de [scripting de WinRM](winrm-scripting-api.md). No se usa una ruta [de acceso WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) para buscar un recurso. En su lugar, convierta el espacio de nombres WMI y la jerarquía en un [*URI*](windows-remote-management-glossary.md).

El URI de WinRM para una clase WMI contiene dos partes: el prefijo [uri](uri-prefixes.md) y la clase a la que desea acceder.

Por ejemplo, se puede proporcionar el siguiente URI al [**método Session.Enumerate**](session-enumerate.md) para enumerar todos los servicios de un equipo. El prefijo URI es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` y la clase es Servicio [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

En WMI, enumere los datos de todas las instancias de un recurso o clase de varias maneras:

-   Consulta para todas las instancias de ese recurso.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Una llamada a [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject.Instances. \_**](/windows/desktop/WmiSdk/swbemobject-instances-)

    `Set colServices = InstancesOf("Win32_Service")`

En WinRM, hay una manera de enumerar todas las instancias de un recurso: [**Session.Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Buscar una instancia específica de un recurso WMI

En WMI, puede designar una instancia determinada de una clase especificando valores para las propiedades de clave o consultando una instancia de que coincida con una lista de valores de propiedad. Las propiedades de clave tienen el [**calificador de clave WMI**](/windows/desktop/WmiSdk/key-qualifier).

Puede obtener una instancia específica de una clase de varias maneras:

-   Una llamada a [**Session.Enumerate con los**](session-enumerate.md) *parámetros filter* y *dialect* para crear una consulta.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Una llamada a [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get). Para [**Session.Get**](session-get.md), debe proporcionar uno o varios valores de clave específicos, precedidos de un signo de interrogación (?).

    El formato del URI para una instancia específica es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Una clase WMI puede tener más de una clave. Los pares clave-valor están separados por un signo "+". En ese caso, el formato es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    La sintaxis de WinRM para obtener un objeto WMI singleton es diferente de WMI. Un singleton es una clase WMI definida para que solo se permita una instancia. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting son**](/windows/desktop/CIMWin32Prov/win32-wmisetting) ejemplos de una clase singleton wmi.

    La sintaxis WMI para singletons se muestra en el siguiente ejemplo de código VBScript.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    En el ejemplo siguiente se muestra la sintaxis singleton de WinRM que no usa "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Agregar un [*selector*](windows-remote-management-glossary.md) a un [**objeto ResourceLocator**](resourcelocator.md) [**o IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

    En el ejemplo de código de VBScript siguiente se muestra cómo usar un selector para obtener una instancia específica del [**procesador Win32 \_**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Prefijos URI](uri-prefixes.md)
</dt> <dt>

[URI de recursos](resource-uris.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> </dl>
