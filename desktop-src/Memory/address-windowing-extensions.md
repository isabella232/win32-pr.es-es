---
description: Extensiones de ventana de dirección (AWE) es un conjunto de extensiones que permite a una aplicación manipular rápidamente la memoria física superior a 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Extensiones de ventana de dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cb311bf9ecef2de334018ca3f9982a31f0b072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909485"
---
# <a name="address-windowing-extensions"></a>Extensiones de ventana de dirección

Extensiones de ventana de dirección (AWE) es un conjunto de extensiones que permite a una aplicación manipular rápidamente la memoria física superior a 4 GB. Ciertas aplicaciones con un uso intensivo de datos, como los sistemas de administración de bases de datos y el software científico y de ingeniería, necesitan tener acceso a memorias caché de datos muy grandes. En el caso de conjuntos de datos muy grandes, restringir la memoria caché para que quepa en el espacio de direcciones de los 2 GB de la aplicación es una restricción grave. En estas situaciones, la memoria caché es demasiado pequeña para admitir la aplicación correctamente.

AWE resuelve este problema al permitir que las aplicaciones resuelvan directamente grandes cantidades de memoria al tiempo que se siguen usando punteros de 32 bits. AWE permite que las aplicaciones tengan cachés de datos mayores de 4 GB (donde hay suficiente memoria física). AWE usa la memoria física no paginada y vistas de ventana de varias partes de esta memoria física en un espacio de direcciones virtuales de 32 bits.

AWE impone algunas restricciones sobre cómo se puede usar esta memoria, principalmente porque estas restricciones permiten una asignación, reasignación y liberación extremadamente rápidas. La administración de memoria rápida es importante para estos espacios de direcciones potencialmente enormes.

-   Los intervalos de direcciones virtuales asignados para AWE no se pueden compartir con otros procesos (y, por lo tanto, no se pueden heredar). De hecho, no se permite que dos direcciones virtuales AWE diferentes dentro del mismo proceso asignen la misma página física. Estas restricciones proporcionan una reasignación y limpieza rápidas cuando se libera memoria.
-   Las páginas físicas que se pueden asignar a una región AWE están limitadas por el número de páginas físicas presentes en la máquina, ya que esta memoria nunca se pagina; se bloquea hasta que la aplicación la libera explícitamente o se cierra. Las páginas físicas asignadas para un proceso determinado pueden asignarse a cualquier región virtual de AWE dentro del mismo proceso. Las aplicaciones que usan AWE deben tener cuidado de no tomar tanta memoria física como para la paginación excesiva de otras aplicaciones o impedir la creación de nuevos procesos o subprocesos debido a la falta de recursos. Utilice la función [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) para supervisar el uso de la memoria física.
-   Las direcciones virtuales AWE siempre son de lectura/escritura y no se pueden proteger mediante llamadas a [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (es decir, no se puede especificar ninguna memoria de solo lectura, memoria de noaccesos, páginas de protección y similares).
-   Los intervalos de direcciones AWE no se pueden usar para almacenar en búfer los datos de las llamadas de gráficos o de vídeo.
-   Un intervalo de memoria AWE no se puede dividir ni se pueden eliminar partes. En su lugar, todo el intervalo de direcciones virtuales debe eliminarse como una unidad cuando se requiere la eliminación. Esto significa que debe especificar **la \_ versión de MEM** al llamar a [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree).
-   Las aplicaciones pueden asignar varias regiones simultáneamente, siempre y cuando no se superpongan.
-   Las aplicaciones que usan AWE no se admiten en el modo de emulación. Es decir, se debe volver a compilar una aplicación x86 que use funciones AWE para ejecutarse en otro procesador, mientras que la mayoría de las aplicaciones se pueden ejecutar sin volver a compilar en un emulador en otras plataformas.

Esta solución soluciona los problemas de memoria física de una manera muy general y muy aplicable. Algunas de las ventajas de AWE son:

-   Se define un pequeño grupo de funciones nuevas para manipular la memoria AWE.
-   AWE proporciona una capacidad de reasignación muy rápida. La reasignación se realiza mediante la manipulación de las tablas de memoria virtual, no mediante el movimiento de datos en la memoria física.
-   AWE proporciona granularidad del tamaño de página adecuado para el procesador (por ejemplo, 4 KB en x86), que es más útil para las aplicaciones que las páginas de gran tamaño (por ejemplo, 2 MB o 4 MB en x86).

Una aplicación debe tener el privilegio bloquear páginas en memoria para usar AWE. Para obtener este privilegio, un administrador debe agregar **páginas de bloqueo en la memoria** a las **asignaciones de derechos de usuario** del usuario. Para obtener más información acerca de cómo hacerlo, consulte "derechos de usuario" en la ayuda del sistema operativo.

Las siguientes funciones componen la API de extensiones de ventana de dirección (AWE).



| Función                                                                          | Descripción                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) y [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserve una parte del espacio de direcciones virtuales que se va a usar para AWE mediante el uso de **memoria \_ física**.                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Asigne memoria física para su uso con AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Asigne (o invalide) direcciones virtuales AWE en cualquier conjunto de páginas físicas obtenidas con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Asigne (o invalide) direcciones virtuales AWE en cualquier conjunto de páginas físicas obtenidas con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages), pero con un control más preciso que el que proporciona [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memoria física libre que se usó para AWE.                                                                                                                                                                                                               |



 

 

 
