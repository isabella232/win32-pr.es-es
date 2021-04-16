---
description: En el ejemplo siguiente se muestra el uso de las funciones VirtualAlloc y VirtualFree para reservar y confirmar la memoria según sea necesario para una matriz dinámica.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reservar y confirmar memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688682"
---
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="aa6b1-103">Reservar y confirmar memoria</span><span class="sxs-lookup"><span data-stu-id="aa6b1-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="aa6b1-104">En el ejemplo siguiente se muestra el uso de las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) y [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) para reservar y confirmar la memoria según sea necesario para una matriz dinámica.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="aa6b1-105">En primer lugar, se llama a **VirtualAlloc** para reservar un bloque de páginas con **null** especificado como parámetro de dirección base, obligando al sistema a determinar la ubicación del bloque.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="aa6b1-106">Más adelante, se llama a **VirtualAlloc** siempre que es necesario confirmar una página de esta región reservada y se especifica la dirección base de la página siguiente que se va a confirmar.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="aa6b1-107">En el ejemplo se usa la sintaxis de control de excepciones estructurado para confirmar páginas de la región reservada.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="aa6b1-108">Siempre que se produce una excepción de error de página durante la ejecución del bloque **\_ \_ try** , se ejecuta la función de filtro en la expresión que precede al bloque **\_ \_ Except** .</span><span class="sxs-lookup"><span data-stu-id="aa6b1-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="aa6b1-109">Si la función de filtro puede asignar otra página, la ejecución continúa en el bloque **\_ \_ try** en el punto donde se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="aa6b1-110">De lo contrario, se ejecuta el controlador de excepciones en el bloque **\_ \_ Except** .</span><span class="sxs-lookup"><span data-stu-id="aa6b1-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="aa6b1-111">Para obtener más información, vea [control de excepciones estructurado](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="aa6b1-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="aa6b1-112">Como alternativa a la asignación dinámica, el proceso puede simplemente confirmar toda la región en lugar de reservarla únicamente.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="aa6b1-113">Ambos métodos dan lugar al mismo uso de memoria física porque las páginas confirmadas no consumen almacenamiento físico hasta que se accede a ellas por primera vez.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="aa6b1-114">La ventaja de la asignación dinámica es que minimiza el número total de páginas confirmadas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="aa6b1-115">En el caso de las asignaciones muy grandes, la confirmación previa de una asignación completa puede hacer que el sistema se quede sin páginas confirmables, lo que provoca errores de asignación de memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="aa6b1-116">La función [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) del bloque **\_ \_ Except** libera automáticamente las asignaciones de memoria virtual, por lo que no es necesario liberar explícitamente las páginas cuando el programa finaliza a través de esta ruta de acceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="aa6b1-117">La función [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera las páginas reservadas y confirmadas si el programa se compila con el control de excepciones deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="aa6b1-118">Esta función usa **la \_ versión de MEM** para anular la confirmación y liberar toda la región de las páginas reservadas y confirmadas.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="aa6b1-119">En el siguiente ejemplo de C++ se muestra la asignación de memoria dinámica mediante un controlador de excepciones estructurado.</span><span class="sxs-lookup"><span data-stu-id="aa6b1-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


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



 

 
