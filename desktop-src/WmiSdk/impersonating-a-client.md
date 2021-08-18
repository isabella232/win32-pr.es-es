---
description: Cuando una aplicación de usuario solicita datos de objetos del sistema a través de un proveedor WMI, la suplantación significa que el proveedor presenta credenciales que representan el nivel de seguridad de los clientes en lugar de los proveedores.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Suplantación de un cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b6d1fe931a9e0620643d8b3f8a77c63d031a41f1dac9d17301e11c03d21bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757945"
---
# <a name="impersonating-a-client"></a>Suplantación de un cliente

Cuando una aplicación de usuario solicita datos de objetos del sistema a través de un proveedor WMI, la suplantación significa que el proveedor presenta credenciales que representan el nivel de seguridad del cliente en lugar del proveedor. La suplantación impide que un cliente obtenga acceso no autorizado a la información del sistema.

En este tema se de abordan las siguientes secciones:

-   [Registro de un proveedor para suplantación](#registering-a-provider-for-impersonation)
-   [Establecer niveles de suplantación dentro de un proveedor](#setting-impersonation-levels-within-a-provider)
-   [Mantener los niveles de seguridad en un proveedor](#maintaining-security-levels-in-a-provider)
-   [Control de mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider)
-   [Informes de instancias parciales](#reporting-partial-instances)
-   [Informes de enumeraciones parciales](#reporting-partial-enumerations)
-   [Depuración del código de acceso denegado](#debugging-your-access-denied-code)
-   [Temas relacionados](#related-topics)

WMI normalmente se ejecuta como un servicio administrativo en un nivel de seguridad alto, mediante el contexto de seguridad LocalServer. El uso de un servicio administrativo proporciona a WMI los medios para acceder a información con privilegios. Al llamar a un proveedor para obtener información, WMI pasa su identificador de seguridad (SID) al proveedor, lo que permite al proveedor acceder a la información en el mismo nivel de seguridad alto.

Durante el proceso de inicio de la aplicación WMI, el Windows operativo proporciona a la aplicación WMI el contexto de seguridad del usuario que inició el proceso. El contexto de seguridad del usuario suele ser un nivel de seguridad inferior al de LocalServer, por lo que es posible que el usuario no tenga permiso para acceder a toda la información disponible para WMI. Cuando la aplicación de usuario solicita información dinámica, WMI pasa el SID del usuario al proveedor correspondiente. Si se escribe correctamente, el proveedor intenta acceder a la información con el SID del usuario, en lugar del SID del proveedor.

Para que el proveedor suplante correctamente la aplicación cliente, la aplicación cliente y el proveedor deben cumplir los criterios siguientes:

-   La aplicación cliente debe llamar a WMI con un nivel de seguridad de conexión COM **de RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE** o **RPC C IMP LEVEL \_ \_ \_ \_ DELEGATE**. Para obtener más información, vea [Mantener la seguridad de WMI.](maintaining-wmi-security.md)
-   El proveedor debe registrarse con WMI como proveedor de suplantación. Para obtener más información, [vea Registrar un proveedor para la suplantación.](#registering-a-provider-for-impersonation)
-   El proveedor debe cambiar al nivel de seguridad de la aplicación cliente antes de acceder a la información con privilegios. Para obtener más información, vea [Establecer niveles de suplantación dentro de un proveedor](#setting-impersonation-levels-within-a-provider).
-   El proveedor debe controlar correctamente las condiciones de error si se deniega el acceso a esta información. Para obtener más información, vea [Control de mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registro de un proveedor para suplantación

WMI solo pasa el SID de una aplicación cliente a los proveedores que se han registrado como proveedores de suplantación. La habilitación de un proveedor para realizar la suplantación requiere que modifique el proceso de registro del proveedor.

En el procedimiento siguiente se describe cómo registrar un proveedor para suplantación. En el procedimiento se da por supuesto que ya comprende el proceso de registro. Para obtener más información sobre el proceso de registro, vea [Registrar un proveedor.](registering-a-provider.md)

**Para registrar un proveedor para suplantación**

1.  Establezca la [**propiedad ImpersonationLevel**](swbemsecurity-impersonationlevel.md) de la [**\_ \_ clase Win32Provider**](--win32provider.md) que representa el proveedor en 1.

    La [**propiedad ImpersonationLevel**](swbemsecurity-impersonationlevel.md) documenta si el proveedor admite la suplantación o no. Establecer **ImpersonationLevel** en 0 indica que el proveedor no suplanta al cliente y realiza todas las operaciones solicitadas en el mismo contexto de usuario que WMI. Establecer **ImpersonationLevel en** 1 indica que el proveedor usa llamadas de suplantación para comprobar las operaciones realizadas en nombre del cliente.

2.  Establezca la **propiedad PerUserInitialization** de la misma [**\_ \_ clase Win32Provider**](--win32provider.md) en **TRUE.**

> [!Note]  
> Si registra un proveedor con la propiedad **InitializeAsAdminFirst** de [**\_ \_ Win32Provider**](--win32provider.md) establecida en **TRUE,** el proveedor usa el token de seguridad de subprocesos de nivel de administración solo durante la fase de inicialización. Aunque no se producirá un error en una llamada a [**CoImpersonateClient,**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) el proveedor usa el contexto de seguridad de WMI y no del cliente.

 

En el ejemplo de código siguiente se muestra cómo registrar un proveedor para suplantación.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Establecer niveles de suplantación dentro de un proveedor

Si registra un proveedor con la propiedad de clase [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) de [**\_ \_ Win32Provider**](--win32provider.md) establecida en 1, WMI llama al proveedor para suplantar a varios clientes. Para controlar estas llamadas, use las funciones COM [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) en la implementación de la [**interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

La [**función CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) permite a un servidor suplantar al cliente que realizó la llamada. Al realizar una llamada a **CoImpersonateClient** en la implementación de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), permite al proveedor establecer el token de subproceso del proveedor para que coincida con el token de subproceso del cliente y, por tanto, suplantar al cliente. Si no llama a **CoImpersonateClient,** el proveedor ejecuta código en un nivel de seguridad de administrador, lo que crea una posible vulnerabilidad de seguridad. Si el proveedor necesita actuar temporalmente como administrador o realizar la comprobación de acceso manualmente, llame a [**CoRevertToSelf.**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)

A diferencia de [**CoImpersonateClient,**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) es una función COM que controla los niveles de suplantación de subprocesos. En este caso, **CoRevertToSelf** vuelve a cambiar el nivel de suplantación a la configuración de suplantación original. En general, el proveedor es inicialmente un administrador y alterna entre **CoImpersonateClient** y **CoRevertToSelf** en función de si realiza una llamada que representa al autor de la llamada o a sus propias llamadas. Es responsabilidad del proveedor realizar estas llamadas correctamente para no exponer un problema de seguridad al usuario final. Por ejemplo, el proveedor solo debe llamar a funciones nativas Windows dentro de la secuencia de código suplantada.

> [!Note]  
> El propósito de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) es establecer la seguridad de un proveedor. Si determina que se ha generado un error en la suplantación, debe devolver un código de finalización adecuado a WMI a través [**de IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Para obtener más información, vea [Control de mensajes de acceso denegado en un proveedor](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Mantener los niveles de seguridad en un proveedor

Los proveedores no pueden llamar a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) una vez en una implementación de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y asumir que las credenciales de suplantación permanecen en su lugar mientras dure el proveedor. En su lugar, llame a **CoImpersonateClient** varias veces durante el transcurso de una implementación para evitar que WMI cambie las credenciales.

La principal preocupación para establecer la suplantación de un proveedor es la reenlazamiento. En este contexto, la reenlazancia se produce cuando un proveedor realiza una llamada a WMI para obtener información y espera hasta que WMI vuelve a llamar al proveedor. Básicamente, el subproceso de ejecución deja el código del proveedor, solo para volver a escribir el código en una fecha posterior. Reentry forma parte del diseño de COM y, por lo general, no es un problema. Sin embargo, cuando el subproceso de ejecución entra en WMI, el subproceso toma los niveles de suplantación de WMI. Cuando el subproceso vuelva al proveedor, debe restablecer los niveles de suplantación con otra llamada a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).

Para protegerse de los problemas de seguridad del proveedor, debe realizar llamadas reentrante solo en WMI mientras suplanta al cliente. Es decir, las llamadas a WMI deben realizarse después de llamar a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) y antes de [**llamar a CoRevertToSelf.**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) Dado que **CoRevertToSelf** hace que la suplantación se establezca en el nivel de usuario en el que se ejecuta WMI, por lo general LocalSystem, las llamadas reentrantes a WMI después de llamar a **CoRevertToSelf** podrían proporcionar al usuario y a cualquier proveedor llamado, muchas más funcionalidades de las que deberían tener.

> [!Note]  
> Si llama a una función del sistema u otro método de interfaz, no se garantiza que se mantenga el contexto de llamada.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Control de mensajes de acceso denegado en un proveedor

La mayoría de los mensajes de error de acceso denegado aparecen cuando un cliente solicita una clase o información a la que no tienen acceso. Si el proveedor devuelve un mensaje de error acceso denegado a WMI y WMI lo pasa al cliente, el cliente puede deducir que la información existe. En algunas situaciones, esto puede ser una vulneración de la seguridad. Por lo tanto, el proveedor no debe propagar el mensaje al cliente. En su lugar, no se debe exponer el conjunto de clases que el proveedor habría proporcionado. Del mismo modo, un proveedor de instancias dinámicas debe llamar al origen de datos subyacente para determinar cómo tratar los mensajes de acceso denegado. Es responsabilidad del proveedor replicar esa filosofía en el entorno WMI. Para obtener más información, vea [Notificar instancias parciales y](#reporting-partial-instances) [Enumeraciones parciales de informes](#reporting-partial-enumerations).

Al determinar cómo debe controlar el proveedor los mensajes de acceso denegado, debe escribir y depurar el código. Durante la depuración, suele ser conveniente distinguir entre una denegación debido a una suplantación baja y una denegación debido a un error en el código. Puede usar una prueba sencilla en el código para determinar la diferencia. Para obtener más información, vea [Depuración del código de acceso denegado.](#debugging-your-access-denied-code)

## <a name="reporting-partial-instances"></a>Informes de instancias parciales

Una repetición común de un mensaje de acceso denegado es cuando WMI no puede proporcionar toda la información para rellenar una instancia. Por ejemplo, un cliente puede tener la autoridad para ver un objeto de unidad de disco duro, pero puede que no tenga autoridad para ver cuánto espacio está disponible en la propia unidad de disco duro. El proveedor debe determinar cómo controlar cualquier situación en la que el proveedor no pueda rellenar completamente una instancia con propiedades debido a una infracción de acceso.

WMI no requiere una única respuesta a los clientes que tienen acceso parcial a una instancia. En su lugar, la versión 1.x de WMI permite al proveedor una de las siguientes opciones:

-   Se producirá un error en toda la **operación con WBEM \_ E ACCESS \_ \_ DENIED** y no se devolverá ninguna instancia.

    Devuelve un objeto de error junto con **WBEM \_ E ACCESS \_ \_ DENIED** para describir el motivo de la denegación.

-   Devuelve todas las propiedades disponibles y rellena las propiedades no disponibles con **NULL.**

> [!Note]  
> Asegúrese de que devolver **WBEM \_ E ACCESS \_ \_ DENIED** no crea un vacío de seguridad en su empresa.

 

## <a name="reporting-partial-enumerations"></a>Informes de enumeraciones parciales

Otra repetición común de una infracción de acceso es cuando WMI no puede devolver toda una enumeración. Por ejemplo, un cliente puede tener acceso para ver todos los objetos de equipo de red local, pero puede que no tenga acceso para ver objetos de equipo fuera de su dominio. El proveedor debe determinar cómo controlar cualquier situación en la que no se pueda completar una enumeración debido a una infracción de acceso.

Al igual que con un proveedor de instancias, WMI no requiere una única respuesta a una enumeración parcial. En su lugar, la versión 1.x de WMI permite a un proveedor una de las siguientes opciones:

-   Devuelve **WBEM \_ S NO \_ \_ ERROR** para todas las instancias a las que el proveedor puede tener acceso.

    Si usa esta opción, el usuario no es consciente de que algunas instancias no estaban disponibles. Varios proveedores, como los que usan Lenguaje de consulta estructurado (SQL) con seguridad de nivel de fila, devuelven resultados parciales correctos mediante el nivel de seguridad del autor de la llamada para definir el conjunto de resultados.

-   Se producirá un error en toda la **operación con WBEM \_ E ACCESS \_ \_ DENIED** y no se devolverá ninguna instancia.

    Opcionalmente, el proveedor puede incluir un objeto de error que describa la situación para el cliente. Tenga en cuenta que algunos proveedores pueden acceder a los orígenes de datos en serie y no pueden encontrar denegaciones hasta que se desvía por la enumeración.

-   Devuelve todas las instancias a las que se puede acceder, pero también devuelve el código de estado noerror **WBEM \_ S ACCESS \_ \_ DENIED**.

    El proveedor debe tener en cuenta la denegación durante la enumeración y puede seguir proporcionando instancias, finalizando con el código de estado noerror. El proveedor también puede optar por finalizar la enumeración en la primera denegación. La justificación de esta opción es que los distintos proveedores tienen paradigmas de recuperación diferentes. Es posible que un proveedor ya haya entregado instancias antes de detectar una infracción de acceso. Algunos proveedores pueden optar por seguir proporcionando otras instancias y otros pueden desear finalizar.

Debido a la estructura de COM, no se puede serializar ninguna información durante un error excepto para un objeto de error. Por lo tanto, no puede devolver información y un código de error. Si decide devolver información, debe usar un código de estado noerror en su lugar.

## <a name="debugging-your-access-denied-code"></a>Depuración del código de acceso denegado

Algunas aplicaciones pueden usar niveles de suplantación inferiores a **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE**. En este caso, se producirá un error en la mayoría de las llamadas de suplantación realizadas por el proveedor para la aplicación cliente. Para diseñar e implementar correctamente un proveedor, debe tener en cuenta esta idea.

De forma predeterminada, el único otro nivel de suplantación que puede tener acceso a un proveedor es **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY**. En los casos en los que una aplicación cliente usa **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY,** [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) no devuelve un código de error. En su lugar, el proveedor suplanta al cliente solo con fines de identificación. Por lo tanto, la mayoría Windows métodos a los que llama el proveedor devolverán un mensaje de acceso denegado. Esto es inofensivo en la práctica, ya que los usuarios no podrán hacer nada inadecuado. Sin embargo, puede ser útil durante el desarrollo del proveedor saber si el cliente se suplantó realmente o no.

El código requiere las siguientes referencias e \# instrucciones include para compilarse correctamente.


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

[Establecer descriptores de seguridad de namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
