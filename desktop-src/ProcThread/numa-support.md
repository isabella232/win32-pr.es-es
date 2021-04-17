---
description: El modelo tradicional de compatibilidad con varios procesadores es el multiprocesador simétrico (SMP). En este modelo, cada procesador tiene el mismo acceso a la memoria y a la e/s. A medida que se agregan más procesadores, el bus de procesador se convierte en una limitación para el rendimiento del sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Compatibilidad con NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559df7d4e13571953f2826188bd80ccbc472b2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677851"
---
# <a name="numa-support"></a>Compatibilidad con NUMA

El modelo tradicional de compatibilidad con varios procesadores es el multiprocesador simétrico (SMP). En este modelo, cada procesador tiene el mismo acceso a la memoria y a la e/s. A medida que se agregan más procesadores, el bus de procesador se convierte en una limitación para el rendimiento del sistema.

Los diseñadores del sistema usan el acceso a memoria no uniforme (NUMA) para aumentar la velocidad del procesador sin aumentar la carga en el bus del procesador. La arquitectura no es uniforme porque cada procesador está cerca de algunas partes de la memoria y más lejos de otras partes de la memoria. El procesador obtiene rápidamente el acceso a la memoria a la que está cerca, aunque puede tardar más tiempo en obtener acceso a la memoria que está más lejos.

En un sistema NUMA, las CPU están organizadas en sistemas más pequeños denominados *nodos*. Cada nodo tiene sus propios procesadores y memoria y está conectado al sistema más grande a través de un bus de interconexión coherente con la memoria caché.

El sistema intenta mejorar el rendimiento mediante la programación de subprocesos en procesadores que se encuentran en el mismo nodo que la memoria que se está usando. Intenta satisfacer las solicitudes de asignación de memoria desde dentro del nodo, pero asignará memoria de otros nodos si es necesario. También proporciona una API para que la topología del sistema esté disponible para las aplicaciones. Puede mejorar el rendimiento de las aplicaciones mediante las funciones NUMA para optimizar el uso de la memoria y la programación.

