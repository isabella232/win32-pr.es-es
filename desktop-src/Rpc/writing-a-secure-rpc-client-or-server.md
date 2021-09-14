---
title: Escritura de un cliente o servidor RPC seguro
description: En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un cliente o servidor RPC seguro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, escritura de un cliente o servidor seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073826"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Escritura de un cliente o servidor RPC seguro

En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un cliente o servidor RPC seguro.

La información de esta sección se aplica a Windows 2000 y Windows XP. Esta sección se aplica a todas las secuencias de protocolo, incluido [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Los desarrolladores tienden a pensar que **ncalrpc** no es un objetivo probable de un ataque, lo que no es cierto en un servidor terminal en el que potencialmente cientos de usuarios tienen acceso a un servicio, y poner en peligro o incluso poner en peligro un servicio puede dar lugar a la adquisición de acceso adicional.

Esta sección se divide en los temas siguientes:

-   [Qué proveedor de seguridad se va a usar](which-security-provider-to-use.md)
-   [Controlar la autenticación de cliente](controlling-client-authentication.md)
-   [Elección de un nivel de autenticación](choosing-an-authentication-level.md)
-   [Elección de las opciones de QOS de seguridad](choosing-security-qos-options.md)
-   [Error común: Suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Devoluciones de llamada](callbacks.md)
-   [Sesiones null](null-sessions.md)
-   [Uso de la marca /robust](use-the-robust-flag.md)
-   [Técnicas de IDL para mejorar la interfaz y el diseño de métodos](idl-techniques-for-better-interface-and-method-design.md)
-   [Identificadores de contexto strict y type strict](strict-and-type-strict-context-handles.md)
-   [No confiar en el mismo nivel](do-not-trust-your-peer.md)
-   [No usar la seguridad de los puntos de conexión](do-not-use-endpoint-security.md)
-   [Tenga cuidado con otros puntos de conexión RPC que se ejecutan en el mismo proceso.](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Compruebe que el servidor Quién que dice ser](verify-the-server-is-who-it-claims-to-be.md)
-   [Usar secuencias de protocolo estándar](use-mainstream-protocol-sequences.md)
-   [¿Qué tan seguro es mi servidor RPC ahora?](how-secure-is-my-rpc-server-now.md)

 

 