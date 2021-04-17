---
description: Las aplicaciones deben sincronizar el acceso a las variables compartidas por varios subprocesos.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Acceso a variables entrelazadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2e083d3e3420e870ad9781b0d262df3d0786f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667977"
---
# <a name="interlocked-variable-access"></a>Acceso a variables entrelazadas

Las aplicaciones deben sincronizar el acceso a las variables compartidas por varios subprocesos. Las aplicaciones también deben asegurarse de que las operaciones en estas variables se realizan de forma atómica (se realizan en su totalidad o no).

Las lecturas y escrituras simples en las variables de 32 bits con una alineación correcta son operaciones atómicas. En otras palabras, no terminará con solo una parte de la variable actualizada; todos los bits se actualizan de forma atómica. Sin embargo, no se garantiza que el acceso esté sincronizado. Si dos subprocesos leen y escriben desde la misma variable, no puede determinar si un subproceso realizará su operación de lectura antes de que el otro realice su operación de escritura.

Las lecturas y escrituras simples en las variables de 64 bits alineadas correctamente son atómicas en Windows de 64 bits. No se garantiza que las lecturas y escrituras en valores de 64 bits sean atómicas en Windows de 32 bits. No se garantiza que las lecturas y escrituras en variables de otros tamaños sean atómicas en ninguna plataforma.

## <a name="the-interlocked-api"></a>La API entrelazada

Las funciones entrelazadas proporcionan un mecanismo sencillo para sincronizar el acceso a una variable compartida por varios subprocesos. También realizan operaciones en variables de una manera atómica. Los subprocesos de diferentes procesos pueden usar estas funciones si la variable está en la memoria compartida.

Las funciones [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) y [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinan los pasos necesarios para aumentar o disminuir una variable en una operación atómica. Esta característica es útil en un sistema operativo multitarea, en el que el sistema puede interrumpir la ejecución de un subproceso para conceder un segmento de tiempo de procesador a otro subproceso. Sin esta sincronización, dos subprocesos podrían leer el mismo valor, incrementarlo en 1 y almacenar el nuevo valor para un aumento total de 1 en lugar de 2. Las funciones de acceso variable entrelazadas protegen frente a este tipo de error.

Las funciones [**InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) y [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) intercambian atómicamente los valores de las variables especificadas. La función [**InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combina dos operaciones: agregar dos variables juntas y almacenar el resultado en una de las variables.

Las funciones [**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))y [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinan dos operaciones: comparar dos valores y almacenar un tercer valor en una de las variables, en función del resultado de la comparación.

Las [](/windows/win32/api/winnt/nf-winnt-interlockedand)funciones InterlockedAnd [**, interlocker**](/windows/win32/api/winnt/nf-winnt-interlockedor)y [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) realizan atómicamente las operaciones and, or y XOR, respectivamente.

Hay funciones que se han diseñado específicamente para realizar el acceso a variables entrelazadas en las direcciones y valores de memoria de 64 bits y se optimizan para su uso en Windows de 64 bits. Cada una de estas funciones contiene "64" en el nombre; por ejemplo, [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) y [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

La mayoría de las funciones entrelazadas proporcionan barreras de memoria completas en todas las plataformas de Windows. También hay funciones que combinan las operaciones básicas de acceso variable de interbloqueo con la semántica de orden de la memoria de adquisición y liberación que admiten determinados procesadores. Cada una de estas funciones contiene la palabra "adquire" o "release" en sus nombres; por ejemplo, [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) y [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). Adquirir la semántica de memoria especifique que la operación de memoria que realiza el subproceso actual será visible antes de que se intenten otras operaciones de memoria. La semántica de liberación de memoria especifica que la operación de memoria que realiza el subproceso actual será visible una vez completadas todas las demás operaciones de memoria. Esta semántica permite forzar la realización de operaciones de memoria en un orden específico. Use la semántica de adquisición al entrar en una región protegida y liberar la semántica cuando la deje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Intrínsecos del controlador](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Problemas de sincronización y multiprocesador](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
