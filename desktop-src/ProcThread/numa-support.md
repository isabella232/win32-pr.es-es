---
description: El modelo tradicional para la compatibilidad con varios procesadores es multiprocesador simétrico (SMP). En este modelo, cada procesador tiene el mismo acceso a la memoria y la E/S. A medida que se agregan más procesadores, el bus de procesador se convierte en una limitación para el rendimiento del sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Compatibilidad NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b64f6f18779fb66a87fc3c45b682fcb97248c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479431"
---
# <a name="numa-support"></a>Compatibilidad NUMA

El modelo tradicional para la compatibilidad con varios procesadores es multiprocesador simétrico (SMP). En este modelo, cada procesador tiene el mismo acceso a la memoria y la E/S. A medida que se agregan más procesadores, el bus de procesador se convierte en una limitación para el rendimiento del sistema.

Los diseñadores del sistema usan el acceso a memoria no uniforme (NUMA) para aumentar la velocidad del procesador sin aumentar la carga en el bus del procesador. La arquitectura no es uniforme porque cada procesador está cerca de algunas partes de la memoria y más lejos de otras partes de la memoria. El procesador obtiene rápidamente acceso a la memoria a la que está cerca, mientras que puede tardar más tiempo en obtener acceso a la memoria que está más lejos.

En un sistema NUMA, las CPU se organizan en sistemas más pequeños *denominados nodos*. Cada nodo tiene sus propios procesadores y memoria, y está conectado al sistema más grande a través de un bus de interconexión coherente con la memoria caché.

El sistema intenta mejorar el rendimiento programando subprocesos en procesadores que se encuentran en el mismo nodo que la memoria que se usa. Intenta satisfacer las solicitudes de asignación de memoria desde dentro del nodo, pero asignará memoria de otros nodos si es necesario. También proporciona una API para que la topología del sistema esté disponible para las aplicaciones. Puede mejorar el rendimiento de las aplicaciones mediante las funciones NUMA para optimizar la programación y el uso de memoria.

En primer lugar, deberá determinar el diseño de los nodos del sistema. Para recuperar el nodo numerado más alto del sistema, use la [**función GetNumaHighestNodeNumber.**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) Tenga en cuenta que no se garantiza que este número sea igual al número total de nodos del sistema. Además, no se garantiza que los nodos con números secuenciales se cierren juntos. Para recuperar la lista de procesadores del sistema, use la [**función GetProcessAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) Puede determinar el nodo de cada procesador de la lista mediante la [**función GetNumaProcessorNode.**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) Como alternativa, para recuperar una lista de todos los procesadores de un nodo, use la [**función GetNumaNodeProcessorMask.**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)

Después de determinar qué procesadores pertenecen a qué nodos, puede optimizar el rendimiento de la aplicación. Para asegurarse de que todos los subprocesos del proceso se ejecutan en el mismo nodo, use la función [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) con una máscara de afinidad de proceso que especifique procesadores en el mismo nodo. Esto aumenta la eficacia de las aplicaciones cuyos subprocesos necesitan acceder a la misma memoria. Como alternativa, para limitar el número de subprocesos en cada nodo, use la [**función SetThreadAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)

Las aplicaciones que consumen mucha memoria tendrán que optimizar su uso de memoria. Para recuperar la cantidad de memoria disponible para un nodo, use la [**función GetNumaAvailableMemoryNode.**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) La [**función VirtualAllocExNuma permite**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) a la aplicación especificar un nodo preferido para la asignación de memoria. **VirtualAllocExNuma** no asigna ninguna página física, por lo que se realizará correctamente tanto si las páginas están disponibles en ese nodo como en otra parte del sistema. Las páginas físicas se asignan a petición. Si el nodo preferido se queda sin páginas, el administrador de memoria usará páginas de otros nodos. Si se pagina la memoria, se usa el mismo proceso cuando se vuelve a traer.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Compatibilidad con NUMA en sistemas con más de 64 procesadores lógicos

