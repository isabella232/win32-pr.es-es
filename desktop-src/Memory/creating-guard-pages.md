---
description: Una página de protección proporciona una alarma de una captura para el acceso a la página de memoria.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Creación de páginas de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677402"
---
# <a name="creating-guard-pages"></a>Creación de páginas de protección

Una página de protección proporciona una alarma de una captura para el acceso a la página de memoria. Esto puede ser útil para una aplicación que necesita supervisar el crecimiento de grandes estructuras de datos dinámicos. Por ejemplo, hay sistemas operativos que usan páginas de protección para implementar la comprobación automática de la pila.

Para crear una página de protección, establezca el modificador de protección página de protección de **página \_** para la página. Este valor se puede especificar, junto con otros modificadores de protección de página, en las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)y [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) . El modificador de protección de **\_ Página** se puede usar con cualquier otro modificador de protección de página, excepto la **página \_ NoAccess**.

Si un programa intenta tener acceso a una dirección dentro de una página de protección, el sistema genera una excepción de **\_ \_ \_ infracción** de la página de protección de estado (0x80000001). El sistema también borra el modificador de **\_ protección de página** y quita el estado de la página de protección de la página de memoria. El sistema no detendrá el siguiente intento de acceder a la página de memoria con una excepción de **\_ \_ \_ infracción** de la página de protección de estado.

Si se produce una excepción de página de protección durante un servicio del sistema, el servicio genera un error y normalmente devuelve algún indicador de estado de error. Dado que el sistema también quita el estado de página de protección correspondiente de la página de memoria, la siguiente invocación del mismo servicio del sistema no producirá un error debido a una excepción de **\_ \_ \_ infracción** de la página de protección de estado (a menos que, por supuesto, alguien vuelva a establecer la página de protección).

El siguiente programa breve ilustra el comportamiento de la protección de la página de protección.


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



Se produce un error en el primer intento de bloquear el bloque de memoria, generando una excepción de **\_ \_ \_ infracción de página de protección de estado** . El segundo intento se realiza correctamente porque el primer intento ha desactivado la protección de la página de protección del bloque de memoria.

 

 
