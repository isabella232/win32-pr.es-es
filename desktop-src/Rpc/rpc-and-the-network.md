---
title: RPC y la red
description: En esta sección se describe cómo tratar la no confiabilidad de la red cuando se usa RPC y se explica cómo las API de nivel de RPC se traducen en la actividad de red. La sección solo se refiere a \_ las \_ secuencias de protocolo TCP IP ncacn y ncacn \_ http.
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC (llamada a procedimiento remoto), procedimientos recomendados, RPC y la red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149501"
---
# <a name="rpc-and-the-network"></a>RPC y la red

En esta sección se describe cómo tratar la no confiabilidad de la red cuando se usa RPC y se explica cómo las API de nivel de RPC se traducen en la actividad de red. La sección solo se refiere a las secuencias de protocolo [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) .

Esta sección se divide en los temas siguientes:

-   [Desarrollo frente a implementación en la red](development-versus-deployment-in-the-network.md)
-   [Evitar bloqueos Client-Side](preventing-client-side-hangs.md)
-   [Administración de conjuntos de conexiones de red (asociaciones)](managing-network-connection-sets-associations-.md)
-   [Limpieza de conexión inactiva](idle-connection-cleanup.md)
-   [Tratamiento de la pérdida de conectividad](dealing-with-loss-of-connectivity.md)
-   [Limpieza del lado servidor](server-side-cleanup.md)

 

 