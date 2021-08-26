---
description: En el ejemplo siguiente se muestra cómo un subproceso inicializa, escribe y libera una sección crítica. Usa las funciones InitializeCriticalSectionAndSpinCount, EnterCriticalSection, LeaveCriticalSection y DeleteCriticalSection.
ms.assetid: 3c96414b-97e7-4ebb-a629-bfdb7a77c576
title: Usar objetos de sección críticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe2634987b49ebd6fb0109597fe7429ac9467e4e5178f0e65242f1c7cf402be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073065"
---
# <a name="using-critical-section-objects"></a>Usar objetos de sección críticos

En el ejemplo siguiente se muestra cómo un subproceso inicializa, escribe y libera una [sección crítica](critical-section-objects.md). Usa las [**funciones InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount), [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection), [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection)y [**DeleteCriticalSection.**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection)

``` syntax
// Global variable
CRITICAL_SECTION CriticalSection; 

int main( void )
{
    ...

    // Initialize the critical section one time only.
    if (!InitializeCriticalSectionAndSpinCount(&CriticalSection, 
        0x00000400) ) 
        return;
    ...

    // Release resources used by the critical section object.
    DeleteCriticalSection(&CriticalSection);
}

DWORD WINAPI ThreadProc( LPVOID lpParameter )
{
    ...

    // Request ownership of the critical section.
    EnterCriticalSection(&CriticalSection); 

    // Access the shared resource.

    // Release ownership of the critical section.
    LeaveCriticalSection(&CriticalSection);

    ...
return 1;
}
```

 

 
