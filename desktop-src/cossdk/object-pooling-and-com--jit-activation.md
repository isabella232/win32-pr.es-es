---
description: La activación JIT de COM+ básicamente pone en peligro a los clientes expansidores y los servidores expansiones para obtener un rendimiento óptimo. Los clientes obtienen para mantener las referencias de objeto, mientras que los servidores pueden administrar más estrechamente el uso de memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Agrupación de objetos y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a61534d19559c5d3492cd73f99fe65cf837c059d5f58b226d56a6cd301d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306153"
---
# <a name="object-pooling-and-com-jit-activation"></a>Agrupación de objetos y activación JIT de COM+

La activación JIT de COM+ básicamente pone en peligro a los clientes expansidores y los servidores expansiones para obtener un rendimiento óptimo. Los clientes obtienen para mantener las referencias de objeto, mientras que los servidores pueden administrar más estrechamente el uso de memoria.

Puede refinar esto aún más mediante la [agrupación de objetos COM+.](com--object-pooling.md) Al agrupar objetos que están activados JIT, puede dedicar una determinada cantidad de memoria para contener un determinado número de objetos activos en la memoria, listos para su reutilización inmediata. Esto tiene más sentido cuando los objetos son caros de crear, como en el caso en el que tienen varios recursos.

La agrupación de objetos activados por JIT de esta manera le permite obtener las siguientes ventajas:

-   Tiempos de reactivación de objetos muy acelerados.
-   Reutilización de los recursos costosos que los objetos están manteniendo.
-   Control más preciso del uso de memoria y recursos para los objetos agrupados.
-   Retención de flexibilidad administrativa para que la aplicación se pueda escalar para usar los recursos disponibles y adaptarse a los cambiantes requisitos de rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Agrupación de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transacciones y activación JIT de COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



