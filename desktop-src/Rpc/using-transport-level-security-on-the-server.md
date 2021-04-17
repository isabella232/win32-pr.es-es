---
title: Usar la seguridad de nivel de transporte en el servidor
description: Usar la seguridad de nivel de transporte en el servidor con llamada a procedimiento remoto (RPC).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de la seguridad de nivel de transporte en el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39af5b8fb43a57683804eb7b91067ca9faad4390
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487867"
---
# <a name="using-transport-level-security-on-the-server"></a>Usar la seguridad de nivel de transporte en el servidor

En esta sección se presentan los debates sobre la seguridad de nivel de transporte, divididos en los temas siguientes:

-   [Usar la seguridad de Transport-Level en el cliente](using-transport-level-security-on-the-client.md)

Cuando se usa [ncacn \_ NP](/windows/desktop/Midl/ncacn-np) o [ncalrpc](/windows/desktop/Midl/ncalrpc) como secuencia de protocolos, el servidor especifica un descriptor de seguridad para el punto de conexión en el momento en que selecciona la secuencia del protocolo. Para obtener más información sobre las secuencias de protocolo, consulte [especificar secuencias de protocolos](specifying-protocol-sequences.md). La aplicación proporciona el descriptor de seguridad como parámetro adicional (una extensión para los parámetros estándar de OSF-DCE) en todas las funciones que empiezan con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). El descriptor de seguridad controla si un cliente puede conectarse al punto de conexión.

Cada proceso y subproceso está asociado a un token de seguridad. Este token incluye un descriptor de seguridad predeterminado que se usa para los objetos que crea el proceso, como el punto de conexión. Si la aplicación no especifica un descriptor de seguridad al llamar a una función con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), la biblioteca en tiempo de ejecución de RPC aplica el descriptor de seguridad predeterminado del token de seguridad del proceso al extremo.

Para garantizar que todos los clientes pueden tener acceso a la aplicación de servidor, el administrador debe iniciar la aplicación de servidor en un proceso que tenga un descriptor de seguridad predeterminado que todos los clientes puedan usar. Por lo general, solo los procesos del sistema tienen un descriptor de seguridad predeterminado.

Para obtener más información sobre estas funciones y las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 