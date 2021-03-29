---
title: No usar seguridad de extremo
description: La seguridad del punto de conexión es un modelo de seguridad en el que se proporciona un descriptor de seguridad cuando se crea un punto de conexión con el grupo de funciones RPC RpcServerUseProtseq \.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775498"
---
# <a name="do-not-use-endpoint-security"></a>No usar seguridad de extremo

La seguridad del punto de conexión es un modelo de seguridad en el que se proporciona un descriptor [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) de seguridad cuando se crea un punto de conexión con el \* grupo de RPCSERVERUSEPROTSEQ de funciones RPC. No utilice este modelo de seguridad. No proporcione descriptores de seguridad a esas funciones. Como es mejor, este método es un desperdicio de recursos de CPU. En el peor de los entornos, es posible eludir el descriptor de seguridad, ya que los [puntos de conexión RPC que se ejecutan en la misma](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) sección de proceso ejemplifican.

La seguridad del punto de conexión solo existe para la compatibilidad con versiones anteriores.

 

 




