---
title: Atravesar la lista de montones
description: Ejemplos que muestran cómo obtener una lista de montones para el proceso actual.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994499"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="d6d37-103">Atravesar la lista de montones</span><span class="sxs-lookup"><span data-stu-id="d6d37-103">Traversing the Heap List</span></span>

<span data-ttu-id="d6d37-104">En el ejemplo siguiente se obtiene una lista de montones para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="d6d37-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="d6d37-105">Toma una instantánea de los montones mediante la función [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) y, a continuación, recorre la lista con las funciones [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) y [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="d6d37-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="d6d37-106">Para cada montón, usa las funciones [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para recorrer los bloques del montón.</span><span class="sxs-lookup"><span data-stu-id="d6d37-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d37-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) son ineficaces, especialmente en el caso de montones grandes.</span><span class="sxs-lookup"><span data-stu-id="d6d37-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="d6d37-108">Sin embargo, son útiles para consultar otros procesos en los que normalmente tendría que insertar un subproceso en el otro proceso para recopilar la información (estas API hacen esto por usted).</span><span class="sxs-lookup"><span data-stu-id="d6d37-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="d6d37-109">Vea el segundo ejemplo para obtener una alternativa equivalente, mucho más eficaz, que usa [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) en lugar de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span><span class="sxs-lookup"><span data-stu-id="d6d37-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="d6d37-110">Tenga en cuenta que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) solo se puede usar para el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="d6d37-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

<span data-ttu-id="d6d37-111">El siguiente fragmento de código usa la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) para recorrer los montones de proceso, lo que produce una salida idéntica al ejemplo anterior, pero es mucho más eficaz:</span><span class="sxs-lookup"><span data-stu-id="d6d37-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="d6d37-112">Recorrer un montón con la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) es aproximadamente lineal en el tamaño del montón, mientras que recorrer un montón con la función [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) es aproximadamente cuadrático en el tamaño del montón.</span><span class="sxs-lookup"><span data-stu-id="d6d37-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="d6d37-113">Incluso en el caso de un montón modesto con 10.000 asignaciones, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) se ejecuta 10.000 veces más rápido que [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , a la vez que proporciona información más detallada.</span><span class="sxs-lookup"><span data-stu-id="d6d37-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="d6d37-114">La diferencia de rendimiento se vuelve aún más espectacular a medida que aumenta el tamaño del montón.</span><span class="sxs-lookup"><span data-stu-id="d6d37-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="d6d37-115">Para obtener un ejemplo más detallado de cómo recorrer el montón con la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consulte [enumeración de un montón](/windows/win32/memory/enumerating-a-heap).</span><span class="sxs-lookup"><span data-stu-id="d6d37-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
