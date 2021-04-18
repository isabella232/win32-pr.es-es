---
description: Especifica el modelo de hospedaje del proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegios especificado.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hospedaje y seguridad de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6b88a5727f34fbb76baf62dcdf0488e5eb9eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706928"
---
# <a name="provider-hosting-and-security"></a>Hospedaje y seguridad de proveedores

La propiedad [**HostingModel**](--win32provider.md) de la instancia de **\_ \_ Win32Provider** que representa el proveedor especifica el modelo de hospedaje del proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegios especificado.

## <a name="shared-provider-host-process"></a>Proceso de host de proveedor compartido

WMI reside en un host de servicio compartido con otros servicios. Para evitar la detención de todos los servicios cuando se produce un error en un proveedor, los proveedores se cargan en un proceso de host independiente denominado "Wmiprvse.exe". Se puede ejecutar más de un proceso con este nombre. Cada una de ellas puede ejecutarse en una cuenta diferente con una seguridad variable. Tenga en cuenta que, a partir de Windows Vista, use el comando [**WinMgmt**](winmgmt.md) para ejecutar WMI en un proceso independiente mediante un puerto fijo. Para obtener más información, vea [conectarse a WMI de forma remota a partir de vista](connecting-to-wmi-remotely-starting-with-vista.md).

El host compartido puede ejecutarse en una de las siguientes cuentas del sistema en un proceso de host Wmiprvse.exe:

-   [LocalSystem (Sistema local)](/windows/desktop/Services/localsystem-account)
-   [NetworkService (Servicio de red)](/windows/desktop/Services/networkservice-account)
-   [LocalService (Servicio local)](/windows/desktop/Services/localservice-account)

Un proveedor también puede ser un servidor COM local (. exe) o autohospedado, que no requiere un host del proveedor WMI.

## <a name="setting-the-hosting-model"></a>Establecer el modelo de hospedaje

Dado que LocalSystem es una cuenta con privilegios, se recomienda establecer [**HostingModel**](--win32provider.md) en **NetworkServiceHost** cuando un proveedor se ejecute en un proceso de Wmiprvse.exe. La cuenta NetworkServiceHost es para los servicios que no requieren privilegios extensivos, pero que deben comunicarse de forma remota con otros sistemas.

Si no establece un valor para la propiedad [**HostingModel**](--win32provider.md) , WMI establecerá un valor predeterminado de **NetworkServiceHostOrSelfHost**. Si el valor de **HostingModel** se establece en **LocalSystemHost**, WMI utiliza el seguimiento para generar los eventos 5603 y 5604 en el registro de eventos de Windows. Dado que la cuenta local [LocalSystem](/windows/desktop/Services/localsystem-account) tiene privilegios elevados, no se recomienda esta configuración. Puede ver estos eventos en el **visor de eventos**. Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

Establezca la propiedad [**HostingModel**](--win32provider.md) para los proveedores desacoplados como "desacoplado: com". Los proveedores creados mediante la adición de clases de instrumentación de [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) en el .NET Framework son proveedores desacoplados. (**System. Management. Instrumentation** ya no se admite). Para obtener más información sobre la creación de un proveedor desacoplado, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

El modelo de hospedaje se especifica en la propiedad [**HostingModel**](--win32provider.md) de la instancia de **\_ \_ Win32Provider** que representa el proveedor.

**Para establecer el modelo de hospedaje para un proveedor**

