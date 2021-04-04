---
title: Próximos saltos
description: Las rutas tienen uno o más saltos próximos asociados.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075201"
---
# <a name="next-hops"></a>Próximos saltos

Las rutas tienen uno o más saltos próximos asociados. Si el destino no está en una red conectada directamente, el próximo salto es la dirección del siguiente enrutador (o red) de la red de salida que puede enrutar mejor los datos al destino. La mejor ruta es la ruta que tiene el menor costo, en función de la Directiva de enrutamiento en uso. Cada próximo salto se puede usar para reenviar los datos de la ruta de acceso al destino. Todas las rutas que posee un cliente comparten un conjunto común de entradas de próximo salto agregadas por el cliente.

Cada próximo salto se identifica de forma única mediante la dirección del próximo salto y el índice de interfaz que se usa para alcanzar el próximo salto.

Si el próximo salto no se conecta directamente, se marca como un próximo salto "remoto". En este caso, el reenviador debe realizar otra búsqueda mediante la dirección de red del próximo salto. Esta búsqueda es necesaria para encontrar el próximo salto "local" que se usa para alcanzar el próximo salto remoto y el destino.

Una entrada de próximo salto en la tabla de enrutamiento incluye:

-   La dirección de red del próximo salto
-   Propietario del próximo salto.
-   El identificador de la interfaz de salida.
-   Estado del próximo salto
-   Marcas asociadas al próximo salto
-   Información privada para el propietario del próximo salto
-   Identificador del destino correspondiente al próximo salto remoto.

 

 




