---
title: Autenticación mutua en aplicaciones RPC
description: Los servicios RPC pueden usar puntos de conexión de servicio para publicarse por sí mismos o pueden usar las API del servicio de nombres de RPC (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en aplicaciones RPC AD
- Active Directory, usar, autenticación mutua, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904487"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Autenticación mutua en aplicaciones RPC

Los servicios RPC pueden usar puntos de conexión de servicio para publicarse por sí mismos o pueden usar las API del servicio de nombres de RPC (RpcNs). En este tema se describe cómo realizar la autenticación mutua con un servicio RPC que se publica mediante las API del servicio de nombres de RPC (RpcNs).

**Para registrar un SPN en el directorio**

1.  Llame a la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear un nombre de entidad de seguridad de servicio (SPN) para el servicio.
2.  Llame a la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar el SPN en la cuenta de servicio o en la cuenta de equipo en cuyo contexto se ejecutará el servicio.

**Para registrar un servicio con el servicio de nombres de RPC**

1.  Compruebe que los SPN adecuados están registrados en la cuenta en la que se está ejecutando el servicio. Para obtener más información, consulte tareas de mantenimiento de la [cuenta de inicio de sesión](logon-account-maintenance-tasks.md).
2.  Llame a la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) para registrar el SPN del servicio con el servicio de autenticación RPC y especifique el **RPC \_ C \_ authn \_ GSS \_ Negotiate** como el servicio de autenticación que se va a usar.

Para obtener más información acerca de cómo realizar la autenticación mutua en un servicio RPC, consulte [escribir un servidor SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).

**Para autenticar el servicio desde el cliente**

1.  Extraiga el nombre de host del enlace RPC.
2.  Cree el SPN para el servicio mediante una llamada a la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la clase de servicio, el nombre de host DNS y el nombre del servicio. es el nombre distintivo del punto de conexión en el caso de RpcNs.

    Para obtener más información acerca de la creación de un SPN para un servicio RpcNs, consulte [composición de SPN para un servicio RpcNs](composing-spns-for-an-rpcns-service.md).

3.  Configure una [**estructura \_ \_ QoS de seguridad RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) para solicitar la autenticación mutua.
4.  Llame a la función [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para establecer los datos de autenticación para el enlace RPC. El cliente debe solicitar al menos **\_ integridad de \_ nivel de \_ autenticación \_ \_ de RPC C** para asegurarse de que las comunicaciones no se han alterado. Para mayor seguridad, el cliente debe especificar **la \_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** para solicitar el cifrado.
5.  Realizar la llamada RPC.

Para obtener más información sobre cómo realizar la autenticación mutua en un cliente RPC, consulte [escribir un cliente SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).

**Para autenticar el cliente desde el servicio**

1.  Llame a la función [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) para comprobar los parámetros de autenticación especificados por el cliente. Si el cliente no ha solicitado el nivel deseado de autenticación, rechace la llamada. Tenga en cuenta que un servicio RPC debe comprobar el nivel de autenticación, el servicio de autenticación y la identidad del cliente en cada llamada para asegurarse de que el cliente se ha autenticado correctamente.
2.  Llame a la función [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para suplantar al cliente.
3.  Realizar la operación solicitada.
4.  Llame a la función [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) para revertir al contexto de seguridad del servicio.

Para obtener más información acerca de la suplantación de cliente RPC, consulte [suplantación de cliente](/windows/desktop/Rpc/client-impersonation).

Para más información, consulte:

-   [Publicación con el servicio de nombres RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Aspectos básicos de seguridad de RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 