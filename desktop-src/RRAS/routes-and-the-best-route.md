---
title: Rutas y la mejor ruta
description: Una ruta es \ 0034;ruta de acceso de red \ 0034; a un destino que tiene un costo determinado asociado. El costo se representa por su preferencia administrativa y su métrica específica del protocolo. Las rutas con costos más bajos son preferibles a las demás rutas.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78d03821ad767561441b7fc853ebac73af420ef6c239456b1d4fac59e244af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081065"
---
# <a name="routes-and-the-best-route"></a>Rutas y la mejor ruta

Una ruta es una "ruta de acceso de red" a un destino que tiene un costo determinado asociado. El costo se representa por su preferencia administrativa y su métrica específica del protocolo. Las rutas con costos más bajos son preferibles a las demás rutas.

Una entrada de ruta en la tabla de enrutamiento incluye:

-   Identificador del destino
-   Propietario de esta ruta
-   Vecino (del mismo nivel) que proporcionó la información de ruta
-   Marcas asociadas al estado de la ruta
-   Marcas asociadas a la ruta
-   Preferencia y métrica de la ruta
-   Lista de vistas a las que pertenece la ruta
-   Información privada para el propietario de la ruta
-   Lista de próximo saltos usados para llegar al destino

Los siguientes valores, tomados juntos, identifican de forma única una ruta en la tabla de enrutamiento:

-   La red de destino
-   Propietario de la ruta
-   El vecino que proporcionó la ruta

## <a name="metrics-and-preference"></a>Métricas y preferencias

Cada ruta tiene una preferencia administrativa (especificada por la directiva de enrutamiento) y una métrica dependiente del cliente. El administrador de tablas de enrutamiento usa esta información para determinar qué ruta es la mejor ruta a un destino. Las rutas con preferencias más bajas son mejores rutas (una es la más baja y, por tanto, la mejor). Si dos rutas tienen la misma preferencia, la ruta con la métrica inferior es la mejor.

Normalmente, la preferencia de una ruta viene determinada por la preferencia del cliente que agregó la ruta. Sin embargo, para las rutas agregadas mediante la herramienta Netsh.exe administración, se puede especificar un valor de preferencia por ruta.

Normalmente, las preferencias se usan para indicar la prioridad entre los clientes. Por ejemplo, un administrador puede asignar a OSPF una preferencia menor (mejor) que RIP. En este caso, las rutas OSPF son preferibles a las rutas RIP.

 

 




