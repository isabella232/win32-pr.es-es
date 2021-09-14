---
Description: A continuación se muestra una breve comparación de los distintos métodos de asignación de memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparar métodos de asignación de memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159892"
---
# <a name="comparing-memory-allocation-methods"></a>Comparar métodos de asignación de memoria

A continuación se muestra una breve comparación de los distintos métodos de asignación de memoria:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **New**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Aunque las [**funciones GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)y [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) asignan en última instancia memoria del mismo montón, cada una proporciona un conjunto ligeramente diferente de funcionalidad. Por ejemplo, se puede indicar a **HeapAlloc** que cree una excepción si no se pudo asignar memoria, una funcionalidad no disponible con **LocalAlloc**. **LocalAlloc admite** la asignación de identificadores que permiten mover la memoria subyacente mediante una reasignación sin cambiar el valor del identificador, una funcionalidad que no está disponible **con HeapAlloc**.

A partir de los Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se implementan como funciones contenedoras que llaman a [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mediante un identificador para el montón predeterminado del proceso. Por lo tanto, **GlobalAlloc** y **LocalAlloc** tienen una mayor sobrecarga que **HeapAlloc.**

Dado que los distintos asignadores de montón proporcionan una funcionalidad distinta mediante mecanismos diferentes, debe liberar memoria con la función correcta. Por ejemplo, la memoria asignada con [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) debe liberarse [**con HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) y no [**con LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ni [**GlobalFree.**](/windows/desktop/api/WinBase/nf-winbase-globalfree) La memoria asignada con [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) debe consultarse, validarse y liberarse con la función global o local correspondiente.

La [**función VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) permite especificar opciones adicionales para la asignación de memoria. Sin embargo, sus asignaciones usan una granularidad de página, por lo que el uso de **VirtualAlloc** puede dar lugar a un mayor uso de memoria.

La **función malloc** tiene la desventaja de depender en tiempo de ejecución. El **nuevo operador** tiene la desventaja de ser dependiente del compilador y dependiente del lenguaje.

La [**función CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tiene la ventaja de funcionar bien en C, C++ o Visual Basic. También es la única manera de compartir memoria en una aplicación basada en COM, ya que MIDL usa **CoTaskMemAlloc** y [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para serializar la memoria.


## <a name="examples"></a>Ejemplos

* [Reserva y confirmación de memoria](./reserving-and-committing-memory.md)

* [Ejemplo de AWE](./awe-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones globales y locales](global-and-local-functions.md)
</dt> <dt>

[Funciones de montón](heap-functions.md)
</dt> <dt>

[Funciones de memoria virtual](virtual-memory-functions.md)
</dt> </dl>

 

 