En sistemas con más de 64 procesadores lógicos, los nodos se asignan a grupos de procesadores [según](processor-groups.md) la capacidad de los nodos. La capacidad de un nodo es el número de procesadores que están presentes cuando el sistema se inicia junto con cualquier procesador lógico adicional que se pueda agregar mientras se ejecuta el sistema.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admiten grupos de procesadores.

Cada nodo debe estar totalmente contenido dentro de un grupo. Si las capacidades de los nodos son relativamente pequeñas, el sistema asigna más de un nodo al mismo grupo, eligiendo nodos físicamente cercanos entre sí para mejorar el rendimiento. Si la capacidad de un nodo supera el número máximo de procesadores de un grupo, el sistema divide el nodo en varios nodos más pequeños, cada uno lo suficientemente pequeño como para caber en un grupo.

Se puede solicitar un nodo NUMA ideal para un nuevo proceso mediante el atributo [**extendido PROC THREAD ATTRIBUTE PREFERRED \_ \_ \_ \_ NODE**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) cuando se crea el proceso. Al igual que un procesador ideal para subprocesos, el nodo ideal es una sugerencia para el programador, que asigna el nuevo proceso al grupo que contiene el nodo solicitado si es posible.

Las funciones NUMA extendidas [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx,**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex) [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)y [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) difieren de sus homólogos no extendidos en que el número de nodo es un valor **USHORT** en lugar de **un UCHAR**, para dar cabida al número potencialmente mayor de nodos en un sistema con más de 64 procesadores lógicos. Además, el procesador especificado con o recuperado por las funciones extendidas incluye el grupo de procesadores; el procesador especificado con o recuperado por las funciones no existentes es relativo al grupo. Para más información, consulte los temas de referencia de funciones individuales.

Una aplicación que tenga en cuenta el grupo puede asignar todos sus subprocesos a un nodo determinado de forma similar a la descrita anteriormente en este tema, mediante las funciones NUMA extendidas correspondientes. La aplicación usa [**GetLogicalProcessorInformationEx para**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) obtener la lista de todos los procesadores del sistema. Tenga en cuenta que la aplicación no puede establecer la máscara de afinidad de proceso a menos que el proceso esté asignado a un único grupo y el nodo previsto se encuentra en ese grupo. Normalmente, la aplicación debe llamar [**a SetThreadGroupAffinity para**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) limitar sus subprocesos al nodo previsto.


### <a name="behavior-starting-with-windows-10-build-20348"></a>Comportamiento a partir de Windows 10 Compilación 20348 

> [!NOTE]
> A partir Windows 10 compilación 20348, el comportamiento de esta y otras funciones NUMA se ha modificado para admitir mejor los sistemas con nodos que contienen más de 64 procesadores.

La creación de nodos "falsos" para dar cabida a una asignación 1:1 entre grupos y nodos ha dado lugar a comportamientos confusos en los que se notifican números inesperados de nodos NUMA, por lo que, a partir de la compilación 20348 de Windows 10, el sistema operativo ha cambiado para permitir que varios grupos se asocien a un nodo, por lo que ahora se puede informar de la verdadera topología NUMA del sistema.  

Como parte de estos cambios en el sistema operativo, varias API NUMA han cambiado para admitir la informes de varios grupos que ahora se pueden asociar a un único nodo NUMA. Las API actualizadas y nuevas se etiquetan en la tabla de la sección **API de NUMA** siguiente.

