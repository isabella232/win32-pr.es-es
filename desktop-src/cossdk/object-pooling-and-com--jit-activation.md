---
description: La activación JIT de COM+ se pone en peligro entre los clientes expansivos y los servidores expansivos con el fin de obtener un rendimiento óptimo. Los clientes obtienen referencias a objetos, mientras que los servidores pueden administrar con mayor precisión el uso de memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Agrupación de objetos y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423491"
---
# <a name="object-pooling-and-com-jit-activation"></a>Agrupación de objetos y activación JIT de COM+

La activación JIT de COM+ se pone en peligro entre los clientes expansivos y los servidores expansivos con el fin de obtener un rendimiento óptimo. Los clientes obtienen referencias a objetos, mientras que los servidores pueden administrar con mayor precisión el uso de memoria.

Puede refinar aún más mediante el uso de la [agrupación de objetos com+](com--object-pooling.md). Al agrupar los objetos que están activados con JIT, puede dedicar una determinada cantidad de memoria para almacenar un cierto número de objetos activos en la memoria, listos para su reutilización inmediata. Esto resulta más útil cuando los objetos son caros de crear, como en el caso de que contengan varios recursos.

Agrupar objetos activados con JIT de esta manera, puede lograr las siguientes ventajas:

-   Tiempos de reactivación de objetos muy acelerados.
-   Reutilización de los recursos caros que contienen los objetos.
-   Un control más preciso de la memoria y el uso de recursos para los objetos agrupados.
-   Retención de flexibilidad administrativa para que la aplicación pueda escalar para usar los recursos disponibles y adaptarse al cambio de los requisitos de rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Agrupación de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Habilitar la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transacciones y activación JIT de COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



