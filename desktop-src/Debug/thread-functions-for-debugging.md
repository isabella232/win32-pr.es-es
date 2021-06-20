---
description: Aprenda a usar la función CreateThread para crear un subproceso para un proceso. Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funciones de subproceso para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403988"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="c43fc-104">Funciones de subproceso para la depuración</span><span class="sxs-lookup"><span data-stu-id="c43fc-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="c43fc-105">La [**función CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso.</span><span class="sxs-lookup"><span data-stu-id="c43fc-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="c43fc-106">Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="c43fc-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="c43fc-107">Para ello, un depurador debe obtener un identificador para el subproceso mediante la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) y especificar el acceso adecuado al subproceso (THREAD GET CONTEXT, THREAD SET CONTEXT o \_ \_ \_ \_ ambos).</span><span class="sxs-lookup"><span data-stu-id="c43fc-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="c43fc-108">La [**función OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite a un depurador obtener el identificador de un subproceso existente.</span><span class="sxs-lookup"><span data-stu-id="c43fc-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="c43fc-109">Un proceso con acceso adecuado a un subproceso puede examinar los registros del subproceso mediante la función [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) y establecer el contenido de los registros del subproceso mediante la [**función SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)</span><span class="sxs-lookup"><span data-stu-id="c43fc-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="c43fc-110">Un proceso también puede obtener acceso \_ THREAD SUSPEND RESUME a un \_ subproceso.</span><span class="sxs-lookup"><span data-stu-id="c43fc-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="c43fc-111">Este tipo de acceso permite a un depurador controlar la ejecución de un subproceso con las [**funciones SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**y ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)</span><span class="sxs-lookup"><span data-stu-id="c43fc-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="c43fc-112">Para obtener más información sobre los subprocesos, [vea Procesos y subprocesos.](../procthread/processes-and-threads.md)</span><span class="sxs-lookup"><span data-stu-id="c43fc-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