Dado que la eliminación de la división de nodos puede afectar potencialmente a las aplicaciones existentes, hay un valor del Registro disponible para permitir volver a participar en el comportamiento de división de nodos heredado. La división de nodos se puede volver **a** habilitar creando un valor REG_DWORD denominado "SplitLargeNodes" con el valor 1 debajo HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. Los cambios en esta configuración requieren que se realice un reinicio.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNodes /t REG_DWORD /d 1
```

> [!NOTE]
> Las aplicaciones que se actualizan para usar la nueva funcionalidad de API que informa de la topología NUMA verdadera seguirán funcionando correctamente en sistemas donde se ha habilitado la división de nodos grandes con esta clave del Registro.

En el ejemplo siguiente se muestran primero posibles problemas con las tablas de compilaciones que asigna procesadores a nodos NUMA mediante las API de afinidad heredadas, que ya no proporcionan una cobertura completa de todos los procesadores del sistema, lo que puede dar lugar a una tabla incompleta. Las implicaciones de esta falta de integridad dependen del contenido de la tabla. Si la tabla simplemente almacena el número de nodo correspondiente, es probable que esto sea solo un problema de rendimiento con procesadores descubiertos que se quedan como parte del nodo 0. Sin embargo, si la tabla contiene punteros a una estructura de contexto por nodo, esto puede dar lugar a desreferencias NULL en tiempo de ejecución.

A continuación, en el ejemplo de código se muestran dos soluciones alternativas para el problema. La primera es migrar a las API de afinidad de nodo de varios grupos (modo de usuario y modo kernel). La segunda es usar **KeQueryLogicalProcessorRelationship para** consultar directamente el nodo NUMA asociado a un número de procesador determinado.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>NUMA API

En la tabla siguiente se describe la API NUMA.



| Función                                                                     | Descripción                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Asigna páginas de memoria física que se asignarán y desasignarán dentro de cualquier región de extensiones de ventana de direcciones [](../memory/address-windowing-extensions.md) (AWE) de un proceso especificado y especifica el nodo NUMA para la memoria física. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado y especifica el nodo NUMA para la memoria física.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Se actualizó Windows 10 compilación 20348. Recupera información sobre procesadores lógicos y hardware relacionado.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Se actualizó Windows 10 compilación 20348. Recupera información sobre las relaciones de los procesadores lógicos y el hardware relacionado.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera la cantidad de memoria disponible en el nodo especificado.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera la cantidad de memoria disponible en un nodo especificado como un **valor USHORT.**                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera el nodo que tiene actualmente el número más alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Se actualizó Windows 10 compilación 20348. Recupera la máscara del procesador para el nodo especificado.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | Novedad de Windows 10 Compilación 20348. Recupera la máscara de procesador de varios grupos del nodo especificado.                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Se actualizó Windows 10 compilación 20348. Recupera la máscara de procesador para un nodo especificado como **un valor USHORT.**                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera el número de nodo para el procesador especificado.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera el número de nodo como un **valor USHORT** para el procesador especificado.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera el número de nodo para el identificador de proximidad especificado.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera el número de nodo como un **valor USHORT** para el identificador de proximidad especificado.                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | Novedad de Windows 10 compilación 20348. Recupera la lista de conjuntos de CPU del conjunto predeterminado de procesos establecido por SetProcessDefaultCpuSetMasks o SetProcessDefaultCpuSets.                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | Novedad de Windows 10 compilación 20348. Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se establece una.                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada y especifica el nodo NUMA para la memoria física.                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | Novedad de Windows 10 compilación 20348. Establece la asignación predeterminada de conjuntos de CPU para subprocesos en el proceso especificado.                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | Novedad de Windows 10 compilación 20348. Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se establece una.                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Reserva o confirma una región de memoria dentro del espacio de direcciones virtuales del proceso especificado y especifica el nodo NUMA para la memoria física.                                                                          |



 

La [**función QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) se puede usar para recuperar el nodo NUMA en el que se asigna una página. Para obtener un ejemplo, vea [Asignación de memoria desde un nodo NUMA.](../memory/allocating-memory-from-a-numa-node.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de memoria desde un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Varios procesadores](multiple-processors.md)
</dt> <dt>

[Grupos de procesadores](processor-groups.md)
</dt> </dl>

 

 
