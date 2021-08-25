---
description: Las aplicaciones deben sincronizar el acceso a las variables que comparten varios subprocesos.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Acceso a variables entrelazado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b298dffe45d1a0de655e225c8a240dd72be15a0fff7e4d6eac25ebb0a1130ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126325"
---
# <a name="interlocked-variable-access"></a>Acceso a variables entrelazado

Las aplicaciones deben sincronizar el acceso a las variables que comparten varios subprocesos. Las aplicaciones también deben asegurarse de que las operaciones en estas variables se realizan de forma atómica (se realizan en su totalidad o no).

Las lecturas y escrituras simples en variables de 32 bits alineadas correctamente son operaciones atómicas. En otras palabras, no terminará con una sola parte de la variable actualizada; todos los bits se actualizan de forma atómica. Sin embargo, no se garantiza que el acceso se sincronice. Si dos subprocesos leen y escriben desde la misma variable, no puede determinar si un subproceso realizará su operación de lectura antes de que el otro realice su operación de escritura.

Las lecturas y escrituras simples en variables de 64 bits alineadas correctamente son atómicas en variables de 64 Windows. No se garantiza que las lecturas y escrituras en valores de 64 bits sean atómicas en valores de 32 Windows. No se garantiza que las lecturas y escrituras en variables de otros tamaños sean atómicas en ninguna plataforma.

## <a name="the-interlocked-api"></a>La API entrelazado

Las funciones entrelazados proporcionan un mecanismo sencillo para sincronizar el acceso a una variable compartida por varios subprocesos. También realizan operaciones en variables de forma atómica. Los subprocesos de distintos procesos pueden usar estas funciones si la variable está en memoria compartida.

Las [**funciones InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinan los pasos necesarios para incrementar o disminuir una variable en una operación atómica. Esta característica es útil en un sistema operativo multitarea, en el que el sistema puede interrumpir la ejecución de un subproceso para conceder un segmento de tiempo de procesador a otro subproceso. Sin esta sincronización, dos subprocesos podrían leer el mismo valor, incrementarlo en 1 y almacenar el nuevo valor para un aumento total de 1 en lugar de 2. Las funciones de acceso variable entrelazado protegen contra este tipo de error.

Las [**funciones InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) e [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) intercambian de forma atómica los valores de las variables especificadas. La [**función InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combina dos operaciones: agregar dos variables juntas y almacenar el resultado en una de las variables.

Las funciones [**InterlockedCompareExchange,**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange) [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))e [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinan dos operaciones: comparar dos valores y almacenar un tercer valor en una de las variables, en función del resultado de la comparación.

Las [**funciones InterlockedAnd,**](/windows/win32/api/winnt/nf-winnt-interlockedand) [**InterlockedOr**](/windows/win32/api/winnt/nf-winnt-interlockedor)e [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) realizan de forma atómica operaciones AND, OR y XOR, respectivamente.

Hay funciones diseñadas específicamente para realizar el acceso a variables entrelazado en direcciones y valores de memoria de 64 bits, y están optimizadas para su uso en direcciones de 64 Windows. Cada una de estas funciones contiene "64" en el nombre; por ejemplo, [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) e [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

La mayoría de las funciones entrelazados proporcionan barreras de memoria completa en todas Windows plataformas. También hay funciones que combinan las operaciones básicas de acceso a variables entrelazados con la semántica de ordenación de la memoria de adquisición y liberación admitida por determinados procesadores. Cada una de estas funciones contiene la palabra "Acquire" o "Release" en sus nombres; por ejemplo, [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) [**e InterlockedDecrementRelease.**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)) Adquirir semántica de memoria especifica que la operación de memoria que realiza el subproceso actual será visible antes de que se realicen otras operaciones de memoria. La semántica de la memoria de liberación especifica que la operación de memoria que realiza el subproceso actual será visible después de que se hayan completado todas las demás operaciones de memoria. Esta semántica le permite forzar que las operaciones de memoria se realicen en un orden específico. Use adquirir semántica al especificar una región protegida y liberar semántica al salir de ella.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Intrínsecos del controlador](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Problemas de sincronización y multiprocesador](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
