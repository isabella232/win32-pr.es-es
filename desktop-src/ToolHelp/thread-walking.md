---
title: Recorrido de subprocesos
description: Una instantánea que incluye la lista de subprocesos contiene información acerca de cada subproceso de cada uno de los procesos que se están ejecutando actualmente.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerar
- enumerar, subprocesos
- subprocesos
- subprocesos, enumerar subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685759"
---
# <a name="thread-walking"></a><span data-ttu-id="8d0f3-107">Recorrido de subprocesos</span><span class="sxs-lookup"><span data-stu-id="8d0f3-107">Thread Walking</span></span>

<span data-ttu-id="8d0f3-108">Una instantánea que incluye la lista de subprocesos contiene información acerca de cada subproceso de cada uno de los procesos que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="8d0f3-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="8d0f3-109">Puede recuperar información para el primer subproceso de la lista mediante la función [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) .</span><span class="sxs-lookup"><span data-stu-id="8d0f3-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="8d0f3-110">Después de recuperar el primer subproceso de la lista, puede recuperar información de subprocesos posteriores mediante la función [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="8d0f3-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="8d0f3-111">**Thread32First** y **Thread32Next** rellenan una estructura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con información sobre los subprocesos individuales de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="8d0f3-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="8d0f3-112">Puede enumerar los subprocesos de un proceso específico tomando una instantánea que incluye los subprocesos y, a continuación, atravesar la lista de subprocesos, manteniendo la información sobre los subprocesos que tienen el mismo identificador de proceso que el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="8d0f3-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="8d0f3-113">Puede recuperar un código de estado de error extendido para [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) y [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="8d0f3-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="8d0f3-114">El contenido del miembro **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) es un identificador de subproceso y se puede usar en cualquier función que requiera un identificador de subproceso.</span><span class="sxs-lookup"><span data-stu-id="8d0f3-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8d0f3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d0f3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0f3-116">Atravesar la lista de subprocesos</span><span class="sxs-lookup"><span data-stu-id="8d0f3-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 