---
description: En este ejemplo se muestra el uso de la función GetProcessHeaps para recuperar los identificadores del montón de proceso predeterminado y los montones privados que están activos para el proceso actual.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Obtener montones de proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caffc8dcc69b02ab671b379dbb5e133e65f8d448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001882"
---
# <a name="getting-process-heaps"></a><span data-ttu-id="e1169-103">Obtener montones de proceso</span><span class="sxs-lookup"><span data-stu-id="e1169-103">Getting Process Heaps</span></span>

<span data-ttu-id="e1169-104">En este ejemplo se muestra el uso de la función [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) para recuperar los identificadores del montón de proceso predeterminado y los montones privados que están activos para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="e1169-104">This example illustrates the use of the [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) function to retrieve handles to the default process heap and any private heaps that are active for the current process.</span></span>

<span data-ttu-id="e1169-105">En el ejemplo se llama a [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) dos veces, primero para calcular el tamaño del búfer necesario y de nuevo para recuperar los identificadores en el búfer.</span><span class="sxs-lookup"><span data-stu-id="e1169-105">The example calls [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) twice, first to calculate the size of the buffer needed and again to retrieve handles into the buffer.</span></span> <span data-ttu-id="e1169-106">El búfer se asigna desde el montón de proceso predeterminado, utilizando el identificador devuelto por [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap).</span><span class="sxs-lookup"><span data-stu-id="e1169-106">The buffer is allocated from the default process heap, using the handle returned by [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap).</span></span> <span data-ttu-id="e1169-107">En el ejemplo se imprime la dirección inicial de cada montón en la consola.</span><span class="sxs-lookup"><span data-stu-id="e1169-107">The example prints the starting address of each heap to the console.</span></span> <span data-ttu-id="e1169-108">A continuación, usa la función [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para liberar la memoria asignada para el búfer.</span><span class="sxs-lookup"><span data-stu-id="e1169-108">It then uses the [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) function to free memory allocated for the buffer.</span></span>

<span data-ttu-id="e1169-109">El número de montones de un proceso puede variar.</span><span class="sxs-lookup"><span data-stu-id="e1169-109">The number of heaps in a process may vary.</span></span> <span data-ttu-id="e1169-110">Un proceso siempre tiene al menos un montón (el montón de proceso predeterminado) y puede tener uno o más montones privados creados por la aplicación o por los archivos DLL que se cargan en el espacio de direcciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="e1169-110">A process always has at least one heap—the default process heap—and it may have one or more private heaps created by the application or by DLLs that are loaded into the address space of the process.</span></span>

<span data-ttu-id="e1169-111">Tenga en cuenta que una aplicación debe llamar a las funciones del montón solo en su montón de proceso predeterminado o en los montones privados que ha creado la aplicación; la llamada a funciones del montón en un montón privado que pertenece a otro componente puede producir un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="e1169-111">Note that an application should call heap functions only on its default process heap or on private heaps that the application has created; calling heap functions on a private heap owned by another component may cause undefined behavior.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



