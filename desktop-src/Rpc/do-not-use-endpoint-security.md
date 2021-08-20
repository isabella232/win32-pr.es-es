---
title: No usar Endpoint Security
description: La seguridad de los puntos de conexión es un modelo de seguridad en el que se proporciona un descriptor de seguridad cuando se crea un punto de conexión con el grupo RpcServerUseProtseq\ de funciones RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930702"
---
# <a name="do-not-use-endpoint-security"></a>No usar Endpoint Security

La seguridad de los puntos de conexión es un modelo de seguridad en el que se proporciona un descriptor de seguridad cuando se crea un punto de conexión con el grupo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* de funciones RPC. No use este modelo de seguridad. No dé descriptores de seguridad a esas funciones. En el mejor de los casos, este método es una pérdida de recursos de CPU. En el peor de los casos, en muchos entornos es posible sortear el descriptor de seguridad, como ejemplifica la sección Be [Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) (Tener cuidado con otros puntos de conexión RPC que se ejecutan en el mismo proceso).

La seguridad del punto de conexión solo existe por compatibilidad con versiones anteriores.

 

 




