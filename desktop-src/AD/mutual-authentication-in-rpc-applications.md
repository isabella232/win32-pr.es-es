---
title: Autenticación mutua en aplicaciones RPC
description: Los servicios RPC pueden usar puntos de conexión de servicio para publicarse, o bien pueden usar las API del servicio de nombres RPC (RPCN).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en RPC Applications AD
- Active Directory, Uso, Autenticación mutua, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c7d5ea3632d08671861b72267419efd54c1a6a89770fbde72543596b29fa8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186060"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Autenticación mutua en aplicaciones RPC

Los servicios RPC pueden usar puntos de conexión de servicio para publicarse, o bien pueden usar las API del servicio de nombres RPC (RPCN). En este tema se describe cómo realizar la autenticación mutua con un servicio RPC que se publica a sí mismo mediante las API del servicio de nombres RPC (RPCN).

**Para registrar un SPN en el directorio**

1.  Llame a [**la función DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear un nombre de entidad de seguridad de servicio (SPN) para el servicio.
2.  Llame a [**la función DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar el SPN en la cuenta de servicio o en la cuenta de equipo en cuyo contexto se ejecutará el servicio.

**Para registrar un servicio con el servicio de nomenclatura RPC**

1.  Compruebe que los SPN adecuados están registrados en la cuenta con la que se ejecuta el servicio. Para obtener más información, vea [Tareas de mantenimiento de cuentas de inicio de sesión.](logon-account-maintenance-tasks.md)
2.  Llame a [**la función RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) para registrar el SPN de servicio con el servicio de autenticación RPC y especifique **RPC C \_ \_ \_ AUTHN GSS \_ NEGOTIATE** como el servicio de autenticación que se usará.

Para obtener más información sobre cómo realizar la autenticación mutua en un servicio RPC, vea [Escribir un servidor SSPI autenticado.](/windows/desktop/Rpc/writing-an-authenticated-sspi-server)

**Para autenticar el servicio desde el cliente**

1.  Extraiga el nombre de host del enlace RPC.
2.  Cree el SPN para el servicio mediante una llamada a la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la clase de servicio, el nombre de host DNS y el nombre del servicio; que es el nombre distintivo del punto de conexión en el caso de rpcN.

    Para obtener más información sobre cómo crear un SPN para un servicio RpcNs, vea Composición de [SPN para un servicio RpcNs](composing-spns-for-an-rpcns-service.md).

3.  Configure una estructura [**DE \_ \_ QOS de SEGURIDAD RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) para solicitar la autenticación mutua.
4.  Llame a [**la función RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para establecer los datos de autenticación para el enlace RPC. El cliente debe solicitar al menos **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** para asegurarse de que las comunicaciones no se han alterado. Para aumentar la seguridad, el cliente debe especificar **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** para solicitar el cifrado.
5.  Realice la llamada RPC.

Para obtener más información sobre cómo realizar la autenticación mutua en un cliente RPC, vea [Escribir un cliente SSPI autenticado.](/windows/desktop/Rpc/writing-an-authenticated-sspi-client)

**Para autenticar el cliente desde el servicio**

1.  Llame a [**la función RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) para comprobar los parámetros de autenticación especificados por el cliente. Si el cliente no ha solicitado el nivel deseado de autenticación, rechace la llamada. Tenga en cuenta que un servicio RPC debe comprobar el nivel de autenticación, el servicio de autenticación y la identidad de cliente en cada llamada para asegurarse de que el cliente se ha autenticado correctamente.
2.  Llame a [**la función RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para suplantar al cliente.
3.  Realice la operación solicitada.
4.  Llame a [**la función RpcRevertToSelf para**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) revertir al contexto de seguridad del servicio.

Para obtener más información sobre la suplantación de cliente RPC, vea [Suplantación de cliente.](/windows/desktop/Rpc/client-impersonation)

Para más información, consulte:

-   [Publicación con el servicio de nombres RPC (RPCN)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Aspectos básicos de la seguridad de RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 