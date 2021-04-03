---
description: La función CreateProcess permite a un depurador iniciar un proceso y depurarlo.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funciones de proceso para depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998224"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="269db-103">Funciones de proceso para depuración</span><span class="sxs-lookup"><span data-stu-id="269db-103">Process Functions for Debugging</span></span>

<span data-ttu-id="269db-104">La función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite a un depurador iniciar un proceso y depurarlo.</span><span class="sxs-lookup"><span data-stu-id="269db-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="269db-105">El parámetro *fdwCreate* de **CreateProcess** se usa para especificar el tipo de operación de depuración.</span><span class="sxs-lookup"><span data-stu-id="269db-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="269db-106">Si \_ se especifica la marca de proceso de DEpuración para el parámetro, un depurador depura el nuevo proceso y todos los descendientes del proceso, siempre que los descendientes se creen sin la marca de proceso de DEpuración \_ .</span><span class="sxs-lookup"><span data-stu-id="269db-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="269db-107">Si el proceso de depuración \_ y la DEpuración \_ solo \_ \_ se especifican en *fdwCreate*, un depurador devuelverá el nuevo proceso pero ninguno de sus descendientes.</span><span class="sxs-lookup"><span data-stu-id="269db-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="269db-108">Un depurador puede depurar otro mediante la creación de un proceso con la marca DEBUG Process (proceso de depuración) \_ .</span><span class="sxs-lookup"><span data-stu-id="269db-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="269db-109">El nuevo proceso (el depurador que se está depurando) debe crear un proceso con la marca DEBUG Process (proceso de depuración) \_ .</span><span class="sxs-lookup"><span data-stu-id="269db-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="269db-110">La función [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permite a un depurador obtener el identificador de un proceso existente.</span><span class="sxs-lookup"><span data-stu-id="269db-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="269db-111">(La función [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa este identificador para adjuntar el depurador al proceso). Normalmente, los depuradores abren un proceso con las marcas de escritura de VM de proceso \_ \_ lectura y procesamiento de máquina virtual \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="269db-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="269db-112">El uso de estas marcas permite que el depurador Lea y escriba en la memoria virtual del proceso mediante el uso de las funciones [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) y [**writeprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="269db-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="269db-113">Para obtener más información, vea [**procesos y subprocesos**](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="269db-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 