1.  En el archivo MOF que define el proveedor, cree una instancia de [**\_ \_ Win32Provider**](--win32provider.md).
2.  Asigne un nombre al proveedor en la propiedad **nombre** y asigne el identificador de clase (CLSID) del objeto com del proveedor a la propiedad **CLSID** .

    En el ejemplo de código siguiente se asigna un nombre a la propiedad **Name** y el CSLID del objeto com Provider a la propiedad **CLSID** .

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Asigne el valor de host compartido adecuado a la propiedad [**HostingModel**](--win32provider.md) . Los valores de host compartido como "NetworkServiceHost" se definen en la propiedad **HostingSpecification** de la clase de [**\_ proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .

    En el ejemplo de código siguiente se asigna un valor de host compartido a la propiedad [**HostingModel**](--win32provider.md) .

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

En el ejemplo de código siguiente se muestra cómo registrar un proveedor en NetworkServiceHost.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Si tiene varios proveedores, puede agruparlos en un host de servicio específico registrando el proveedor para que resida en la instancia específica.

En el ejemplo de código siguiente también se registra un proveedor en NetworkServiceHost. La clase de [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) define valores para los dos valores que se combinan para crear la propiedad **HostingModel** de [**\_ \_ Win32Provider**](--win32provider.md) . En el ejemplo, el valor "NetworkServiceHost" procede de la propiedad **HostingSpecification** de los **\_ proveedores msft** y "LocalServiceHost" procede de la propiedad **HostingGroup** .

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Existen problemas de desarrollo especiales para los proveedores que no están desacoplados y que se hospedan en el proceso de Wmiprvse. Para obtener más información, vea [depuración de proveedores](debugging-providers.md).

Si está escribiendo un proveedor que contiene el registro de la propiedad o del proveedor de clases, no todos los modelos de subprocesos funcionan. Para obtener más información, vea [elegir el registro correcto](choosing-correct-registration.md).

## <a name="hostingmodel-values-for-in-process-providers"></a>Valores de HostingModel para proveedores de In-Process

En la lista siguiente se enumeran los valores del modelo de hospedaje de proveedor que se usarán en la instancia de [**\_ \_ Win32Provider**](--win32provider.md) para los proveedores que se ejecutan en un proceso de Wmiprvse.exe.



| Valor de [ **\_ \_ Win32Provider. HostingModel**](--win32provider.md) | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | El proveedor comienza a usar la implementación del servidor local en lugar de in-Process. El contexto de seguridad del proceso en el que se ejecuta el proveedor determina el contexto de seguridad del proveedor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | El proveedor, si se implementa como in-Process, se carga en un host de proveedor compartido que se ejecuta en el contexto de [LocalSystem](/windows/desktop/Services/localsystem-account) . A partir de Windows Vista, **LocalSystemHost** ya no es el modelo de hospedaje predeterminado si el [**HostingModel**](--win32provider.md) de un proveedor WMI (**\_ \_ Win32Provider**.**** La propiedad HostingModel) no está especificada. Para obtener más información, vea [seguridad de los modelos de hospedaje](#provider-hosting-and-security).                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | El proveedor se autohospeda o se carga en el proceso de Wmiprvse.exe que se ejecuta en la cuenta [LocalSystem](/windows/desktop/Services/localsystem-account) . Dado que LocalSystem es una cuenta con privilegios elevados, se genera una entrada en el registro de eventos de NT de seguridad para notificar a los administradores de un proveedor que se ejecutan en este estado de confianza.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | El proveedor, si se implementa como in-Process, se carga en el proceso de Wmiprvse.exe que se ejecuta en la cuenta [NetworkService](/windows/desktop/Services/networkservice-account) . A partir de Windows Vista, este es el modelo de hospedaje predeterminado si el [**HostingModel**](--win32provider.md) de un proveedor WMI (**\_ \_ Win32Provider**.**** La propiedad HostingModel) no está especificada. Para obtener más información, vea [seguridad de los modelos de hospedaje](#provider-hosting-and-security).<br/> **NetworkServiceHost** tiene privilegios limitados y, por tanto, reduce la posibilidad de que se produzca un ataque de elevación de privilegios. Si el proveedor solo funciona dentro del equipo local, establezca la propiedad [**HostingModel**](--win32provider.md) en **LocalServiceHost**.<br/> |
| **NetworkServiceHostOrSelfHost**                                   | El proveedor se autohospeda o se carga en el proceso de WmiPrvse.exe que se ejecuta en la cuenta [NetworkService](/windows/desktop/Services/networkservice-account) . **NetworkServiceHostOrSelfHost** es la configuración predeterminada cuando la propiedad [**HostingModel**](--win32provider.md) de **\_ \_ Win32Provider** es **null**. Dado que **NetworkServiceHostOrSelfHost** es el valor predeterminado, los proveedores de sistemas operativos anteriores pueden seguir funcionando en Windows Vista, windows Server 2008 y los sistemas operativos posteriores.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | El proveedor, si se implementa como in-Process, se carga en el proceso de Wmiprvse.exe que se ejecuta en la cuenta [LocalService](/windows/desktop/Services/localservice-account) . Este es el modelo de hospedaje recomendado para los servicios porque LocalService tiene privilegios limitados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valores de HostingModel para proveedores desacoplados

En la lista siguiente se enumeran los valores del modelo de hospedaje de proveedor para los proveedores desacoplados.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Desacoplado: com**
</dt> <dd>

El proveedor es un proveedor desacoplado hospedado en un proceso independiente que es un cliente de WMI.

En el ejemplo siguiente se muestra el especificador FoldIdentity para la propiedad [**HostingModel**](--win32provider.md) establecida en **false**, lo que permite al proveedor suplantar al cliente.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Si no se especifica FoldIdentity, el valor de FoldIdentity se establece en **true** de forma predeterminada. Por motivos de seguridad, se recomienda no especificar FoldIdentity (FALSE), ya que una aplicación no autorizada con suplantación de delegado puede afectar a todo el dominio.

En el ejemplo siguiente se muestra la propiedad [**HostingModel**](--win32provider.md) establecida de la manera recomendada, que es equivalente a establecer FOLDIDENTITY (true).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Desacoplado: Noncom**
</dt> <dd>

Solo para uso interno. No se admite.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Seguridad de los modelos de hospedaje

En la mayoría de los casos, **LocalSystem** no es necesario y el contexto **NetworkServiceHost** es más adecuado. La mayoría de los proveedores de WMI deben suplantar el contexto de seguridad del cliente para realizar las operaciones solicitadas en nombre del cliente WMI. A partir de Windows Vista, un proveedor WMI que carece de una definición de modelo de hospedaje y se ejecuta como si se estuviera ejecutando en **LocalSystem** no se ejecutará correctamente. Para corregir esta situación, cambie el modelo de hospedaje esperado y asegúrese de que el código del proveedor WMI realiza las operaciones en el contexto de seguridad del cliente mediante la suplantación del cliente WMI. LocalSystem rara vez es un requisito. Si el proveedor debe tener ese nivel de privilegios, especifique el modelo de hospedaje con la siguiente instrucción en el archivo MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elección del registro correcto](choosing-correct-registration.md)
</dt> <dt>

[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Clases de solución de problemas y configuración del proveedor](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**Proveedores de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

