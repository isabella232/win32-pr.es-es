---
title: Administración remota de Windows y WMI
description: Administración remota de Windows se puede utilizar para recuperar los datos expuestos por Instrumental de administración de Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105698032"
---
# <a name="windows-remote-management-and-wmi"></a>Administración remota de Windows y WMI

Administración remota de Windows se puede utilizar para recuperar los datos expuestos por Instrumental de administración de Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) y [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)). Puede obtener datos de WMI con scripts o aplicaciones que usan la [API de scripting de WinRM](winrm-scripting-api.md) o a través de la herramienta de línea de comandos de **WinRM** .

WinRM es compatible con la mayoría de las clases y operaciones de WMI conocidas, incluidos los objetos incrustados. WinRM puede aprovechar WMI para recopilar datos acerca de [*los recursos*](windows-remote-management-glossary.md) o para administrar recursos en un sistema operativo basado en Windows. Esto significa que puede obtener datos sobre objetos como discos, adaptadores de red, servicios o procesos de su empresa a través del conjunto existente de [clases WMI](/windows/desktop/WmiSdk/wmi-classes). También puede tener acceso a los datos de hardware que están disponibles en el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)estándar de WMI.

## <a name="identifying-a-wmi-resource"></a>Identificar un recurso WMI

Puede hacer referencia a una clase WMI como un [*recurso*](windows-remote-management-glossary.md) en WinRM y en el protocolo WS-Management: un tipo de entidad administrada, como un servicio o un disco.

Una clase o un método WMI se identifica mediante un [*URI*](windows-remote-management-glossary.md), al igual que cualquier otro recurso cuando se usa el protocolo WS-Management. El URI puede especificar un recurso de WMI (clase), una acción de WMI (método) o identificar una instancia específica de una clase en [*los mensajes*](windows-remote-management-glossary.md) enviados a través de una red. Para obtener más información, vea [URI de recursos](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Construir el prefijo URI para clases WMI

El prefijo URI contiene una parte fija y el espacio de nombres WMI. Por ejemplo, el prefijo URI en Windows Server que contiene la parte fija del prefijo es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Esto permite generar el prefijo de URI para cualquier espacio de nombres WMI. Por ejemplo, para tener acceso al espacio de nombres WMI **\\ predeterminado raíz** , use el siguiente prefijo de URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

La mayoría de las clases WMI para la administración se encuentran en el espacio de nombres **root \\ cimv2** . Para tener acceso a las clases e instancias del espacio de nombres **root \\ cimv2** , use el prefijo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Para obtener más información, vea [URI de recursos](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Generar un URI completo para clases WMI

El URI que proporcione, ya sea a la herramienta de línea de comandos de **WinRM** o a un script, consta del prefijo más la especificación de recursos.

En el procedimiento siguiente se describe cómo generar un URI de recurso para obtener una clase WMI o para usarla en una operación de enumeración.

**Para generar un URI de recurso para una clase WMI**

1.  Comience con el prefijo que indica que se debe usar el esquema de protocolo WS-Management.

    https://schemas.microsoft.com/wbem/wsman/1

    El prefijo de URI de recurso para las clases WMI siempre es el mismo. Para obtener más información, vea [prefijos de URI](uri-prefixes.md).

2.  Agregue el espacio de nombres WMI al prefijo.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Agregue el nombre de clase.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Para establecer el valor de una propiedad, o para invocar un método específico, agregue el valor o los valores de clave necesarios para la clase.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Si deja el valor de clave en blanco, no modificará el valor de la propiedad original.

    > [!Note]  
    > Si se deja el valor de clave en blanco, el valor de la propiedad se establece en **null**.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Localizar un recurso WMI con WinRM

Puede obtener datos de WMI a través de la herramienta de línea de comandos, **WinRM** o a través de un script de Visual Basic que use la [API de scripting de WinRM](winrm-scripting-api.md). No se usa una [ruta de acceso WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) para buscar un recurso. En su lugar, convierta el espacio de nombres y la jerarquía de WMI a un [*URI*](windows-remote-management-glossary.md).

El URI de WinRM de una clase WMI contiene dos partes: el [Prefijo de URI](uri-prefixes.md) y la clase a la que desea obtener acceso.

Por ejemplo, se puede proporcionar el siguiente URI al método [**Session. Enumerate**](session-enumerate.md) para enumerar todos los servicios de un equipo. El prefijo URI es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` y la clase es [**el \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

En WMI, enumere los datos de todas las instancias de un recurso o clase de varias maneras:

-   Una consulta para todas las instancias de ese recurso.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Una llamada a [**SWbemServices. instances**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject. \_ instances**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

En WinRM, hay una manera de enumerar todas las instancias de un recurso: [**Session. Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Buscar una instancia específica de un recurso WMI

En WMI, puede designar una instancia determinada de una clase especificando valores para las propiedades de clave o consultando una instancia que coincida con una lista de valores de propiedad. Las propiedades de clave tienen el [**calificador de clave**](/windows/desktop/WmiSdk/key-qualifier)de WMI.

Puede obtener una instancia específica de una clase de varias maneras:

-   Una llamada a [**Session. Enumerate**](session-enumerate.md) con los parámetros *Filter* y *Dialect* para crear una consulta.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Una llamada a [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get). Para [**Session. Get**](session-get.md), debe proporcionar uno o varios valores de clave específicos, precedidos de un signo de interrogación (?).

    El formato del URI para una instancia específica es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Una clase WMI puede tener más de una clave. Los pares de nombre y valor de clave se separan con un signo "+". En ese caso, el formato es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    La sintaxis de WinRM para obtener un objeto WMI singleton es diferente de la de WMI. Un singleton es una clase WMI definida para que solo se permita una instancia. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) son ejemplos de una clase singleton de WMI.

    La sintaxis de WMI para singletons se muestra en el siguiente ejemplo de código de VBScript.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    En el ejemplo siguiente se muestra la sintaxis singleton de WinRM que no usa "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Agregar un [*selector*](windows-remote-management-glossary.md) a un objeto [**ResourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .

    En el ejemplo de código de VBScript siguiente se muestra cómo utilizar un selector para obtener una instancia específica del [**\_ procesador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Prefijos de URI](uri-prefixes.md)
</dt> <dt>

[URI de recursos](resource-uris.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> </dl>
