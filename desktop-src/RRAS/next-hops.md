---
title: Próximo salto
description: Las rutas tienen uno o varios saltos siguientes asociados.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a8d73a0d553773537ca2efd67457498ff9710cf9e7834d6952fcf2a81c5c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790105"
---
# <a name="next-hops"></a>Próximo salto

Las rutas tienen uno o varios saltos siguientes asociados. Si el destino no está en una red conectada directamente, el próximo salto es la dirección del siguiente enrutador (o red) de la red saliente que mejor puede enrutar los datos al destino. La mejor ruta es la que tiene el menor costo, en función de la directiva de enrutamiento en uso. Cada próximo salto se puede usar para reenviar datos en la ruta de acceso al destino. Todas las rutas propiedad de un cliente comparten un conjunto común de entradas de próximo salto agregadas por el cliente.

Cada próximo salto se identifica de forma única por la dirección del próximo salto y el índice de interfaz utilizado para alcanzar el próximo salto.

Si el próximo salto no está conectado directamente, se marca como un próximo salto "remoto". En este caso, el reenviador debe realizar otra búsqueda mediante la dirección de red del próximo salto. Esta búsqueda es necesaria para buscar el próximo salto "local" que se usa para alcanzar el próximo salto remoto y el destino.

Una entrada de próximo salto en la tabla de enrutamiento incluye:

-   Dirección de red del próximo salto
-   Propietario del próximo salto
-   Identificador de la interfaz saliente
-   Estado del próximo salto
-   Marcas asociadas al próximo salto
-   Información privada para el propietario del próximo salto
-   Identificador del destino correspondiente al próximo salto remoto

 

 




