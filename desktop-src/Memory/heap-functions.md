---
description: Cada proceso tiene un montón predeterminado proporcionado por el sistema. Las aplicaciones que realizan asignaciones frecuentes del montón pueden mejorar el rendimiento mediante el uso de montones privados.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funciones del montón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909478"
---
# <a name="heap-functions"></a>Funciones del montón

Cada proceso tiene un montón predeterminado proporcionado por el sistema. Las aplicaciones que realizan asignaciones frecuentes del montón pueden mejorar el rendimiento mediante el uso de montones privados.

Un montón privado es un bloque de una o varias páginas en el espacio de direcciones del proceso de llamada. Después de crear el montón privado, el proceso usa funciones como [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) y [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para administrar la memoria del montón.

Las funciones del montón también se pueden usar para administrar la memoria en el montón predeterminado del proceso, utilizando el identificador devuelto por la función [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) . Las nuevas aplicaciones deben usar las funciones del montón en lugar de las [funciones globales y locales](global-and-local-functions.md) para este fin.

No hay ninguna diferencia entre la memoria asignada de un montón privado y la asignada mediante las demás funciones de asignación de memoria. Para obtener una lista completa de las funciones, consulte la tabla en [funciones de administración de memoria](memory-management-functions.md).

> [!Note]  
> Un subproceso debe llamar a las funciones del montón solo para el montón predeterminado del proceso y los montones privados que el subproceso crea y administra, utilizando los identificadores devueltos por la función [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) o [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) .

 

La función [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) crea un objeto de montón privado desde el que el proceso de llamada puede asignar bloques de memoria mediante la función [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) . **HeapCreate** especifica tanto el tamaño inicial como el tamaño máximo del montón. El tamaño inicial determina el número de páginas confirmadas, de lectura y escritura asignadas inicialmente para el montón. El tamaño máximo determina el número total de páginas reservadas. Estas páginas crean un bloque contiguo en el espacio de direcciones virtuales de un proceso en el que el montón puede crecer. Las páginas adicionales se confirman automáticamente desde este espacio reservado si las solicitudes de **HeapAlloc** superan el tamaño actual de las páginas confirmadas, siempre que el almacenamiento físico esté disponible. Una vez que se confirman las páginas, no se desasignan hasta que finaliza el proceso o hasta que el montón se destruye llamando a la función [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) .

La memoria de un objeto de montón privado solo es accesible para el proceso que lo creó. Si una biblioteca de vínculos dinámicos (DLL) crea un montón privado, lo hace en el espacio de direcciones del proceso que llamó a la DLL. Solo es accesible para ese proceso.

La función [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) asigna un número especificado de bytes de un montón privado y devuelve un puntero al bloque asignado. Este puntero se puede usar en las funciones [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)y [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) .

La memoria asignada por [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) no es movible. La dirección devuelta por **HeapAlloc** es válida hasta que el bloque de memoria se libera o se vuelve a asignar. no es necesario que el bloque de memoria esté bloqueado.

Dado que el sistema no puede compactar un montón privado, se puede fragmentar. Las aplicaciones que asignan grandes cantidades de memoria en varios tamaños de asignación pueden utilizar el [montón de baja fragmentación](low-fragmentation-heap.md) para reducir la fragmentación del montón.

Un posible uso de las funciones del montón es crear un montón privado cuando se inicia un proceso, especificando un tamaño inicial suficiente para satisfacer los requisitos de memoria del proceso. Si se produce un error en la llamada a la función [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) , el proceso puede finalizar o notificar al usuario sobre la escasez de memoria. sin embargo, si se realiza correctamente, se garantiza que el proceso tiene la memoria que necesita.

La memoria solicitada por [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) puede ser contigua o no. La memoria asignada dentro de un montón por [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) es contigua. No debe escribir ni leer de la memoria en un montón, salvo que lo asigna **HeapAlloc**, y no debe asumir ninguna relación entre dos áreas de memoria asignadas por **HeapAlloc**.

No debe hacer referencia de ningún modo a la memoria que se ha liberado por [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree). Una vez liberada la memoria, toda la información que pueda haber estado en ella desaparecerá para siempre. Si necesita información, no libere memoria que contenga la información. Las llamadas de función que devuelven información sobre la memoria (como [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) no se pueden usar con la memoria liberada, ya que pueden devolver datos ficticios.

La función [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) destruye un objeto de montón privado. Anula la confirmación y libera todas las páginas del objeto Heap, y invalida el identificador del montón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



