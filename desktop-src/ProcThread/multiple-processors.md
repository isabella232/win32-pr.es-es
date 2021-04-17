---
description: 'Los equipos con varios procesadores suelen estar diseñados para una de estas dos arquitecturas: acceso a memoria no uniforme (NUMA) o multiproceso simétrico (SMP).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Varios procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677857"
---
# <a name="multiple-processors"></a>Varios procesadores

Los equipos con varios procesadores suelen estar diseñados para una de estas dos arquitecturas: acceso a memoria no uniforme (NUMA) o multiproceso simétrico (SMP).

En un equipo NUMA, cada procesador está más cerca de algunas partes de la memoria que otros, lo que facilita el acceso a la memoria para algunas partes de la memoria que otras partes. En el modelo NUMA, el sistema intenta programar subprocesos en procesadores que están cerca de la memoria que se está usando. Para obtener más información sobre NUMA, consulte [compatibilidad con Numa](numa-support.md).

En un equipo SMP, dos o más procesadores o núcleos idénticos se conectan a una sola memoria principal compartida. En el modelo SMP, cualquier subproceso se puede asignar a cualquier procesador. Por lo tanto, la programación de subprocesos en un equipo SMP es similar a la programación de subprocesos en un equipo con un solo procesador. Sin embargo, Scheduler tiene un grupo de procesadores, por lo que puede programar subprocesos para que se ejecuten simultáneamente. La programación sigue siendo determinada por la prioridad de los subprocesos, pero se puede influir en la configuración de la afinidad de subprocesos y el procesador ideal de subprocesos, como se describe en este tema.

## <a name="thread-affinity"></a>Afinidad de subprocesos

La *afinidad de subprocesos* obliga a que un subproceso se ejecute en un subconjunto específico de procesadores. Por lo general, se debe evitar establecer la afinidad de subprocesos, ya que puede interferir con la capacidad del programador de programar subprocesos de forma eficaz entre los procesadores. Esto puede reducir las mejoras de rendimiento generadas por el procesamiento en paralelo. Un uso adecuado de la afinidad de subprocesos es probar cada procesador.

El sistema representa la afinidad con una máscara de subred denominada máscara de afinidad de procesador. Affinity mask es el tamaño del número máximo de procesadores del sistema, con bits establecido para identificar un subconjunto de procesadores. Inicialmente, el sistema determina el subconjunto de procesadores de la máscara.

Puede obtener la afinidad del subproceso actual para todos los subprocesos del proceso mediante una llamada a la función [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Utilice la función [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) para especificar la afinidad de subprocesos para todos los subprocesos del proceso. Para establecer la afinidad de subprocesos para un único subproceso, utilice la función [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) . La afinidad de subprocesos debe ser un subconjunto de la afinidad de proceso.

En sistemas con más de 64 procesadores, la máscara de afinidad representa inicialmente los procesadores de un solo grupo de procesadores. Sin embargo, la afinidad de subprocesos se puede establecer en un procesador de un grupo diferente, lo que altera la máscara de afinidad para el proceso. Para obtener más información, consulte [grupos de procesadores](processor-groups.md).

## <a name="thread-ideal-processor"></a>Procesador ideal para subprocesos

Cuando se especifica un *procesador ideal para un subproceso*, el programador ejecuta el subproceso en el procesador especificado siempre que sea posible. Utilice la función [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) para especificar un procesador preferido para un subproceso. Esto no garantiza que se elija el procesador ideal, sino que proporciona una sugerencia útil al programador. En sistemas con más de 64 procesadores, puede usar la función [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) para especificar un procesador preferido en un grupo de procesadores específico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con NUMA](numa-support.md)
</dt> <dt>

[Grupos de procesadores](processor-groups.md)
</dt> </dl>

 

 
