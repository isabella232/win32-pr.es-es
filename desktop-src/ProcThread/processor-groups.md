---
description: Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 y versiones posteriores de Windows admiten más de 64 procesadores lógicos en un solo equipo. Esta funcionalidad no está disponible en versiones de 32 bits de Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Grupos de procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5916faf3cf90bce7f8549834fe130f299f782d6b2534969c89d74df454ae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418675"
---
# <a name="processor-groups"></a>Grupos de procesadores

Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 y versiones posteriores de Windows admiten más de 64 procesadores lógicos en un solo equipo. Esta funcionalidad no está disponible en versiones de 32 bits de Windows.

Los sistemas con más de un procesador físico o sistemas con procesadores físicos que tienen varios núcleos proporcionan al sistema operativo varios procesadores lógicos. Un *procesador lógico* es un motor informático lógico desde la perspectiva del sistema operativo, la aplicación o el controlador. Un *núcleo* es una unidad de procesador, que puede constar de uno o varios procesadores lógicos. Un *procesador físico* puede constar de uno o varios núcleos. Un procesador físico es el mismo que un paquete de procesador, un socket o una CPU.

La compatibilidad con sistemas que tienen más de 64 procesadores lógicos se basa en el concepto de un grupo de procesadores *,* que es un conjunto estático de hasta 64 procesadores lógicos que se trata como una única entidad de programación. Los grupos de procesadores se numeran a partir de 0. Los sistemas con menos de 64 procesadores lógicos siempre tienen un único grupo, Grupo 0.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admiten grupos de procesadores.

Cuando se inicia el sistema, el sistema operativo crea grupos de procesadores y asigna procesadores lógicos a los grupos. Si el sistema es capaz de agregar procesadores en caliente, el sistema operativo permite espacio en grupos para los procesadores que pueden llegar mientras se ejecuta el sistema. El sistema operativo minimiza el número de grupos de un sistema. Por ejemplo, un sistema con 128 procesadores lógicos tendría dos grupos de procesadores con 64 procesadores en cada grupo, no cuatro grupos con 32 procesadores lógicos en cada grupo.

Para mejorar el rendimiento, el sistema operativo tiene en cuenta la localidad física al asignar procesadores lógicos a grupos. Todos los procesadores lógicos de un núcleo y todos los núcleos de un procesador físico se asignan al mismo grupo, si es posible. Los procesadores físicos que están físicamente cerca unos de otros se asignan al mismo grupo. Un nodo NUMA se asigna a un único grupo a menos que la capacidad del nodo supere el tamaño máximo del grupo. Para obtener más información, vea [Compatibilidad con NUMA.](numa-support.md)

En sistemas con 64 o menos procesadores, las aplicaciones existentes funcionarán correctamente sin modificaciones. Las aplicaciones que no llamen a ninguna función que use máscaras de afinidad de procesador o números de procesador funcionarán correctamente en todos los sistemas, independientemente del número de procesadores. Para funcionar correctamente en sistemas con más de 64 procesadores lógicos, los siguientes tipos de aplicaciones pueden requerir modificaciones:

-   Las aplicaciones que administran, mantienen o muestran información por procesador para todo el sistema deben modificarse para admitir más de 64 procesadores lógicos. Un ejemplo de este tipo de aplicación es Windows Administrador de tareas, que muestra la carga de trabajo de cada procesador del sistema.
-   Las aplicaciones para las que el rendimiento es crítico y que se pueden escalar de forma eficaz más allá de 64 procesadores lógicos deben modificarse para ejecutarse en dichos sistemas. Por ejemplo, las aplicaciones de base de datos pueden beneficiarse de las modificaciones.
-   Si una aplicación usa un archivo DLL que tiene estructuras de datos por procesador y el archivo DLL no se ha modificado para admitir más de 64 procesadores lógicos, todos los subprocesos de la aplicación que llaman a funciones exportadas por el archivo DLL deben asignarse al mismo grupo.

De forma predeterminada, una aplicación está restringida a un único grupo, que debe proporcionar una amplia funcionalidad de procesamiento para la aplicación típica. Inicialmente, el sistema operativo asigna cada proceso a un único grupo de una manera round robin entre los grupos del sistema. Un proceso comienza su ejecución asignada a un grupo. El primer subproceso de un proceso se ejecuta inicialmente en el grupo al que se asigna el proceso. Cada subproceso recién creado se asigna al mismo grupo que el subproceso que lo creó.

Una aplicación que requiere el uso de varios grupos para que pueda ejecutarse en más de 64 procesadores debe determinar explícitamente dónde ejecutar sus subprocesos y es responsable de establecer las afinidades de procesador de los subprocesos en los grupos deseados. La [marca INHERIT PARENT \_ \_ AFFINITY](process-creation-flags.md) se puede usar para especificar un proceso primario (que puede ser diferente del proceso actual) a partir del cual se va a generar la afinidad para un nuevo proceso. Si el proceso se ejecuta en un único grupo, puede leer y modificar su afinidad mediante [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) y [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) mientras permanece en el mismo grupo. si se modifica la afinidad de proceso, la nueva afinidad se aplica a sus subprocesos.

La afinidad de un subproceso se puede especificar durante la creación mediante el atributo extendido [**PROC THREAD ATTRIBUTE GROUP \_ \_ \_ \_ AFFINITY**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con la [**función CreateRemoteThreadEx.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) Una vez creado el subproceso, se puede cambiar su afinidad llamando a [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) o [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Si un subproceso se asigna a un grupo diferente del proceso, la afinidad del proceso se actualiza para incluir la afinidad del subproceso y el proceso se convierte en un proceso de varios grupos. Se deben realizar más cambios de afinidad para subprocesos individuales; La afinidad de un proceso de varios grupos no se puede modificar mediante [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). La [**función GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) recupera el conjunto de grupos a los que se asignan un proceso y sus subprocesos.

Para especificar la afinidad de todos los procesos asociados a un objeto de trabajo, use la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información **JobObjectGroupInformation** o **JobObjectGroupInformationEx.**

Un procesador lógico se identifica por su número de grupo y su número de procesador relativo al grupo. Esto se representa mediante una [**estructura PROCESSOR \_ NUMBER.**](/windows/desktop/api/WinNT/ns-winnt-processor_number) Los números numéricos de procesador utilizados por las funciones heredadas son relativos a grupos.

Para obtener una explicación de los cambios en la arquitectura del sistema operativo para admitir más de 64 procesadores, vea las white paper [Supporting Systems That Have More Than 64 Processors](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Para obtener una lista de nuevas funciones y estructuras que admiten grupos de procesadores, vea [Novedades de Procesos y subprocesos.](what-s-new-in-processes-and-threads.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Varios procesadores](multiple-processors.md)
</dt> <dt>

[Compatibilidad NUMA](numa-support.md)
</dt> </dl>

 

 
