---
title: Escritura de un cliente o servidor RPC seguro
description: En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un servidor o cliente RPC seguro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, escribir un cliente o servidor seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078115"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Escritura de un cliente o servidor RPC seguro

En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un servidor o cliente RPC seguro.

La información de esta sección se aplica a Windows 2000 y Windows XP. Esta sección se aplica a todas las secuencias de protocolos, incluido [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Los desarrolladores suelen pensar en que **ncalrpc** no es un objetivo probable para un ataque, lo que no es cierto en un servidor de Terminal Server donde puede haber cientos de usuarios que tengan acceso a un servicio y poner en peligro o incluso detener un servicio puede llevar a adquirir acceso adicional.

Esta sección se divide en los temas siguientes:

-   [Qué proveedor de seguridad usar](which-security-provider-to-use.md)
-   [Controlar la autenticación del cliente](controlling-client-authentication.md)
-   [Elección de un nivel de autenticación](choosing-an-authentication-level.md)
-   [Elegir opciones de QOS de seguridad](choosing-security-qos-options.md)
-   [Error común: suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Devoluciones de llamada](callbacks.md)
-   [Sesiones nulas](null-sessions.md)
-   [Usar la marca/Robust](use-the-robust-flag.md)
-   [Técnicas de IDL para mejorar el diseño de la interfaz y el método](idl-techniques-for-better-interface-and-method-design.md)
-   [Identificadores de contexto STRICT y Type STRICT](strict-and-type-strict-context-handles.md)
-   [No confíe en su equipo del mismo nivel](do-not-trust-your-peer.md)
-   [No usar seguridad de extremo](do-not-use-endpoint-security.md)
-   [Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Compruebe que el servidor es quien dice ser](verify-the-server-is-who-it-claims-to-be.md)
-   [Usar secuencias de protocolo estándar](use-mainstream-protocol-sequences.md)
-   [¿Es seguro ahora mi servidor RPC?](how-secure-is-my-rpc-server-now.md)

 

 