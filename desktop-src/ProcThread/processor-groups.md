---
description: Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 y versiones posteriores de Windows admiten más de 64 procesadores lógicos en un único equipo. Esta funcionalidad no está disponible en las versiones de 32 bits de Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Grupos de procesadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cebc5b9ab1b386847b6561a9f6322c2fca0e2ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082648"
---
# <a name="processor-groups"></a>Grupos de procesadores

Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 y versiones posteriores de Windows admiten más de 64 procesadores lógicos en un único equipo. Esta funcionalidad no está disponible en las versiones de 32 bits de Windows.

Los sistemas con más de un procesador físico o sistemas con procesadores físicos que tienen varios núcleos proporcionan el sistema operativo con varios procesadores lógicos. Un *procesador lógico* es un motor de proceso lógico desde la perspectiva del sistema operativo, la aplicación o el controlador. Un *núcleo* es una unidad de procesador, que puede estar formada por uno o varios procesadores lógicos. Un *procesador físico* puede estar formado por uno o varios núcleos. Un procesador físico es igual que un paquete de procesador, un socket o una CPU.

La compatibilidad con sistemas que tienen más de 64 procesadores lógicos se basa en el concepto de *grupo de procesadores*, que es un conjunto estático de hasta 64 procesadores lógicos que se trata como una única entidad de programación. Los grupos de procesadores se numeran a partir de 0. Los sistemas con menos de 64 procesadores lógicos siempre tienen un solo grupo, grupo 0.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admiten los grupos de procesadores.

Cuando se inicia el sistema, el sistema operativo crea grupos de procesadores y asigna procesadores lógicos a los grupos. Si el sistema es capaz de agregar procesadores en caliente, el sistema operativo permite el espacio en grupos para los procesadores que pueden llegar mientras el sistema se está ejecutando. El sistema operativo minimiza el número de grupos de un sistema. Por ejemplo, un sistema con procesadores lógicos 128 tendría dos grupos de procesadores con procesadores 64 en cada grupo, no cuatro grupos con 32 procesadores lógicos en cada grupo.

Para mejorar el rendimiento, el sistema operativo tiene en cuenta el emplazamiento físico al asignar procesadores lógicos a grupos. Todos los procesadores lógicos de un núcleo, y todos los núcleos de un procesador físico, se asignan al mismo grupo, si es posible. Los procesadores físicos que están físicamente cercanos entre sí se asignan al mismo grupo. Un nodo NUMA se asigna a un único grupo a menos que la capacidad del nodo supere el tamaño máximo del grupo. Para obtener más información, consulte [compatibilidad con Numa](numa-support.md).

En sistemas con 64 o menos procesadores, las aplicaciones existentes funcionarán correctamente sin modificaciones. Las aplicaciones que no llamen a ninguna función que use máscaras de afinidad de procesador o números de procesador funcionarán correctamente en todos los sistemas, independientemente del número de procesadores. Para funcionar correctamente en sistemas con más de 64 procesadores lógicos, es posible que sea necesario modificar los siguientes tipos de aplicaciones:

-   Las aplicaciones que administran, mantienen o muestran información por procesador para todo el sistema deben modificarse para admitir más de 64 procesadores lógicos. Un ejemplo de este tipo de aplicación es el administrador de tareas de Windows, que muestra la carga de trabajo de cada procesador del sistema.
-   Las aplicaciones para las que el rendimiento es fundamental y que se pueden escalar eficazmente más allá de 64 procesadores lógicos se deben modificar para ejecutarse en dichos sistemas. Por ejemplo, las aplicaciones de base de datos podrían beneficiarse de las modificaciones.
-   Si una aplicación utiliza un archivo DLL que tiene estructuras de datos por procesador y el archivo DLL no se ha modificado para admitir más de 64 procesadores lógicos, todos los subprocesos de la aplicación que llaman a las funciones exportadas por el archivo DLL deben estar asignados al mismo grupo.

De forma predeterminada, una aplicación está restringida a un único grupo, que debe proporcionar una gran capacidad de procesamiento para la aplicación típica. Inicialmente, el sistema operativo asigna cada proceso a un único grupo de forma Round Robin a través de los grupos del sistema. Un proceso comienza su ejecución asignada a un grupo. El primer subproceso de un proceso se ejecuta inicialmente en el grupo al que se asigna el proceso. Cada subproceso recién creado se asigna al mismo grupo que el subproceso que lo creó.

Una aplicación que requiere el uso de varios grupos para que pueda ejecutarse en más de 64 procesadores debe determinar explícitamente dónde ejecutar sus subprocesos y es responsable de establecer las afinidades del procesador de los subprocesos en los grupos deseados. La marca [heredar \_ \_ afinidad primaria](process-creation-flags.md) se puede usar para especificar un proceso primario (que puede ser diferente del proceso actual) desde el que se va a generar la afinidad para un nuevo proceso. Si el proceso se está ejecutando en un grupo único, puede leer y modificar su afinidad mediante [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) y [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) mientras permanezca en el mismo grupo; Si se modifica la afinidad del proceso, se aplica la nueva afinidad a sus subprocesos.

La afinidad de un subproceso se puede especificar en la creación mediante el atributo de [**afinidad de grupo de \_ atributos de subprocesos \_ \_ \_**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) extendidos con la función [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) . Una vez creado el subproceso, se puede cambiar su afinidad llamando a [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) o [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Si un subproceso se asigna a un grupo diferente del proceso, se actualiza la afinidad del proceso para incluir la afinidad del subproceso y el proceso se convierte en un proceso de varios grupos. Se deben realizar más cambios de afinidad para los subprocesos individuales; no se puede modificar la afinidad de un proceso de varios grupos mediante [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). La función [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) recupera el conjunto de grupos al que se asignan un proceso y sus subprocesos.

Para especificar la afinidad para todos los procesos asociados a un objeto de trabajo, utilice la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información **JobObjectGroupInformation** o **JobObjectGroupInformationEx** .

Un procesador lógico se identifica por su número de grupo y su número de procesador relativo al grupo. Se representa mediante una estructura [**de \_ número de procesador**](/windows/desktop/api/WinNT/ns-winnt-processor_number) . Los números de procesador numéricos usados por funciones heredadas son relativos al grupo.

Para obtener una descripción de los cambios en la arquitectura del sistema operativo para admitir más de 64 procesadores, consulte las notas del producto [que admiten sistemas que tienen más de 64 procesadores](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Para obtener una lista de las nuevas funciones y estructuras que admiten grupos de procesadores, consulte [novedades en procesos y subprocesos](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Varios procesadores](multiple-processors.md)
</dt> <dt>

[Compatibilidad con NUMA](numa-support.md)
</dt> </dl>

 

 
