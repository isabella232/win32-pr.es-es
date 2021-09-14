---
title: Límites de la firma raíz
description: La firma raíz es el patrimonio real primo y hay límites y costos estrictos que se deben tener en cuenta.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072886"
---
# <a name="root-signature-limits"></a>Límites de la firma raíz

La firma raíz es el patrimonio real primo y hay límites y costos estrictos que se deben tener en cuenta.

-   [Límites y costos de memoria](#memory-limits-and-costs)
-   [Costos de rendimiento](#performance-costs)
-   [Muestreadores estáticos](#static-samplers)
-   [Temas relacionados](#related-topics)

## <a name="memory-limits-and-costs"></a>Límites y costos de memoria

El tamaño máximo de una firma raíz es de 64 DWORD.

Este tamaño máximo se elige para evitar el abuso de la firma raíz como una manera de almacenar datos masivos. Cada entrada de la firma raíz tiene un costo hacia este límite de 64 DWORD:

-   Las tablas de descriptores cuestan 1 DWORD cada una.
-   Las constantes raíz cuestan 1 DWORD cada una, ya que son valores de 32 bits.
-   Los descriptores raíz (direcciones virtuales de GPU de 64 bits) cuestan 2 DWORD cada uno.

Los muestreadores estáticos no tienen ningún costo en el tamaño de la firma raíz.

## <a name="performance-costs"></a>Costos de rendimiento

El costo de rendimiento (en términos de niveles de direccionamiento indirecto) es cero para una constante raíz, 1 para un descriptor raíz y 2 para una tabla de descriptores. Si una firma raíz es grande y se desborda fuera de la memoria más rápida en memoria ligeramente más lenta (lo que puede ocurrir en algún hardware), agregue 1 al costo de rendimiento de los elementos que se desbordan al final de la firma raíz.

Puede producirse un desbordamiento en el hardware que podría tener, por ejemplo, un tamaño fijo de 16 DWORD para el espacio de argumentos raíz. Este límite podría reducirse aún más en uno si se usa el ensamblador de entrada. En este caso, hay desbordamiento en la memoria ligeramente más lenta si la firma raíz es demasiado grande para la memoria nativa DWORD 15 o 16. En otro hardware no hay memoria de argumento raíz nativa fija (por lo que la situación de desbordamiento nunca se produce).

Para todo el hardware, si cambia algún argumento raíz, el controlador debe mantener una versión de todos los argumentos raíz (a diferencia de otros almacenamientos, como los montones de descriptores y los recursos de búfer, que no tienen versiones del controlador). En el hardware en el que se produce una situación de desbordamiento, solo es necesario crear versiones del área nativa o de desbordamiento, en función de dónde se produjo el cambio. Obviamente, la cantidad de control de versiones debe mantenerse al mínimo necesario.

Por lo general, tenga en cuenta las siguientes directrices:

-   Use una firma raíz pequeña según sea necesario, aunque equilibra esto con la flexibilidad de una firma raíz mayor.
-   Organice los parámetros en una firma raíz grande para que los parámetros con más probabilidad de cambiar con frecuencia, o si la latencia de acceso baja para un parámetro determinado es importante, se produzcan primero.
-   Si es conveniente, use constantes raíz o vistas de búfer de constantes raíz sobre la colocación de vistas de búfer constante en un montón de descriptores.

## <a name="static-samplers"></a>Muestreadores estáticos

Los muestreadores estáticos (muestreadores donde el estado está totalmente definido e inmutable) forman parte de las firmas raíz, pero no cuentan para el límite de 64 DWORD. Si un sampler se puede definir como estático, no es necesario que el muestreador forme parte de un montón de descriptores.

El uso de muestreadores estáticos no tiene ningún costo de rendimiento y una firma raíz puede contener una combinación de muestreadores estáticos (almacenados en la firma raíz o en espacio reservado en algún hardware) y muestreadores dinámicos (almacenados en un montón de descriptores de sampler). Los muestreadores de un montón de descriptores se pueden asignar e indexar dinámicamente, lo que no pueden hacer los muestreadores estáticos.

Los muestreadores estáticos se pueden escribir como parte de la firma raíz en sombreadores HLSL (consulte Especificación de firmas raíz [en HLSL).](specifying-root-signatures-in-hlsl.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




