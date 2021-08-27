---
title: Escribir un servidor SSPI autenticado
description: Antes de que se pueda realizar la comunicación autenticada entre los programas cliente y servidor, el servidor debe registrar su información de autenticación.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Llamada a procedimiento remoto RPC, tareas, escritura de un servidor SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462f153905d6b654a0533c7bd05bff0e9627869d6910fb1fea05fe9340b788a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010353"
---
# <a name="writing-an-authenticated-sspi-server"></a>Escribir un servidor SSPI autenticado

Antes de que se pueda realizar la comunicación autenticada entre los programas cliente y servidor, el servidor debe registrar su información de autenticación. En concreto, el servidor debe registrar su nombre principal y especificar el servicio de autenticación que usa. Para obtener más información sobre los nombres de entidad de seguridad, vea [Nombres de entidad de seguridad](principal-names.md). Para obtener más información sobre los servicios de autenticación, vea [Authentication Services](authentication-services.md).

Para registrar su información de autenticación, los servidores llaman a [**la función RpcServerRegisterAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Pase un puntero al nombre principal como valor del primer parámetro. Establezca el segundo parámetro en una constante que indique el servicio de autenticación que usará la aplicación. Para obtener una descripción de los servicios de autenticación, vea [Authentication-Service Constants](authentication-service-constants.md).

El servidor también puede pasar la dirección de una función de adquisición de claves como el valor del tercer parámetro. Vea [Funciones de adquisición de claves](key-acquisition-functions.md). Para usar la función de adquisición de claves predeterminada para el servicio de autenticación seleccionado, establezca el tercer parámetro en **NULL.** El último parámetro de la [**función RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) son datos de puntero que se pasan a la función de adquisición de claves, si proporciona una función de adquisición de claves. En el fragmento de código siguiente se muestra una llamada a **RpcServerRegisterAuthInfo.**


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



Además, el servidor puede proporcionar a la biblioteca en tiempo de ejecución rpc una función de autorización. Para establecer una función de autorización, llame a [**la función RpcMgmtSetAuthorizationFn.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn)

La parte del servidor de una aplicación distribuida puede llamar a la [**función RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para consultar un identificador de enlace para obtener información de autenticación.

Si el servidor se registra con un proveedor de soporte técnico de seguridad, no se enviarán las llamadas de cliente con credenciales no válidas. Sin embargo, se enviarán las llamadas sin credenciales. Hay tres maneras de evitar que esto suceda:

-   Registre la interfaz mediante [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), con una función de devolución de llamada de seguridad; Esto hará que la biblioteca en tiempo de ejecución de RPC rechace automáticamente las llamadas no autenticadas a esa interfaz. El registro de una función de devolución de llamada es compatible con otros métodos de comprobación de las credenciales de acceso. La función de devolución de llamada puede llamar a las funciones [**RpcImpersonateClient,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)o [**RpcBindingInqAuthClientEx,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) entre otras. Sin embargo, estas funciones no pueden usar los argumentos pasados a la función, ya que no están desmarshalled en ese momento.

> [!IMPORTANT]
> El registro de la interfaz mediante [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) con una función de devolución de llamada de seguridad es el método más recomendado para comprobar las credenciales de cliente.

 

-   Llame [**a RpcBindingInqAuthClient para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) determinar el nivel de seguridad que usa el cliente. El código auxiliar puede devolver un error si el cliente no está autenticado.

 

 




