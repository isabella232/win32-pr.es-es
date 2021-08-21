---
description: Una página de protección proporciona una alarma de un solo uso para el acceso a la página de memoria.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Crear páginas de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee4d4a44a6e64d6af81e4b847347f357c3590edbd7e6b806e8f32653e1f869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963295"
---
# <a name="creating-guard-pages"></a>Crear páginas de protección

Una página de protección proporciona una alarma de un solo uso para el acceso a la página de memoria. Esto puede ser útil para una aplicación que necesita supervisar el crecimiento de grandes estructuras de datos dinámicos. Por ejemplo, hay sistemas operativos que usan páginas de protección para implementar la comprobación automática de la pila.

Para crear una página de protección, establezca el modificador **de \_ protección** de páginas PROTECCIÓN DE PÁGINA de la página. Este valor se puede especificar, junto con otros modificadores de protección de páginas, en las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)y [**VirtualProtectEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) El **modificador PAGE \_ GUARD** se puede usar con cualquier otro modificador de protección de página, excepto **PAGE \_ NOACCESS.**

Si un programa intenta acceder a una dirección dentro de una página de protección, el sistema genera una excepción **STATUS \_ GUARD PAGE \_ \_ VIOLATION** (0x80000001). El sistema también borra el modificador **PAGE \_ GUARD** y quita el estado de la página de protección de la página de memoria. El sistema no detendrá el siguiente intento de acceder a la página de memoria con una **excepción INFRACCIÓN DE PÁGINA DE PROTECCIÓN \_ \_ \_ DE** ESTADO.

Si se produce una excepción de página de protección durante un servicio del sistema, se produce un error en el servicio y normalmente devuelve algún indicador de estado de error. Dado que el sistema también quita el estado de la página de protección de la página de memoria correspondiente, la siguiente invocación del mismo servicio del sistema no producirá un error debido a una excepción DE INFRACCIÓN DE PÁGINA DE PROTECCIÓN DE ESTADO (a menos que, por supuesto, alguien vuelva a establecer la página de protección). **\_ \_ \_**

En el siguiente programa corto se muestra el comportamiento de la protección de la página.


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



Se produce un error en el primer intento de bloquear el bloque de memoria, lo que genera una **excepción STATUS \_ GUARD PAGE \_ \_ VIOLATION.** El segundo intento se realiza correctamente, porque el primer intento ha desactivado la protección de la página de protección del bloque de memoria.

 

 
