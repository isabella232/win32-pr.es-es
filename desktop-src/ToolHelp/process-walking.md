---
title: Recorrido del proceso
description: Una instantánea que incluye la lista de procesos contiene información sobre cada uno de los procesos que se están ejecutando actualmente.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerar
- enumerar, procesos
- procesos
- procesos, enumeración de procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487938"
---
# <a name="process-walking"></a><span data-ttu-id="1d98b-107">Recorrido del proceso</span><span class="sxs-lookup"><span data-stu-id="1d98b-107">Process Walking</span></span>

<span data-ttu-id="1d98b-108">Una instantánea que incluye la lista de procesos contiene información sobre cada uno de los procesos que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1d98b-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="1d98b-109">Puede recuperar información para el primer proceso de la lista mediante la función [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="1d98b-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="1d98b-110">Después de recuperar el primer proceso de la lista, puede atravesar la lista de procesos para las entradas subsiguientes mediante la función [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) .</span><span class="sxs-lookup"><span data-stu-id="1d98b-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="1d98b-111">**Process32First** y **Process32Next** rellenan una estructura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) con información sobre un proceso de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="1d98b-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="1d98b-112">Para obtener un ejemplo, consulte [tomar una instantánea y ver los procesos](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="1d98b-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="1d98b-113">Puede recuperar un código de estado de error extendido para [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) y [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="1d98b-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="1d98b-114">Puede leer la memoria de un proceso específico en un búfer mediante la función [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (o la función [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).</span><span class="sxs-lookup"><span data-stu-id="1d98b-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="1d98b-115">El contenido de los miembros **th32ProcessID** y **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) son identificadores de proceso y se pueden usar con cualquier función que requiera un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="1d98b-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 