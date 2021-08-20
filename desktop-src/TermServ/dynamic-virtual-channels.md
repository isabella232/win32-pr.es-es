---
title: Canales virtuales dinámicos
description: Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9d5eed9a43f8aad2b48cb1d77c6203ba717ebd306ced688caceac92bbef038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856165"
---
# <a name="dynamic-virtual-channels"></a>Canales virtuales dinámicos

Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC). Las API de DVC abordan varias limitaciones que existían en las API de SVC entre el cliente y el servidor, como:

-   Un número limitado de canales
-   Reconstrucción de paquetes

Las API de DVC le ayudarán a implementar módulos en el lado servidor y cliente de una conexión Servicios de Escritorio remoto que se comunican entre sí.

Al igual que muchas otras arquitecturas de cliente y servidor, se establece una conexión en función de un fragmento de datos comúnmente acordado, denominado punto de conexión. Un ejemplo similar es TCP/IP, donde se establece un punto de conexión a través de una combinación de la dirección IP del servidor y el nombre del puerto. Otro ejemplo son las canalizaciones con nombre, donde un punto de conexión es una combinación del nombre del servidor y el nombre de la canalización. En una Servicios de Escritorio remoto conexión, solo hay dos lados implicados. Por lo tanto, el punto de conexión consta de una cadena arbitraria simple que identifica de forma única la conexión. Al igual que TCP/IP y canalizaciones con nombre, varias conexiones pueden iniciarse desde el mismo nombre de punto de conexión. En ese sentido, las conexiones no tienen nombres; solo un agente de escucha que espera las solicitudes entrantes en el punto de conexión.

Las API de DVC constan de lo siguiente:

-   API de cliente

    Estas API están disponibles en el cliente Conexión a Escritorio remoto (RDC) como complemento. El lado cliente está en modo pasivo, donde escucha las conexiones entrantes, pero no establece activamente una conexión.

-   API de servidor

    Estas API inician activamente la conexión.

Para obtener información sobre cómo escribir un módulo de canal virtual dinámico (DVC), vea [Detalles de implementación de DVC.](dvc-implementation-details.md)

 

 




