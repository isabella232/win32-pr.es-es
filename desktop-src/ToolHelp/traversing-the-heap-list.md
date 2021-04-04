---
title: Atravesar la lista de montones
description: En el ejemplo siguiente se obtiene una lista de montones para el proceso actual.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25179ab78f59c111d41849bda28184fcbfa7f612
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076031"
---
# <a name="traversing-the-heap-list"></a>Atravesar la lista de montones

En el ejemplo siguiente se obtiene una lista de montones para el proceso actual. Toma una instantánea de los montones mediante la función [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) y, a continuación, recorre la lista con las funciones [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) y [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Para cada montón, usa las funciones [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para recorrer los bloques del montón.


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



 

 




