---
title: Rutas y la mejor ruta
description: Una ruta es una ruta de acceso de red \ 0034; \ 0034; a un destino que tiene un costo determinado asociado. El costo se representa mediante sus preferencias administrativas y su métrica específica del protocolo. Las rutas con costos menores son preferibles a las demás rutas.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676272"
---
# <a name="routes-and-the-best-route"></a>Rutas y la mejor ruta

Una ruta es una "ruta de acceso de red" a un destino que tiene un costo concreto asociado. El costo se representa mediante sus preferencias administrativas y su métrica específica del protocolo. Las rutas con costos menores son preferibles a las demás rutas.

Una entrada de ruta en la tabla de enrutamiento incluye:

-   Identificador del destino.
-   Propietario de esta ruta.
-   El vecino (del mismo nivel) que proporcionó la información de ruta
-   Marcas asociadas al estado de la ruta
-   Marcas asociadas a la ruta
-   La preferencia y la métrica de la ruta
-   Lista de vistas a las que pertenece la ruta
-   Información privada para el propietario de la ruta
-   Lista de próximos saltos usados para alcanzar el destino.

Los siguientes valores, que se toman juntos, identifican de forma única una ruta en la tabla de enrutamiento:

-   La red de destino
-   Propietario de la ruta.
-   El vecino que proporcionó la ruta

## <a name="metrics-and-preference"></a>Métricas y preferencias

Cada ruta tiene una preferencia administrativa (especificada por la Directiva de enrutamiento) y una métrica dependiente del cliente. El administrador de tablas de enrutamiento usa esta información para determinar qué ruta es la mejor ruta a un destino. Las rutas con preferencia más baja son rutas mejores (una es la más baja y, por tanto, la mejor opción). Si dos rutas tienen la misma preferencia, la ruta con la métrica inferior es la más adecuada.

Normalmente, la preferencia de una ruta viene determinada por la preferencia del cliente que agregó la ruta. Sin embargo, para las rutas agregadas mediante la herramienta de administración de Netsh.exe, se puede especificar un valor de preferencia en función de cada ruta.

La preferencia se usa normalmente para indicar la prioridad entre los clientes. Por ejemplo, un administrador puede asignar a OSPF una preferencia inferior (mejor) que RIP. En este caso, las rutas OSPF son preferibles a las rutas RIP.

 

 




