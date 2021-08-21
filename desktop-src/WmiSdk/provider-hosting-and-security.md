---
description: Especifica el modelo de hospedaje del proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegio especificado.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hospedaje y seguridad del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce0853b268f3d0bef0c43cbeabc10651885f0bd3b07f79d5c1b29072b560c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050493"
---
# <a name="provider-hosting-and-security"></a>Hospedaje y seguridad del proveedor

La [**propiedad HostingModel**](--win32provider.md) de la **\_ \_ instancia de Win32Provider** que representa al proveedor especifica el modelo de hospedaje del proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegio especificado.

## <a name="shared-provider-host-process"></a>Proceso de host de proveedor compartido

WMI reside en un host de servicio compartido con otros servicios. Para evitar detener todos los servicios cuando se produce un error en un proveedor, los proveedores se cargan en un proceso de host independiente denominado "Wmiprvse.exe". Se puede ejecutar más de un proceso con este nombre. Cada uno se puede ejecutar en una cuenta diferente con una seguridad variable. Tenga en cuenta que, a partir de Windows Vista, use el comando [**winmgmt**](winmgmt.md) para ejecutar WMI en un proceso independiente por sí mismo mediante un puerto fijo. Para obtener más información, [vea Conectarse a WMI de forma remota a partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md).

El host compartido se puede ejecutar en una de las siguientes cuentas del sistema en un proceso Wmiprvse.exe host:

-   [LocalSystem (Sistema local)](/windows/desktop/Services/localsystem-account)
-   [NetworkService (Servicio de red)](/windows/desktop/Services/networkservice-account)
-   [LocalService (Servicio local)](/windows/desktop/Services/localservice-account)

Un proveedor también puede ser un servidor COM local (.exe) o auto-hospedado, que no requiere un host de proveedor WMI.

## <a name="setting-the-hosting-model"></a>Establecer el modelo de hospedaje

Dado que LocalSystem es una cuenta con privilegios, se recomienda establecer [**HostingModel**](--win32provider.md) en **NetworkServiceHost** cuando un proveedor se ejecuta en un proceso Wmiprvse.exe usuario. La cuenta networkServiceHost es para los servicios que no requieren privilegios amplios, pero necesitan comunicarse de forma remota con otros sistemas.

Si no establece un valor para la propiedad [**HostingModel,**](--win32provider.md) WMI establecerá un valor predeterminado de **NetworkServiceHostOrSelfHost**. Si el **valor de HostingModel** se establece en **LocalSystemHost,** WMI usa el seguimiento para generar los eventos 5603 y 5604 en el Windows de eventos. Dado que la [cuenta local LocalSystem](/windows/desktop/Services/localsystem-account) tiene privilegios elevados, no se recomienda esta configuración. Puede ver estos eventos en **el** Visor de eventos . Para obtener más información, vea [Seguimiento de la actividad WMI](tracing-wmi-activity.md).

