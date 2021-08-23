---
title: Usar la seguridad de nivel de transporte en el servidor
description: Usar la seguridad de nivel de transporte en el servidor con llamada a procedimiento remoto (RPC).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- Remote Procedure Call RPC , tasks, using transport-level security on the server (Llamada a procedimiento remoto a RPC, tareas, mediante seguridad de nivel de transporte en el servidor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010593"
---
# <a name="using-transport-level-security-on-the-server"></a>Usar la seguridad de nivel de transporte en el servidor

En esta sección se presentan los debates sobre la seguridad de nivel de transporte, divididos en los temas siguientes:

-   [Usar Transport-Level seguridad en el cliente](using-transport-level-security-on-the-client.md)

Cuando se usa [ncacn \_ np](/windows/desktop/Midl/ncacn-np) o [ncalrpc](/windows/desktop/Midl/ncalrpc) como secuencia de protocolo, el servidor especifica un descriptor de seguridad para el punto de conexión en el momento en que selecciona la secuencia de protocolo. Para obtener más información sobre las secuencias de protocolo, vea [Especificar secuencias de protocolo.](specifying-protocol-sequences.md) La aplicación proporciona el descriptor de seguridad como un parámetro adicional (una extensión a los parámetros estándar de OSF-DCE) en todas las funciones que comienzan por los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) El descriptor de seguridad controla si un cliente puede conectarse al punto de conexión.

Cada proceso y subproceso está asociado a un token de seguridad. Este token incluye un descriptor de seguridad predeterminado que se usa para los objetos que crea el proceso, como el punto de conexión. Si la aplicación no especifica un descriptor de seguridad al llamar a una función con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)la biblioteca en tiempo de ejecución de RPC aplica el descriptor de seguridad predeterminado del token de seguridad del proceso al punto de conexión.

Para garantizar que la aplicación de servidor sea accesible para todos los clientes, el administrador debe iniciar la aplicación de servidor en un proceso que tenga un descriptor de seguridad predeterminado que puedan usar todos los clientes. Por lo general, solo los procesos del sistema tienen un descriptor de seguridad predeterminado.

Para obtener más información sobre estas funciones y las [**funciones RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 