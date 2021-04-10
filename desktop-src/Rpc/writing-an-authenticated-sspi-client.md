---
title: Escribir un cliente SSPI autenticado
description: Escribir un cliente SSPI autenticado y una llamada a procedimiento remoto (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC llamada a procedimiento remoto, tareas, escribir un cliente SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149467"
---
# <a name="writing-an-authenticated-sspi-client"></a>Escribir un cliente SSPI autenticado

Todas las sesiones de cliente/servidor RPC requieren un enlace entre el cliente y el servidor. Para agregar seguridad a las aplicaciones cliente/servidor, los programas deben usar un enlace autenticado. En esta sección se describe el proceso de creación de un enlace autenticado entre el cliente y el servidor.

-   [Crear identificadores de enlace del lado cliente](#creating-client-side-binding-handles)
-   [Proporcionar credenciales de cliente al servidor](#providing-client-credentials-to-the-server)

Para obtener información relacionada, vea [procedimientos usados con la mayoría de los paquetes de seguridad y protocolos](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) en el kit de desarrollo de software (SDK) de la plataforma.

## <a name="creating-client-side-binding-handles"></a>Crear identificadores de enlace del lado cliente

Para crear una sesión autenticada con un programa de servidor, las aplicaciones cliente deben proporcionar información de autenticación con su identificador de enlace. Para configurar un identificador de enlace autenticado, los clientes invocan a la función [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Estas dos funciones son casi idénticas. La única diferencia entre ellos es que el cliente puede especificar la calidad de servicio con la función **RpcBindingSetAuthInfoEx** .

En el fragmento de código siguiente se muestra cómo puede ser una llamada a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) .


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



Una vez que el cliente llama correctamente a las funciones [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la biblioteca en tiempo de ejecución de RPC autentica automáticamente todas las llamadas RPC en el enlace. El nivel de seguridad y autenticación que selecciona el cliente solo se aplica a ese identificador de enlace. Los identificadores de contexto derivados del identificador de enlace utilizarán la misma información de seguridad, pero las modificaciones posteriores en el identificador de enlace no se reflejarán en los identificadores de contexto. Para obtener más información, vea [identificadores de contexto](context-handles.md).

El nivel de autenticación permanece en vigor hasta que el cliente elige otro nivel o hasta que finaliza el proceso. La mayoría de las aplicaciones no requerirán un cambio en el nivel de seguridad. El cliente puede consultar cualquier identificador de enlace para obtener su información de autorización mediante la invocación de [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) y pasándole el identificador de enlace.

## <a name="providing-client-credentials-to-the-server"></a>Proporcionar credenciales de cliente al servidor

Los servidores usan la información de enlace del cliente para aplicar la seguridad. Los clientes siempre pasan un identificador de enlace como primer parámetro de una llamada a procedimiento remoto. Sin embargo, los servidores no pueden usar el identificador a menos que se declare como el primer parámetro para los procedimientos remotos en el archivo IDL o en el archivo de configuración de la aplicación (ACF) del servidor. Puede optar por mostrar el identificador de enlace en el archivo IDL, pero esto obliga a todos los clientes a declarar y manipular el identificador de enlace en lugar de usar el enlace automático o implícito. Para obtener más información, vea [los archivos IDL y ACF](the-idl-and-acf-files.md).

Otro método consiste en dejar los controladores de enlace fuera del archivo IDL y colocar el atributo **de \_ identificador explícito** en el ACF del servidor. De esta manera, el cliente puede utilizar el tipo de enlace que mejor se adapte a la aplicación, mientras que el servidor utiliza el controlador de enlace como si se hubiera declarado explícitamente.

El proceso de extracción de las credenciales del cliente desde el identificador de enlace tiene el siguiente aspecto:

-   Los clientes RPC llaman a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e incluyen su información de autenticación como parte de la información de enlace que se pasa al servidor.
-   Normalmente, el servidor llama a [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para comportarse como si fuera el cliente. Si el identificador de enlace no está autenticado, se produce un error en la llamada con RPC \_ S \_ no hay ningún \_ contexto \_ disponible. Para obtener el nombre de usuario del cliente, llame a [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) durante la suplantación, o en Windows XP o versiones posteriores de Windows, llame a [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) para obtener el contexto de autorización y, a continuación, use las funciones de authz para recuperar el nombre.
-   Normalmente, el servidor llamará a [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) para crear objetos con ACL. Una vez hecho esto, las comprobaciones de seguridad posteriores se vuelven automáticas.

 

 