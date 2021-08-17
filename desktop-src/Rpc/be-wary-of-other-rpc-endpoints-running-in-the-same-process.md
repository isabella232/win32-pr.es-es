---
title: Tenga cuidado con otros puntos de conexión RPC que se ejecutan en el mismo proceso
description: Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2044b83de96a352546d90c45cd54879fc87923786b7852133ffeb28dbf9cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932356"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Tenga cuidado con otros puntos de conexión RPC que se ejecutan en el mismo proceso

Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos. Por lo tanto, si un componente llama a [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) solo para LRPC, no es necesariamente accesible \* solo a través de LRPC. Puede ser accesible a través de otros protocolos, ya que otros servidores RPC del proceso pueden estar escuchando en canalizaciones o sockets (por ejemplo).

De forma similar a los identificadores de contexto estrictos, no colocar otro punto de conexión en el proceso no significa que no exista otro punto de conexión. Independientemente de cómo registre el servidor, no hay ninguna asociación especial entre la interfaz y el punto de conexión. todas las interfaces se pueden llamar en todos los puntos de conexión de ese proceso. Este es otro motivo por el que el modelo de seguridad del punto de conexión no es eficaz; Si se coloca un descriptor de seguridad en un punto de conexión, los atacantes pueden llamar a la interfaz en otro punto de conexión.

Para asegurarse de que solo se llame a un proceso en una secuencia de protocolo específica, registre una función de devolución de llamada de seguridad y, en esa función, compruebe en qué secuencia de protocolo se realiza la llamada.

 

 




