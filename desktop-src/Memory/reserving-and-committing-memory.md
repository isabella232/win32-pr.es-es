---
description: En el ejemplo siguiente se muestra el uso de las funciones VirtualAlloc y VirtualFree para reservar y confirmar memoria según sea necesario para una matriz dinámica.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reserva y confirmación de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159815"
---
# <a name="reserving-and-committing-memory"></a>Reserva y confirmación de memoria

En el ejemplo siguiente se muestra el uso de las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) y [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) para reservar y confirmar memoria según sea necesario para una matriz dinámica. En primer lugar, se llama a **VirtualAlloc** para reservar un bloque de páginas con **NULL** especificado como parámetro de dirección base, lo que obliga al sistema a determinar la ubicación del bloque. Más adelante, se llama a **VirtualAlloc** siempre que sea necesario confirmar una página de esta región reservada y se especifica la dirección base de la página siguiente que se va a confirmar.

En el ejemplo se usa la sintaxis estructurada de control de excepciones para confirmar páginas de la región reservada. Cada vez que se produce una excepción de error de página durante **\_ \_** la ejecución del bloque **\_ \_ try,** se ejecuta la función de filtro en la expresión anterior al bloque except. Si la función de filtro puede asignar otra página, la ejecución continúa en el **\_ \_ bloque try** en el punto donde se produjo la excepción. De lo contrario, se ejecuta el controlador de excepciones en **\_ \_ el** bloque except. Para obtener más información, vea [Control estructurado de excepciones.](../debug/structured-exception-handling.md)

Como alternativa a la asignación dinámica, el proceso puede confirmar simplemente toda la región en lugar de reservarla únicamente. Ambos métodos tienen como resultado el mismo uso de memoria física porque las páginas confirmadas no consumen ningún almacenamiento físico hasta que se accede por primera vez a ellas. La ventaja de la asignación dinámica es que minimiza el número total de páginas confirmadas en el sistema. En el caso de asignaciones muy grandes, la confirmación previa de una asignación completa puede hacer que el sistema se queme de las páginas confirmables, lo que da lugar a errores de asignación de memoria virtual.

La [**función ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) del bloque **\_ \_ except** libera automáticamente las asignaciones de memoria virtual, por lo que no es necesario liberar explícitamente las páginas cuando el programa finaliza a través de esta ruta de acceso de ejecución. La [**función VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera las páginas reservadas y confirmadas si el programa se ha creado con el control de excepciones deshabilitado. Esta función usa **MEM \_ RELEASE para** desa confirmar y liberar toda la región de las páginas reservadas y confirmadas.

En el siguiente ejemplo de C++ se muestra la asignación dinámica de memoria mediante un controlador de excepciones estructurado.


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
