---
title: Canales virtuales dinámicos
description: Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418657"
---
# <a name="dynamic-virtual-channels"></a>Canales virtuales dinámicos

Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC). Las API de DVC abordan varias limitaciones que existían en las API de SVC entre el cliente y el servidor, por ejemplo:

-   Un número limitado de canales
-   Reconstrucción de paquetes

Las API de DVC le ayudarán a implementar módulos en el lado servidor y cliente de una conexión Servicios de Escritorio remoto que se comunican entre sí.

Al igual que muchas otras arquitecturas de cliente/servidor, se establece una conexión basada en un elemento de datos acordado comúnmente, denominado punto de conexión. Un ejemplo similar es TCP/IP, donde un punto de conexión se establece a través de una combinación de dirección IP del servidor y el nombre del puerto. Otro ejemplo son las canalizaciones con nombre, donde un punto de conexión es una combinación del nombre del servidor y el nombre de la canalización. En una conexión Servicios de Escritorio remoto solo hay dos lados implicados. Por lo tanto, el punto de conexión consta de una cadena arbitraria simple que identifica la conexión de forma única. Al igual que TCP/IP y las canalizaciones con nombre, se pueden iniciar varias conexiones desde el mismo nombre de punto de conexión. En ese sentido, las conexiones no tienen nombres; solo un agente de escucha que espera las solicitudes entrantes en el extremo.

Las API de DVC se componen de lo siguiente:

-   API de cliente

    Estas API están disponibles en el cliente de Conexión a Escritorio remoto (RDC) como complemento. El lado cliente está en modo pasivo, donde escucha las conexiones entrantes, pero no establece activamente una conexión.

-   API de servidor

    Estas API inician activamente la conexión.

Para obtener información sobre cómo escribir un módulo de canal virtual dinámico (DVC), consulte los [detalles de implementación de DVC](dvc-implementation-details.md).

 

 




