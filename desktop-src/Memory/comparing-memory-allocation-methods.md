---
Description: La siguiente es una breve comparación de los distintos métodos de asignación de memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparar métodos de asignación de memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003749"
---
# <a name="comparing-memory-allocation-methods"></a>Comparar métodos de asignación de memoria

La siguiente es una breve comparación de los distintos métodos de asignación de memoria:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **new**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Aunque las funciones [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)y [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) asignan memoria en última instancia del montón, cada una proporciona un conjunto de funcionalidad ligeramente diferente. Por ejemplo, se puede indicar a **HeapAlloc** que genere una excepción si no se pudo asignar memoria, una funcionalidad que no esté disponible con **LocalAlloc**. **LocalAlloc** admite la asignación de identificadores que permiten que la memoria subyacente se mueva mediante una reasignación sin cambiar el valor de identificador, una funcionalidad no disponible con **HeapAlloc**.

A partir de Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se implementan como funciones contenedoras que llaman a [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mediante un identificador del montón predeterminado del proceso. Por lo tanto, **GlobalAlloc** y **LocalAlloc** tienen una mayor sobrecarga que **HeapAlloc**.

Dado que los distintos asignadores de montón proporcionan una funcionalidad distintiva mediante el uso de diferentes mecanismos, debe liberar memoria con la función correcta. Por ejemplo, la memoria asignada con [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) se debe liberar con [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) y no con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) o [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). La memoria asignada con [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se debe consultar, validar y liberar con la función global o local correspondiente.

La función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) le permite especificar opciones adicionales para la asignación de memoria. Sin embargo, sus asignaciones usan una granularidad de página, por lo que el uso de **VirtualAlloc** puede dar lugar a un mayor uso de la memoria.

La función **malloc** tiene la desventaja de que depende del tiempo de ejecución. El operador **New** tiene la desventaja de que dependen del compilador y del lenguaje.

La función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tiene la ventaja de que funciona bien en C, C++ o Visual Basic. También es la única manera de compartir la memoria en una aplicación basada en COM, ya que MIDL usa **CoTaskMemAlloc** y [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para calcular las referencias de la memoria.


## <a name="examples"></a>Ejemplos

* [Reservar y confirmar memoria](./reserving-and-committing-memory.md)

* [Ejemplo de AWE](./awe-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones globales y locales](global-and-local-functions.md)
</dt> <dt>

[Funciones del montón](heap-functions.md)
</dt> <dt>

[Funciones de memoria virtual](virtual-memory-functions.md)
</dt> </dl>

 

 