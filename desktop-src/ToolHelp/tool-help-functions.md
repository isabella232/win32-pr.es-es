---
title: Funciones de ayuda de herramientas
description: Muestra las funciones de la biblioteca de ayuda de la herramienta.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076227"
---
# <a name="tool-help-functions"></a><span data-ttu-id="749d4-103">Funciones de ayuda de herramientas</span><span class="sxs-lookup"><span data-stu-id="749d4-103">Tool Help Functions</span></span>

<span data-ttu-id="749d4-104">Las siguientes funciones forman parte de la biblioteca de ayuda de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="749d4-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="749d4-105">Función</span><span class="sxs-lookup"><span data-stu-id="749d4-105">Function</span></span>                                                           | <span data-ttu-id="749d4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="749d4-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="749d4-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="749d4-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="749d4-108">Toma una instantánea de los procesos especificados, así como los montones, módulos y subprocesos utilizados por estos procesos.</span><span class="sxs-lookup"><span data-stu-id="749d4-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="749d4-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="749d4-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="749d4-110">Recupera información sobre el primer bloque de un montón asignado por un proceso.</span><span class="sxs-lookup"><span data-stu-id="749d4-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="749d4-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="749d4-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="749d4-112">Recupera información sobre el primer montón asignado por un proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="749d4-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="749d4-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="749d4-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="749d4-114">Recupera información sobre el siguiente montón asignado por un proceso.</span><span class="sxs-lookup"><span data-stu-id="749d4-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="749d4-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="749d4-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="749d4-116">Recupera información sobre el siguiente bloque de un montón asignado por un proceso.</span><span class="sxs-lookup"><span data-stu-id="749d4-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="749d4-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="749d4-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="749d4-118">Recupera información sobre el primer módulo asociado a un proceso.</span><span class="sxs-lookup"><span data-stu-id="749d4-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="749d4-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="749d4-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="749d4-120">Recupera información sobre el siguiente módulo asociado a un proceso o subproceso.</span><span class="sxs-lookup"><span data-stu-id="749d4-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="749d4-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="749d4-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="749d4-122">Recupera información sobre el primer proceso encontrado en una instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="749d4-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="749d4-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="749d4-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="749d4-124">Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="749d4-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="749d4-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="749d4-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="749d4-126">Recupera información sobre el primer subproceso de cualquier proceso que se encuentre en una instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="749d4-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="749d4-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="749d4-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="749d4-128">Recupera información sobre el siguiente subproceso de cualquier proceso que se encuentre en la instantánea de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="749d4-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="749d4-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="749d4-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="749d4-130">Copia la memoria asignada a otro proceso en un búfer proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="749d4-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




