---
description: Extensiones de ventana de direcciones (AWE) es un conjunto de extensiones que permite a una aplicación manipular rápidamente la memoria física superior a 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Extensiones de ventana de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764415"
---
# <a name="address-windowing-extensions"></a>Extensiones de ventana de direcciones

Extensiones de ventana de direcciones (AWE) es un conjunto de extensiones que permite a una aplicación manipular rápidamente la memoria física superior a 4 GB. Ciertas aplicaciones que consumen muchos datos, como los sistemas de administración de bases de datos y el software científico e de ingeniería, necesitan acceso a cachés de datos muy grandes. En el caso de conjuntos de datos muy grandes, restringir la memoria caché para que quepa dentro de los 2 GB de espacio de direcciones de usuario de una aplicación es una restricción grave. En estas situaciones, la memoria caché es demasiado pequeña para admitir correctamente la aplicación.

AWE resuelve este problema permitiendo a las aplicaciones abordar directamente grandes cantidades de memoria mientras siguen utilizando punteros de 32 bits. AWE permite a las aplicaciones tener cachés de datos de más de 4 GB (donde hay suficiente memoria física). AWE usa la memoria física sin página y las vistas de ventana de varias partes de esta memoria física dentro de un espacio de direcciones virtuales de 32 bits.

AWE coloca algunas restricciones sobre cómo se puede usar esta memoria, principalmente porque estas restricciones permiten una asignación, una nueva asignación y una liberar extremadamente rápidas. La administración rápida de memoria es importante para estos espacios de direcciones potencialmente enormes.

-   Los intervalos de direcciones virtuales asignados para AWE no se pueden compartir con otros procesos (y, por tanto, no se pueden heredar). De hecho, dos direcciones virtuales de AWE diferentes dentro del mismo proceso no pueden asignar la misma página física. Estas restricciones proporcionan un remapping y una limpieza rápidos cuando se libera memoria.
-   Las páginas físicas que se pueden asignar para una región de AWE están limitadas por el número de páginas físicas presentes en la máquina, ya que esta memoria nunca se pagina: se bloquea hasta que la aplicación la libera o sale explícitamente. Las páginas físicas asignadas para un proceso determinado se pueden asignar a cualquier región virtual de AWE dentro del mismo proceso. Las aplicaciones que usan AWE deben tener cuidado de no tomar tanta memoria física que hacen que otras aplicaciones paginan excesivamente o impidan la creación de nuevos procesos o subprocesos debido a la falta de recursos. Use la [**función GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) para supervisar el uso de memoria física.
-   Las direcciones virtuales de AWE siempre son de lectura y escritura y no se pueden proteger mediante llamadas a [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (es decir, no se puede especificar ninguna memoria de solo lectura, memoria de noaccess, páginas de protección, y otros).
-   Los intervalos de direcciones AWE no se pueden usar para almacenar en búfer los datos de gráficos o llamadas de vídeo.
-   Un intervalo de memoria de AWE no se puede dividir ni se pueden eliminar partes de él. En su lugar, todo el intervalo de direcciones virtuales debe eliminarse como una unidad cuando se requiere la eliminación. Esto significa que debe especificar **MEM \_ RELEASE al** llamar a [**VirtualFree.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)
-   Las aplicaciones pueden asignar varias regiones simultáneamente, siempre que no se superpongan.
-   Las aplicaciones que usan AWE no se admiten en el modo de emulación. Es decir, una aplicación x86 que usa funciones AWE debe volver a compilarse para ejecutarse en otro procesador, mientras que la mayoría de las aplicaciones se pueden ejecutar sin volver a compilar en un emulador en otras plataformas.

Esta solución soluciona los problemas de memoria física de una manera muy general y ampliamente aplicable. Algunas de las ventajas de AWE son:

-   Se define un pequeño grupo de nuevas funciones para manipular la memoria de AWE.
-   AWE proporciona una funcionalidad de remapping muy rápida. La remapping se realiza mediante la manipulación de tablas de memoria virtual, no mediante el movimiento de datos en la memoria física.
-   AWE proporciona granularidad de tamaño de página adecuada para el procesador (por ejemplo, 4 KB en x86), que es más útil para las aplicaciones que las páginas grandes (por ejemplo, 2 MB o 4 MB en x86).

Una aplicación debe tener el privilegio Bloquear páginas en memoria para usar AWE. Para obtener este privilegio, un administrador debe agregar **Páginas de bloqueo** en memoria a asignaciones de derechos de usuario del **usuario.** Para obtener más información sobre cómo hacerlo, vea "Derechos de usuario" en la ayuda del sistema operativo.

Las siguientes funciones son la API de extensiones de ventana de direcciones (AWE).



| Función                                                                          | Descripción                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) y [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserve una parte del espacio de direcciones virtuales que se usará para AWE, mediante **MEM \_ PHYSICAL.**                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Asigne memoria física para su uso con AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Asigne (o invalide) direcciones virtuales de AWE a cualquier conjunto de páginas físicas obtenidas [**con AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Asigne (o invalide) direcciones virtuales de AWE a cualquier conjunto de páginas físicas obtenidas con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages), pero con un control más preciso que el proporcionado por [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memoria física libre que se usó para AWE.                                                                                                                                                                                                               |



 

 

 
