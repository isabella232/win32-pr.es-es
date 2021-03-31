---
description: Cuando una aplicación de usuario solicita datos de objetos del sistema a través de un proveedor WMI, la suplantación significa que el proveedor presenta las credenciales que representan el nivel de seguridad de los clientes en lugar de los proveedores.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Suplantar a un cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911506"
---
# <a name="impersonating-a-client"></a>Suplantar a un cliente

Cuando una aplicación de usuario solicita datos de objetos en el sistema a través de un proveedor WMI, la suplantación significa que el proveedor presenta las credenciales que representan el nivel de seguridad del cliente en lugar de la del proveedor. La suplantación impide que un cliente obtenga acceso no autorizado a la información del sistema.

En este tema se describen las siguientes secciones:

-   [Registrar un proveedor para la suplantación](#registering-a-provider-for-impersonation)
-   [Establecer los niveles de suplantación dentro de un proveedor](#setting-impersonation-levels-within-a-provider)
-   [Mantenimiento de los niveles de seguridad de un proveedor](#maintaining-security-levels-in-a-provider)
-   [Controlar los mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider)
-   [Informar de instancias parciales](#reporting-partial-instances)
-   [Enumeración parcial de informes](#reporting-partial-enumerations)
-   [Depuración del código de acceso denegado](#debugging-your-access-denied-code)
-   [Temas relacionados](#related-topics)

Normalmente, WMI se ejecuta como un servicio administrativo en un nivel de seguridad alto, mediante el contexto de seguridad LocalServer. El uso de un servicio administrativo proporciona a WMI los medios para tener acceso a la información privilegiada. Cuando se llama a un proveedor para obtener información, WMI pasa su identificador de seguridad (SID) al proveedor, lo que permite al proveedor tener acceso a información en el mismo nivel de seguridad alto.

Durante el proceso de inicio de la aplicación WMI, el sistema operativo Windows proporciona a la aplicación WMI el contexto de seguridad del usuario que inició el proceso. Normalmente, el contexto de seguridad del usuario es un nivel de seguridad inferior al de LocalServer, por lo que es posible que el usuario no tenga permiso de acceso a toda la información disponible en WMI. Cuando la aplicación de usuario solicita información dinámica, WMI pasa el SID del usuario al proveedor correspondiente. Si se escribe correctamente, el proveedor intenta tener acceso a la información con el SID de usuario, en lugar del SID del proveedor.

Para que el proveedor suplante correctamente la aplicación cliente, la aplicación cliente y el proveedor deben cumplir los siguientes criterios:

-   La aplicación cliente debe llamar a WMI con un nivel de seguridad de conexión COM del **\_ \_ \_ \_ delegado de nivel** de Imp. **\_ \_ \_ \_** Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).
-   El proveedor debe registrarse en WMI como proveedor de suplantación. Para obtener más información, vea [registrar un proveedor para la suplantación](#registering-a-provider-for-impersonation).
-   El proveedor debe cambiar al nivel de seguridad de la aplicación cliente antes de tener acceso a la información privilegiada. Para obtener más información, vea [configuración de los niveles de suplantación dentro de un proveedor](#setting-impersonation-levels-within-a-provider).
-   El proveedor debe administrar correctamente las condiciones de error si se deniega el acceso a esta información. Para obtener más información, vea [controlar los mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registrar un proveedor para la suplantación

WMI solo pasa el SID de una aplicación cliente a los proveedores que se han registrado como proveedores de suplantación. La habilitación de un proveedor para realizar la suplantación requiere que se modifique el proceso de registro del proveedor.

En el procedimiento siguiente se describe cómo registrar un proveedor para la suplantación. En el procedimiento se supone que ya entiende el proceso de registro. Para obtener más información sobre el proceso de registro, vea [registrar un proveedor](registering-a-provider.md).

**Para registrar un proveedor para la suplantación**

1.  Establezca la propiedad [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) de la clase [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor en 1.

    La propiedad [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) documenta si el proveedor admite la suplantación o no. Al establecer **ImpersonationLevel** en 0, se indica que el proveedor no suplanta al cliente y realiza todas las operaciones solicitadas en el mismo contexto de usuario que WMI. Al establecer **ImpersonationLevel** en 1, se indica que el proveedor utiliza las llamadas de suplantación para comprobar las operaciones realizadas en nombre del cliente.

2.  Establezca la propiedad **PerUserInitialization** de la misma clase [**\_ \_ Win32Provider**](--win32provider.md) en **true**.

> [!Note]  
> Si registra un proveedor con la propiedad [**\_ \_ Win32Provider**](--win32provider.md) **InitializeAsAdminFirst** establecida en **true**, el proveedor utiliza el token de seguridad de subprocesos de nivel de administración solo durante la fase de inicialización. Aunque no se produce un error en una llamada a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) , el proveedor utiliza el contexto de seguridad de WMI y no del cliente.

 

En el ejemplo de código siguiente se muestra cómo registrar un proveedor para la suplantación.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Establecer los niveles de suplantación dentro de un proveedor

Si registra un proveedor con la propiedad de clase [**\_ \_ Win32Provider**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) establecida en 1, WMI llama a su proveedor para suplantar a varios clientes. Para controlar estas llamadas, utilice las funciones de com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) en la implementación de la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

La función [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) permite que un servidor suplante al cliente que realizó la llamada. Al colocar una llamada a **CoImpersonateClient** en la implementación de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), se permite que el proveedor establezca el token de subproceso del proveedor para que coincida con el token de subproceso del cliente y, por tanto, suplantar al cliente. Si no llama a **CoImpersonateClient**, el proveedor ejecuta código en un nivel de seguridad de administrador, con lo que se crea una posible vulnerabilidad de seguridad. Si el proveedor debe actuar temporalmente como administrador o realizar la comprobación de acceso manualmente, llame a [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).

A diferencia de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) es una función com que controla los niveles de suplantación de subprocesos. En este caso, **CoRevertToSelf** cambia el nivel de suplantación de nuevo a la configuración de suplantación original. En general, el proveedor es inicialmente un administrador y alterna entre **CoImpersonateClient** y **CoRevertToSelf** , dependiendo de si está realizando una llamada que representa al llamador o a sus propias llamadas. Es responsabilidad del proveedor colocar estas llamadas correctamente para que no exponga una carencia de seguridad al usuario final. Por ejemplo, el proveedor solo debe llamar a funciones nativas de Windows dentro de la secuencia de código suplantado.

> [!Note]  
> El propósito de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) es establecer la seguridad de un proveedor. Si determina que se ha producido un error en la suplantación, debe devolver un código de finalización adecuado a WMI a través de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Para obtener más información, vea [controlar los mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Mantenimiento de los niveles de seguridad de un proveedor

Los proveedores no pueden llamar a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) una vez en una implementación de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y suponen que las credenciales de suplantación permanecen en su lugar mientras dure el proveedor. En su lugar, llame a **CoImpersonateClient** varias veces durante el transcurso de una implementación para evitar que WMI cambie las credenciales.

La principal preocupación para establecer la suplantación de un proveedor es la reentrada. En este contexto, la reentrada es cuando un proveedor realiza una llamada a WMI para obtener información y espera hasta que WMI vuelva a llamar al proveedor. En esencia, el subproceso de ejecución deja el código del proveedor, solo para volver a escribir el código más adelante. La reentrada es una parte del diseño de COM y no suele ser un problema. Sin embargo, cuando el subproceso de ejecución entra en WMI, el subproceso toma los niveles de suplantación de WMI. Cuando el subproceso vuelva al proveedor, debe restablecer los niveles de suplantación con otra llamada a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).

Para protegerse de los agujeros de seguridad en el proveedor, debe realizar llamadas reentrantes en WMI solo mientras suplanta al cliente. Es decir, las llamadas a WMI deben realizarse después de llamar a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y antes de llamar a [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself). Dado que **CoRevertToSelf** hace que la suplantación se establezca en el nivel de usuario, WMI se está ejecutando, por lo general, LocalSystem, las llamadas reentrantes a WMI después de llamar a **CoRevertToSelf** podrían proporcionar al usuario, y a cualquier proveedor llamado, muchas más capacidades de las que deberían tener.

> [!Note]  
> Si llama a una función del sistema u otro método de interfaz, no se garantiza que el contexto de llamada se mantenga.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Controlar los mensajes de acceso denegado en un proveedor

La mayoría de los mensajes de error de acceso denegado aparecen cuando un cliente solicita una clase o información a la que no tienen acceso. Si el proveedor devuelve un mensaje de error de acceso denegado a WMI y WMI lo pasa al cliente, el cliente puede deducir que existe la información. En algunas situaciones, puede tratarse de una infracción de seguridad. Por lo tanto, el proveedor no debe propagar el mensaje al cliente. En su lugar, el conjunto de clases que el proveedor habría proporcionado no debe exponerse. De forma similar, un proveedor de instancias dinámicas debe llamar al origen de datos subyacente para determinar cómo tratar los mensajes de acceso denegado. Es responsabilidad del proveedor replicar esa filosofía en el entorno de WMI. Para obtener más información, vea [informes de instancias parciales](#reporting-partial-instances) e [informes de enumeraciones parciales](#reporting-partial-enumerations).

Cuando determine cómo el proveedor debe controlar los mensajes de acceso denegado, debe escribir y depurar el código. Durante la depuración, a menudo es conveniente distinguir entre una denegación debida a una suplantación baja y una denegación debido a un error en el código. Puede usar una prueba sencilla en el código para determinar la diferencia. Para obtener más información, vea [depurar el código de acceso denegado](#debugging-your-access-denied-code).

## <a name="reporting-partial-instances"></a>Informar de instancias parciales

Una repetición común de un mensaje de acceso denegado es cuando WMI no puede proporcionar toda la información para rellenar una instancia. Por ejemplo, un cliente puede tener autoridad para ver un objeto de unidad de disco duro, pero puede que no tenga autoridad para ver la cantidad de espacio disponible en la propia unidad de disco duro. El proveedor debe determinar cómo tratar cualquier situación en la que el proveedor no puede rellenar completamente una instancia con propiedades debido a una infracción de acceso.

WMI no requiere una respuesta única a los clientes que tienen acceso parcial a una instancia de. En su lugar, WMI versión 1. x permite al proveedor una de las siguientes opciones:

-   Se produce un error en toda la operación con **WBEM \_ e \_ acceso \_ denegado** y no se devuelve ninguna instancia.

    Devuelve un objeto de error junto con **WBEM \_ E \_ acceso \_ denegado** para describir el motivo de la denegación.

-   Devuelve todas las propiedades disponibles y rellena las propiedades no disponibles con un **valor null**.

> [!Note]  
> Asegúrese de que la devolución de **\_ \_ acceso \_ denegado a WBEM E** no crea una carencia de seguridad en su empresa.

 

## <a name="reporting-partial-enumerations"></a>Enumeración parcial de informes

Otra aparición común de una infracción de acceso es cuando WMI no puede devolver toda una enumeración. Por ejemplo, un cliente puede tener acceso para ver todos los objetos de equipo de la red local, pero es posible que no tenga acceso a los objetos de equipo de vista fuera de su dominio. El proveedor debe determinar cómo tratar cualquier situación en la que no se pueda completar una enumeración debido a una infracción de acceso.

Al igual que con un proveedor de instancias, WMI no requiere una única respuesta a una enumeración parcial. En su lugar, WMI versión 1. x permite a un proveedor de una de las siguientes opciones:

-   Devolver **WBEM \_ S \_ no \_ error** para todas las instancias a las que el proveedor pueda tener acceso.

    Si utiliza esta opción, el usuario no es consciente de que algunas instancias no están disponibles. Varios proveedores, como los que usan Lenguaje de consulta estructurado (SQL) con seguridad de nivel de fila, devuelven resultados parciales correctos mediante el nivel de seguridad del autor de la llamada para definir el conjunto de resultados.

-   Se produce un error en toda la operación con **WBEM \_ e \_ acceso \_ denegado** y no se devuelve ninguna instancia.

    Opcionalmente, el proveedor puede incluir un objeto de error que describa la situación del cliente. Tenga en cuenta que algunos proveedores pueden acceder a los orígenes de datos en serie y es posible que no encuentren denegaciones hasta que MSRC durante a través de la enumeración.

-   Devuelve todas las instancias de a las que se puede tener acceso, pero que también devuelven el código de estado no error **WBEM \_ S \_ acceso \_ denegado**.

    El proveedor debe anotar la denegación durante la enumeración y puede continuar proporcionando instancias, con el código de estado sin errores. El proveedor también puede elegir finalizar la enumeración en la primera denegación. La justificación de esta opción es que los distintos proveedores tienen diferentes paradigmas de recuperación. Un proveedor puede haber proporcionado ya instancias antes de detectar una infracción de acceso. Algunos proveedores pueden optar por continuar proporcionando otras instancias y otros pueden querer terminar.

Debido a la estructura de COM, no se pueden calcular las referencias de ninguna información durante un error, excepto un objeto de error. Por lo tanto, no se puede devolver información y un código de error. Si decide devolver información, debe utilizar en su lugar un código de estado sin errores.

## <a name="debugging-your-access-denied-code"></a>Depuración del código de acceso denegado

Algunas aplicaciones pueden usar niveles de suplantación inferiores a la **\_ \_ \_ \_ suplantación del nivel Imp de RPC C**. En este caso, se producirá un error en la mayoría de las llamadas de suplantación realizadas por el proveedor para la aplicación cliente. Para diseñar e implementar correctamente un proveedor, debe tener en cuenta esta idea.

De forma predeterminada, el único otro nivel de suplantación que puede tener acceso a un proveedor es el **\_ \_ \_ nivel \_ Imp de RPC C**. En los casos en los que una aplicación cliente usa el **\_ \_ \_ nivel \_ Imp de RPC C**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) no devuelve un código de error. En su lugar, el proveedor suplanta al cliente solo con fines de identificación. Por consiguiente, la mayoría de los métodos de Windows llamados por el proveedor devolverán un mensaje de acceso denegado. Esto es inocuo en la práctica, ya que los usuarios no podrán hacer nada inadecuado. Sin embargo, puede resultar útil durante el desarrollo de proveedores para saber si el cliente se suplantó realmente o no.

El código requiere las siguientes referencias y \# instrucciones include para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo determinar si un proveedor ha suplantado correctamente una aplicación cliente.


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
