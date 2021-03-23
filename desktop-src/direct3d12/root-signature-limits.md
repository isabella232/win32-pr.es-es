---
title: Límites de la firma raíz
description: La firma raíz es una auténtica inmobiliaria y se deben tener en cuenta los límites y costos estrictos.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104095"
---
# <a name="root-signature-limits"></a>Límites de la firma raíz

La firma raíz es una auténtica inmobiliaria y se deben tener en cuenta los límites y costos estrictos.

-   [Límites de memoria y costos](#memory-limits-and-costs)
-   [Costos de rendimiento](#performance-costs)
-   [Muestras estáticas](#static-samplers)
-   [Temas relacionados](#related-topics)

## <a name="memory-limits-and-costs"></a>Límites de memoria y costos

El tamaño máximo de una firma raíz es 64 DWORDs.

Este tamaño máximo se elige para evitar el abuso de la firma raíz como una forma de almacenar los datos en bloque. Cada entrada de la firma raíz tiene un costo para este límite de DWORD 64:

-   Las tablas de descriptores tienen el costo 1 DWORD cada una.
-   Las constantes raíz cuestan 1 DWORD cada una, ya que son valores de 32 bits.
-   Los descriptores raíz (direcciones virtuales de GPU de 64 bits) cuestan 2 DWORDs cada uno.

Los muestreadores estáticos no tienen ningún costo en el tamaño de la firma raíz.

## <a name="performance-costs"></a>Costos de rendimiento

El costo de rendimiento (en términos de niveles de direccionamiento indirecto) es cero para una constante raíz, 1 para un descriptor raíz y 2 para una tabla de descriptores. Si una firma raíz es grande y se desborda de la memoria más rápida en una memoria ligeramente más lenta (lo que puede ocurrir en algún hardware), agregue 1 al costo de rendimiento de los elementos de desbordamiento al final de la firma raíz.

Se puede producir un desbordamiento en el hardware que podría tener, por ejemplo, un tamaño fijo de 16 DWORD para el espacio del argumento raíz. Este límite puede reducirse aún más en uno si se utiliza el ensamblador de entrada. En este caso, se produce un desbordamiento en la memoria ligeramente más lenta si la firma raíz es demasiado grande para la memoria nativa de 15 o 16 DWORD. En otro hardware no existe memoria de argumentos raíz nativa fija (por lo que la situación de desbordamiento nunca se produce).

En todo el hardware, si algún argumento raíz cambia, el controlador debe mantener una versión de todos los argumentos raíz (a diferencia de otro almacenamiento como los montones de descriptor y los recursos de búfer, que no son versiones del controlador). En el hardware en el que se produce una situación de desbordamiento, solo es necesario crear versiones del área nativa o de desbordamiento, en función de dónde se haya producido el cambio. Obviamente, la cantidad de versiones debe mantenerse en el mínimo necesario.

En general, tenga en cuenta las siguientes directrices:

-   Use una firma raíz pequeña según sea necesario, pero equilibre esto con la flexibilidad de una firma raíz más grande.
-   Organice los parámetros en una firma raíz de gran tamaño para que los parámetros con más probabilidades de cambiar con frecuencia, o si la latencia de acceso bajo para un parámetro determinado es importante, se produzca primero.
-   Si es conveniente, use constantes raíz o vistas de búfer de constantes raíz en lugar de colocar vistas de búfer constantes en un montón de descriptores.

## <a name="static-samplers"></a>Muestras estáticas

Los muestreadores estáticos (muestreadores en los que el estado es totalmente definido e inmutable) forman parte de las firmas raíz, pero no cuentan para el límite DWORD 64. Si una muestra se puede definir como estática, no es necesario que la muestra forme parte de un montón de descriptores.

El uso de muestras estáticas no supone ningún costo de rendimiento, y una firma raíz puede contener una combinación de muestras estáticas (almacenadas en la firma raíz o en espacio reservado en algún hardware) y muestreadores dinámicos (almacenados en un montón de descriptores de muestra). Los muestreadores de un montón de descriptores se pueden asignar y indexar dinámicamente, lo que los ejemplos estáticos no pueden.

Los muestreadores estáticos se pueden escribir como parte de la firma raíz en los sombreadores HLSL (consulte [especificación de firmas raíz en HLSL](specifying-root-signatures-in-hlsl.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




