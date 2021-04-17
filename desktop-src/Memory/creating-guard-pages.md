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
# <a name="creating-guard-pages"></a><span data-ttu-id="1ba3b-103">Creación de páginas de protección</span><span class="sxs-lookup"><span data-stu-id="1ba3b-103">Creating Guard Pages</span></span>

<span data-ttu-id="1ba3b-104">Una página de protección proporciona una alarma de una captura para el acceso a la página de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-104">A guard page provides a one-shot alarm for memory page access.</span></span> <span data-ttu-id="1ba3b-105">Esto puede ser útil para una aplicación que necesita supervisar el crecimiento de grandes estructuras de datos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-105">This can be useful for an application that needs to monitor the growth of large dynamic data structures.</span></span> <span data-ttu-id="1ba3b-106">Por ejemplo, hay sistemas operativos que usan páginas de protección para implementar la comprobación automática de la pila.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-106">For example, there are operating systems that use guard pages to implement automatic stack checking.</span></span>

<span data-ttu-id="1ba3b-107">Para crear una página de protección, establezca el modificador de protección página de protección de **página \_** para la página.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-107">To create a guard page, set the **PAGE\_GUARD** page protection modifier for the page.</span></span> <span data-ttu-id="1ba3b-108">Este valor se puede especificar, junto con otros modificadores de protección de página, en las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)y [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) .</span><span class="sxs-lookup"><span data-stu-id="1ba3b-108">This value can be specified, along with other page protection modifiers, in the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect), and [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) functions.</span></span> <span data-ttu-id="1ba3b-109">El modificador de protección de **\_ Página** se puede usar con cualquier otro modificador de protección de página, excepto la **página \_ NoAccess**.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-109">The **PAGE\_GUARD** modifier can be used with any other page protection modifiers, except **PAGE\_NOACCESS**.</span></span>

<span data-ttu-id="1ba3b-110">Si un programa intenta tener acceso a una dirección dentro de una página de protección, el sistema genera una excepción de **\_ \_ \_ infracción** de la página de protección de estado (0x80000001).</span><span class="sxs-lookup"><span data-stu-id="1ba3b-110">If a program attempts to access an address within a guard page, the system raises a **STATUS\_GUARD\_PAGE\_VIOLATION** (0x80000001) exception.</span></span> <span data-ttu-id="1ba3b-111">El sistema también borra el modificador de **\_ protección de página** y quita el estado de la página de protección de la página de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-111">The system also clears the **PAGE\_GUARD** modifier, removing the memory page's guard page status.</span></span> <span data-ttu-id="1ba3b-112">El sistema no detendrá el siguiente intento de acceder a la página de memoria con una excepción de **\_ \_ \_ infracción** de la página de protección de estado.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-112">The system will not stop the next attempt to access the memory page with a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span>

<span data-ttu-id="1ba3b-113">Si se produce una excepción de página de protección durante un servicio del sistema, el servicio genera un error y normalmente devuelve algún indicador de estado de error.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-113">If a guard page exception occurs during a system service, the service fails and typically returns some failure status indicator.</span></span> <span data-ttu-id="1ba3b-114">Dado que el sistema también quita el estado de página de protección correspondiente de la página de memoria, la siguiente invocación del mismo servicio del sistema no producirá un error debido a una excepción de **\_ \_ \_ infracción** de la página de protección de estado (a menos que, por supuesto, alguien vuelva a establecer la página de protección).</span><span class="sxs-lookup"><span data-stu-id="1ba3b-114">Since the system also removes the relevant memory page's guard page status, the next invocation of the same system service won't fail due to a **STATUS\_GUARD\_PAGE\_VIOLATION** exception (unless, of course, someone reestablishes the guard page).</span></span>

<span data-ttu-id="1ba3b-115">El siguiente programa breve ilustra el comportamiento de la protección de la página de protección.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-115">The following short program illustrates the behavior of guard page protection.</span></span>


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



<span data-ttu-id="1ba3b-116">Se produce un error en el primer intento de bloquear el bloque de memoria, generando una excepción de **\_ \_ \_ infracción de página de protección de estado** .</span><span class="sxs-lookup"><span data-stu-id="1ba3b-116">The first attempt to lock the memory block fails, raising a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span> <span data-ttu-id="1ba3b-117">El segundo intento se realiza correctamente porque el primer intento ha desactivado la protección de la página de protección del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ba3b-117">The second attempt succeeds, because the memory block's guard page protection has been toggled off by the first attempt.</span></span>

 

 
