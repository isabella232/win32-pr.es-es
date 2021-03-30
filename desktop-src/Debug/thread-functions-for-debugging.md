---
description: La función CreateThread crea un nuevo subproceso para un proceso.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funciones de subproceso para depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538907"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="d9f01-103">Funciones de subproceso para depuración</span><span class="sxs-lookup"><span data-stu-id="d9f01-103">Thread Functions for Debugging</span></span>

<span data-ttu-id="d9f01-104">La función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso.</span><span class="sxs-lookup"><span data-stu-id="d9f01-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="d9f01-105">Los depuradores normalmente necesitan examinar o cambiar el contenido de los registros de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="d9f01-105">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="d9f01-106">Para ello, un depurador debe obtener un identificador para el subproceso mediante la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) y especificar el acceso adecuado al subproceso (contexto get del subproceso, \_ \_ \_ contexto del conjunto de subprocesos \_ o ambos).</span><span class="sxs-lookup"><span data-stu-id="d9f01-106">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="d9f01-107">La función [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite a un depurador obtener el identificador de un subproceso existente.</span><span class="sxs-lookup"><span data-stu-id="d9f01-107">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="d9f01-108">Un proceso con acceso adecuado a un subproceso puede examinar los registros del subproceso mediante la función [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) y establecer el contenido de los registros del subproceso mediante la función [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .</span><span class="sxs-lookup"><span data-stu-id="d9f01-108">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="d9f01-109">Un proceso también puede obtener el \_ acceso a la suspensión de SUBprocesos \_ para reanudar el acceso a un subproceso.</span><span class="sxs-lookup"><span data-stu-id="d9f01-109">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="d9f01-110">Este tipo de acceso permite a un depurador controlar la ejecución de un subproceso con las funciones [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) y [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="d9f01-110">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="d9f01-111">Para obtener más información sobre los subprocesos, vea [procesos y subprocesos](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="d9f01-111">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
