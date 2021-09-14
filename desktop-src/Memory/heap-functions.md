---
description: Cada proceso tiene un montón predeterminado proporcionado por el sistema. Las aplicaciones que hacen asignaciones frecuentes desde el montón pueden mejorar el rendimiento mediante el uso de montones privados.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funciones de montón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159856"
---
# <a name="heap-functions"></a>Funciones de montón

Cada proceso tiene un montón predeterminado proporcionado por el sistema. Las aplicaciones que hacen asignaciones frecuentes desde el montón pueden mejorar el rendimiento mediante el uso de montones privados.

Un montón privado es un bloque de una o varias páginas en el espacio de direcciones del proceso de llamada. Después de crear el montón privado, el proceso usa funciones como [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) y [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para administrar la memoria de ese montón.

Las funciones del montón también se pueden usar para administrar la memoria en el montón predeterminado del proceso, mediante el identificador devuelto por la [**función GetProcessHeap.**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) Las nuevas aplicaciones deben usar las funciones del montón en lugar de las [funciones globales y locales](global-and-local-functions.md) para este propósito.

No hay ninguna diferencia entre la memoria asignada desde un montón privado y la asignada mediante las demás funciones de asignación de memoria. Para obtener una lista completa de las funciones, vea la tabla en [Funciones de administración de memoria](memory-management-functions.md).

> [!Note]  
> Un subproceso debe llamar a funciones de montón solo para el montón predeterminado del proceso y los montones privados que el subproceso crea y administra, mediante identificadores devueltos por la [**función GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) o [**HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate)

 

La [**función HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) crea un objeto de montón privado desde el que el proceso de llamada puede asignar bloques de memoria mediante [**la función HeapAlloc.**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) **HeapCreate** especifica un tamaño inicial y un tamaño máximo para el montón. El tamaño inicial determina el número de páginas confirmadas, de lectura y escritura asignadas inicialmente para el montón. El tamaño máximo determina el número total de páginas reservadas. Estas páginas crean un bloque contiguo en el espacio de direcciones virtuales de un proceso en el que el montón puede crecer. Las páginas adicionales se confirman automáticamente desde este espacio reservado si las solicitudes de **HeapAlloc** superan el tamaño actual de las páginas confirmadas, suponiendo que el almacenamiento físico para él esté disponible. Una vez confirmadas las páginas, no se anulan hasta que finaliza el proceso o hasta que el montón se destruye mediante una llamada a la [**función HeapDestroy.**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy)

La memoria de un objeto de montón privado solo es accesible para el proceso que lo creó. Si una biblioteca de vínculos dinámicos (DLL) crea un montón privado, lo hace en el espacio de direcciones del proceso que llamó al archivo DLL. Solo es accesible para ese proceso.

La [**función HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) asigna un número especificado de bytes de un montón privado y devuelve un puntero al bloque asignado. Este puntero se puede usar en las funciones [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)y [**HeapValidate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate)

La memoria asignada [**por HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) no se puede mover. La dirección devuelta por **HeapAlloc** es válida hasta que se libera o reasigna el bloque de memoria; no es necesario bloquear el bloque de memoria.

Dado que el sistema no puede compactar un montón privado, puede fragmentarse. Las aplicaciones que asignan grandes cantidades de [](low-fragmentation-heap.md) memoria en varios tamaños de asignación pueden usar el montón de baja fragmentación para reducir la fragmentación del montón.

Un posible uso de las funciones del montón es crear un montón privado cuando se inicia un proceso, especificando un tamaño inicial suficiente para satisfacer los requisitos de memoria del proceso. Si se produce un error en la llamada a la función [**HeapCreate,**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) el proceso puede finalizar o notificar al usuario la escasez de memoria. Sin embargo, si se realiza correctamente, el proceso está seguro de tener la memoria que necesita.

La memoria solicitada [**por HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) puede o no ser contigua. La memoria asignada dentro de un montón por [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) es contigua. No debe escribir ni leer desde la memoria en un montón excepto el asignado por **HeapAlloc**, ni debe asumir ninguna relación entre dos áreas de memoria asignadas por **HeapAlloc**.

No debe hacer referencia de ninguna manera a la memoria liberada por [**HeapFree.**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) Una vez liberada la memoria, cualquier información que pueda haber estado en ella desaparece para siempre. Si necesita información, no libre la memoria que contiene la información. Las llamadas de función que devuelven información sobre la memoria (como [**HeapSize)**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)no se pueden usar con la memoria liberada, ya que pueden devolver datos falsos.

La [**función HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) destruye un objeto de montón privado. Anula y libera todas las páginas del objeto de montón y invalida el identificador del montón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



