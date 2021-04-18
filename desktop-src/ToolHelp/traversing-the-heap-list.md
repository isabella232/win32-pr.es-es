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
# <a name="traversing-the-heap-list"></a>Atravesar la lista de montones

En el ejemplo siguiente se obtiene una lista de montones para el proceso actual. Toma una instantánea de los montones mediante la función [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) y, a continuación, recorre la lista con las funciones [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) y [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Para cada montón, usa las funciones [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para recorrer los bloques del montón.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) son ineficaces, especialmente en el caso de montones grandes. Sin embargo, son útiles para consultar otros procesos en los que normalmente tendría que insertar un subproceso en el otro proceso para recopilar la información (estas API hacen esto por usted).

Vea el segundo ejemplo para obtener una alternativa equivalente, mucho más eficaz, que usa [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) en lugar de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next). Tenga en cuenta que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) solo se puede usar para el mismo proceso.

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

El siguiente fragmento de código usa la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) para recorrer los montones de proceso, lo que produce una salida idéntica al ejemplo anterior, pero es mucho más eficaz:

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

Recorrer un montón con la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) es aproximadamente lineal en el tamaño del montón, mientras que recorrer un montón con la función [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) es aproximadamente cuadrático en el tamaño del montón.
Incluso en el caso de un montón modesto con 10.000 asignaciones, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) se ejecuta 10.000 veces más rápido que [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , a la vez que proporciona información más detallada. La diferencia de rendimiento se vuelve aún más espectacular a medida que aumenta el tamaño del montón.

Para obtener un ejemplo más detallado de cómo recorrer el montón con la función [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consulte [enumeración de un montón](/windows/win32/memory/enumerating-a-heap).