Establezca la [**propiedad HostingModel**](--win32provider.md) para los proveedores desacoplados como "Decoupled:Com". Los proveedores creados mediante la adición de clases de [**instrumentación de Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) en .NET Framework son proveedores desacoplados. ( Ya no **se admite System.Management.Instrumentation).** Para obtener más información sobre cómo crear un proveedor desacoplado, vea [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

El modelo de hospedaje se especifica en la [**propiedad HostingModel**](--win32provider.md) en la **\_ \_ instancia de Win32Provider** que representa al proveedor.

**Para establecer el modelo de hospedaje de un proveedor**

1.  En el archivo MOF que define el proveedor, cree una instancia de [**\_ \_ Win32Provider**](--win32provider.md).
2.  Asigne un nombre al proveedor en la propiedad **Name** y asigne el identificador de clase (CLSID) del objeto COM del proveedor a la **propiedad Clsid.**

    En el ejemplo de código siguiente se asigna un nombre a la **propiedad Name** y el CSLID del objeto COM del proveedor a la **propiedad Clsid.**

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Asigne el valor de host compartido adecuado a la [**propiedad HostingModel.**](--win32provider.md) Los valores de host compartidos como "NetworkServiceHost" se definen en la **propiedad HostingSpecification** de la [**clase \_ MsfT Providers.**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)

    En el ejemplo de código siguiente se asigna un valor de host compartido a la [**propiedad HostingModel.**](--win32provider.md)

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

En el ejemplo de código siguiente también se registra un proveedor en NetworkServiceHost. La [**clase MsfT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) define valores para los dos valores que se combinan para crear la [**\_ \_ propiedad HostingModel de Win32Provider.**](--win32provider.md)  En el ejemplo, el valor "NetworkServiceHost" procede de la propiedad **HostingSpecification** de proveedores **\_ de MSFT** y "LocalServiceHost" procede de **la propiedad HostingGroup.**

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Existen problemas de desarrollo especiales para los proveedores que no están desacoplados y se hospedan en el proceso wmiprvse. Para obtener más información, vea [Proveedores de depuración](debugging-providers.md).

Si está escribiendo un proveedor que contiene el registro del proveedor de propiedades o clases, no todos los modelos de subprocesos funcionan. Para obtener más información, vea [Elegir el registro correcto.](choosing-correct-registration.md)

## <a name="hostingmodel-values-for-in-process-providers"></a>Valores de HostingModel para In-Process proveedores

En la lista siguiente se enumeran los valores del modelo de hospedaje del proveedor que se usarán en la [**\_ \_ instancia de Win32Provider**](--win32provider.md) para los proveedores que se ejecutan en un Wmiprvse.exe cliente.



| Valor en [ **\_ \_ Win32Provider.HostingModel**](--win32provider.md) | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | El proveedor comienza a usar la implementación del servidor local en lugar de en proceso. El contexto de seguridad del proceso en el que se ejecuta el proveedor determina el contexto de seguridad del proveedor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | El proveedor, si se implementa como en proceso, se carga en un host de proveedor compartido que se ejecuta en [el contexto LocalSystem.](/windows/desktop/Services/localsystem-account) A partir Windows Vista, **LocalSystemHost** ya no es el modelo de hospedaje predeterminado si [**hostingModel**](--win32provider.md) de un proveedor WMI (**\_ \_ Win32Provider**.**Propiedad HostingModel)** no se especifica. Para obtener más información, vea [Seguridad de los modelos de hospedaje.](#provider-hosting-and-security)                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | El proveedor se hospeda automáticamente o se carga en el proceso Wmiprvse.exe que se ejecuta en la [cuenta LocalSystem.](/windows/desktop/Services/localsystem-account) Dado que LocalSystem es una cuenta con privilegios elevados, se genera una entrada en el registro de eventos nt de seguridad para notificar a los administradores de un proveedor que se ejecuta en este estado de confianza.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | El proveedor, si se implementa como en proceso, se carga en el Wmiprvse.exe que se ejecuta en [la cuenta NetworkService.](/windows/desktop/Services/networkservice-account) A partir Windows Vista, este es el modelo de hospedaje predeterminado si [**hostingModel**](--win32provider.md) de un proveedor WMI (**\_ \_ Win32Provider**.**Propiedad HostingModel)** no se especifica. Para obtener más información, vea [Seguridad de los modelos de hospedaje.](#provider-hosting-and-security)<br/> **NetworkServiceHost tiene** privilegios limitados y, por tanto, reduce la posibilidad de un ataque de elevación de privilegios. Si el proveedor solo funciona dentro del equipo local, establezca la propiedad [**HostingModel**](--win32provider.md) en **LocalServiceHost.**<br/> |
| **NetworkServiceHostOrSelfHost**                                   | El proveedor se hospeda automáticamente o se carga en el proceso WmiPrvse.exe que se ejecuta en la [cuenta NetworkService.](/windows/desktop/Services/networkservice-account) **NetworkServiceHostOrSelfHost es** la configuración predeterminada cuando la propiedad [**HostingModel**](--win32provider.md) de **\_ \_ Win32Provider** es **NULL.** Dado **que NetworkServiceHostOrSelfHost** es el valor predeterminado, los proveedores de sistemas operativos anteriores pueden seguir funcionando en Windows Vista, Windows Server 2008 y sistemas operativos posteriores.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | El proveedor, si se implementa como en proceso, se carga en el Wmiprvse.exe que se ejecuta en la [cuenta LocalService.](/windows/desktop/Services/localservice-account) Este es el modelo de hospedaje recomendado para los servicios porque LocalService tiene privilegios limitados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valores de HostingModel para proveedores desacoplados

En la lista siguiente se enumeran los valores del modelo de hospedaje del proveedor para los proveedores desacoplados.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Desacoplado:Com**
</dt> <dd>

El proveedor es un proveedor desacoplado hospedado en un proceso independiente que es un cliente de WMI.

En el ejemplo siguiente se muestra el especificador FoldIdentity para la propiedad [**HostingModel**](--win32provider.md) establecida en **FALSE**, que permite al proveedor suplantar al cliente.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Si no se especifica FoldIdentity, el valor FoldIdentity se establece en **TRUE** de forma predeterminada. Por motivos de seguridad, se recomienda no especificar FoldIdentity(FALSE), ya que una aplicación no fiable con suplantación de Delegado puede afectar a todo un dominio.

En el ejemplo siguiente se muestra [**la propiedad HostingModel**](--win32provider.md) establecida de la manera recomendada equivalente a establecer FoldIdentity(TRUE).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Desacoplado:Noncom**
</dt> <dd>

Solo para uso interno. No compatible.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Seguridad de los modelos de hospedaje

En la mayoría de las situaciones, **LocalSystem** no es necesario y el **contexto NetworkServiceHost** es más adecuado. La mayoría de los proveedores WMI deben suplantar el contexto de seguridad de cliente para realizar las operaciones solicitadas en nombre del cliente WMI. A partir Windows Vista, un proveedor WMI que carece de una definición de modelo de hospedaje y se ejecuta como si se ejecuta en **LocalSystem** no se ejecutará correctamente. Para corregir esta situación, cambie el modelo de hospedaje esperado y asegúrese de que el código del proveedor WMI realiza las operaciones en el contexto de seguridad del cliente suplantando al cliente WMI. LocalSystem rara vez es un requisito. Si el proveedor debe tener ese nivel de privilegios, especifique el modelo de hospedaje con la siguiente instrucción en el archivo MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elección del registro correcto](choosing-correct-registration.md)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Clases de configuración y solución de problemas del proveedor](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**Proveedores \_ de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

