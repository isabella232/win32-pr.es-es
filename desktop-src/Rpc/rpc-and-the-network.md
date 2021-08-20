---
title: RPC y la red
description: En esta sección se describe cómo tratar la responsabilidad de la red al usar RPC y se explica cómo las API de nivel de RPC se traducen en actividad de red. La sección solo hace referencia a las secuencias de protocolo http ncacn \_ ip \_ tcp y ncacn. \_
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, RPC y la red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212e1f3b6f281709a3344367a59d858b7f96b77a6adbdc44fc8556769f2edcaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926657"
---
# <a name="rpc-and-the-network"></a>RPC y la red

En esta sección se describe cómo tratar la responsabilidad de la red al usar RPC y se explica cómo las API de nivel de RPC se traducen en actividad de red. La sección solo hace referencia a las secuencias de [**protocolo http ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn. \_**](/windows/desktop/Midl/ncacn-http)

Esta sección se divide en los temas siguientes:

-   [Desarrollo frente a implementación en la red](development-versus-deployment-in-the-network.md)
-   [Evitar Client-Side de error](preventing-client-side-hangs.md)
-   [Administración de conjuntos de conexiones de red (asociaciones)](managing-network-connection-sets-associations-.md)
-   [Limpieza de conexión inactiva](idle-connection-cleanup.md)
-   [Tratamiento de la pérdida de conectividad](dealing-with-loss-of-connectivity.md)
-   [Limpieza del lado servidor](server-side-cleanup.md)

 

 