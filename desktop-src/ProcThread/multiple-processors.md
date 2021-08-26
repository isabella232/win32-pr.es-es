---
description: 'Los equipos con varios procesadores están diseñados normalmente para una de estas dos arquitecturas: acceso a memoria no uniforme (NUMA) o multiprocesamiento simétrico (SMP).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Varios procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28b381faaceb5a171ddcf33c0705fee144f98952c4d473c0db8c7d99050deb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032415"
---
# <a name="multiple-processors"></a>Varios procesadores

Los equipos con varios procesadores están diseñados normalmente para una de estas dos arquitecturas: acceso a memoria no uniforme (NUMA) o multiprocesamiento simétrico (SMP).

En un equipo NUMA, cada procesador está más cerca de algunas partes de la memoria que otras, lo que hace que el acceso a la memoria sea más rápido para algunas partes de la memoria que para otras. En el modelo NUMA, el sistema intenta programar subprocesos en procesadores que están cerca de la memoria que se usa. Para obtener más información sobre NUMA, vea [Compatibilidad con NUMA.](numa-support.md)

En un equipo SMP, dos o más procesadores o núcleos idénticos se conectan a una única memoria principal compartida. En el modelo SMP, cualquier subproceso se puede asignar a cualquier procesador. Por lo tanto, la programación de subprocesos en un equipo SMP es similar a la programación de subprocesos en un equipo con un solo procesador. Sin embargo, el programador tiene un grupo de procesadores, por lo que puede programar subprocesos para que se ejecuten simultáneamente. La programación sigue determinada por la prioridad del subproceso, pero se puede ver afectada por la configuración de la afinidad de subprocesos y el procesador ideal para subprocesos, como se describe en este tema.

## <a name="thread-affinity"></a>Afinidad de subprocesos

*La afinidad de* subproceso fuerza a un subproceso a ejecutarse en un subconjunto específico de procesadores. Por lo general, se debe evitar establecer la afinidad de subprocesos, ya que puede interferir con la capacidad del programador de programar subprocesos de forma eficaz entre procesadores. Esto puede reducir las mejoras de rendimiento producidas por el procesamiento paralelo. Un uso adecuado de la afinidad de subprocesos es probar cada procesador.

El sistema representa la afinidad con una máscara de bits denominada máscara de afinidad de procesador. La máscara de afinidad es el tamaño del número máximo de procesadores del sistema, con bits establecidos para identificar un subconjunto de procesadores. Inicialmente, el sistema determina el subconjunto de procesadores de la máscara.

Puede obtener la afinidad de subproceso actual para todos los subprocesos del proceso llamando a la [**función GetProcessAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) Use la [**función SetProcessAffinityMask para**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) especificar la afinidad de subprocesos para todos los subprocesos del proceso. Para establecer la afinidad de subproceso para un único subproceso, use la [**función SetThreadAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) La afinidad de subproceso debe ser un subconjunto de la afinidad de proceso.

En sistemas con más de 64 procesadores, la máscara de afinidad representa inicialmente procesadores en un único grupo de procesadores. Sin embargo, la afinidad de subprocesos se puede establecer en un procesador de un grupo diferente, lo que modifica la máscara de afinidad para el proceso. Para obtener más información, vea [Grupos de procesadores](processor-groups.md).

## <a name="thread-ideal-processor"></a>Procesador ideal para subprocesos

Cuando se especifica un *procesador ideal para subprocesos,* el programador ejecuta el subproceso en el procesador especificado siempre que sea posible. Use la [**función SetThreadIdealProcessor para**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) especificar un procesador preferido para un subproceso. Esto no garantiza que se elija el procesador ideal, pero proporciona una sugerencia útil al programador. En sistemas con más de 64 procesadores, puede usar la función [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) para especificar un procesador preferido en un grupo de procesadores específico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad NUMA](numa-support.md)
</dt> <dt>

[Grupos de procesadores](processor-groups.md)
</dt> </dl>

 

 