En primer lugar, tendrá que determinar el diseño de los nodos del sistema. Para recuperar el nodo con el número más alto del sistema, utilice la función [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Tenga en cuenta que no se garantiza que este número sea igual al número total de nodos del sistema. Además, no se garantiza que los nodos con números secuenciales estén próximos juntos. Para recuperar la lista de procesadores del sistema, utilice la función [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Puede determinar el nodo de cada procesador de la lista mediante la función [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . Como alternativa, para recuperar una lista de todos los procesadores de un nodo, utilice la función [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

Después de determinar qué procesadores pertenecen a qué nodos, puede optimizar el rendimiento de la aplicación. Para asegurarse de que todos los subprocesos del proceso se ejecutan en el mismo nodo, utilice la función [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) con una máscara de afinidad de proceso que especifique los procesadores en el mismo nodo. Esto aumenta la eficacia de las aplicaciones cuyos subprocesos necesitan tener acceso a la misma memoria. Como alternativa, para limitar el número de subprocesos en cada nodo, utilice la función [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Las aplicaciones que usan mucha memoria deberán optimizar el uso de memoria. Para recuperar la cantidad de memoria libre disponible para un nodo, utilice la función [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . La función [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) permite a la aplicación especificar un nodo preferido para la asignación de memoria. **VirtualAllocExNuma** no asigna ninguna página física, por lo que se realizará correctamente independientemente de si las páginas están disponibles en ese nodo o en otra parte del sistema. Las páginas físicas se asignan a petición. Si el nodo preferido se queda sin páginas, el administrador de memoria usará páginas de otros nodos. Si se pagina la memoria, se usa el mismo proceso cuando se vuelve a colocar en.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Compatibilidad con NUMA en sistemas con más de 64 procesadores lógicos

En sistemas con más de 64 procesadores lógicos, los nodos se asignan a los [grupos de procesadores](processor-groups.md) según la capacidad de los nodos. La capacidad de un nodo es el número de procesadores que están presentes cuando el sistema se inicia junto con los procesadores lógicos adicionales que se pueden agregar mientras el sistema se está ejecutando.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admiten los grupos de procesadores.

Cada nodo debe estar incluido en su totalidad dentro de un grupo. Si las capacidades de los nodos son relativamente pequeñas, el sistema asigna más de un nodo al mismo grupo, eligiendo los nodos físicamente cercanos entre sí para mejorar el rendimiento. Si la capacidad de un nodo supera el número máximo de procesadores en un grupo, el sistema divide el nodo en varios nodos más pequeños, cada uno lo suficientemente pequeño como para caber en un grupo.

Se puede solicitar un nodo NUMA ideal para un nuevo proceso mediante el atributo extendido del [**nodo de procedimiento \_ preferido del \_ atributo \_ \_ de subproceso**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) al crear el proceso. Al igual que un procesador ideal para subprocesos, el nodo ideal es una sugerencia para el programador, que asigna el nuevo proceso al grupo que contiene el nodo solicitado si es posible.

Las funciones de NUMA extendidas [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)y [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) se diferencian de sus homólogos no extendidos en que el número de nodo es un valor **USHORT** en lugar de un **UCHAR**, para dar cabida al mayor número de nodos en un sistema con más de 64 procesadores lógicos. Además, el procesador especificado con o recuperado por las funciones extendidas incluye el grupo de procesadores; el procesador especificado con o recuperado por las funciones sin extensión es relativo al grupo. Para obtener más información, vea los temas de referencia de funciones individuales.

Una aplicación compatible con grupos puede asignar todos los subprocesos a un nodo determinado de manera similar a la que se ha descrito anteriormente en este tema, mediante las funciones de NUMA extendidas correspondientes. La aplicación usa [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) para obtener la lista de todos los procesadores del sistema. Tenga en cuenta que la aplicación no puede establecer la máscara de afinidad de proceso a menos que el proceso se asigne a un único grupo y el nodo previsto se encuentre en ese grupo. Normalmente, la aplicación debe llamar a [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) para limitar los subprocesos al nodo previsto.

## <a name="numa-api"></a>API NUMA

En la tabla siguiente se describe la API NUMA.



| Función                                                                     | Descripción                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Asigna páginas de memoria física que se van a asignar y desasignar en cualquier región de [extensiones de ventana de dirección](../memory/address-windowing-extensions.md) (AWE) de un proceso especificado y especifica el nodo Numa para la memoria física. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado y especifica el nodo NUMA de la memoria física.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera información acerca de los procesadores lógicos y el hardware relacionado.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera información acerca de las relaciones de los procesadores lógicos y el hardware relacionado.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera la cantidad de memoria disponible en el nodo especificado.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera la cantidad de memoria disponible en un nodo especificado como valor **USHORT** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera el nodo que tiene actualmente el número más alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Recupera la máscara del procesador para el nodo especificado.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Recupera la máscara del procesador para un nodo especificado como valor **USHORT** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera el número de nodo del procesador especificado.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera el número de nodo como un valor **USHORT** para el procesador especificado.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera el número de nodo del identificador de proximidad especificado.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera el número de nodo como un valor **USHORT** para el identificador de proximidad especificado.                                                                                                                                         |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Asigna una vista de una asignación de archivo en el espacio de direcciones de un proceso de llamada y especifica el nodo NUMA para la memoria física.                                                                                                 |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Reserva o confirma una región de memoria en el espacio de direcciones virtuales del proceso especificado y especifica el nodo NUMA para la memoria física.                                                                          |



 

La función [**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) se puede usar para recuperar el nodo Numa en el que se asigna una página. Para obtener un ejemplo, consulte [asignación de memoria desde un nodo Numa](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de memoria desde un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Varios procesadores](multiple-processors.md)
</dt> <dt>

[Grupos de procesadores](processor-groups.md)
</dt> </dl>

 

 
