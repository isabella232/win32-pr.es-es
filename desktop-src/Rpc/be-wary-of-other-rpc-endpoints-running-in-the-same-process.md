---
title: Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso
description: Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777107"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso

Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos. Como tal, si un componente llama a [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* solo para lrpc, no es necesariamente accesible a través de lrpc. Puede ser accesible a través de otros protocolos, ya que es posible que otros servidores RPC del proceso estén escuchando en canalizaciones o Sockets (por ejemplo,).

De forma similar a los identificadores de contexto estrictos, no colocar otro extremo en el proceso no significa que no exista otro extremo. Independientemente de cómo registre el servidor, no hay ninguna asociación especial entre la interfaz y el punto de conexión; todas las interfaces son Invocables en todos los puntos de conexión de ese proceso. Este es otro motivo por el que el modelo de seguridad del extremo es ineficaz. Si un descriptor de seguridad se coloca en un punto de conexión, los atacantes pueden llamar a la interfaz en otro punto de conexión.

Para asegurarse de que se llame a un proceso solo en una secuencia de protocolo específica, registre una función de devolución de llamada de seguridad y, en esa función, compruebe en qué secuencia de protocolos se realiza la llamada.

 

 




