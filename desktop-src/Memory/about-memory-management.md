---
description: Cada proceso en Microsoft Windows de 32 bits tiene su propio espacio de direcciones virtuales que permite direccionar hasta 4 gigabytes de memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Acerca de la administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686812"
---
# <a name="about-memory-management"></a><span data-ttu-id="92293-103">Acerca de la administración de memoria</span><span class="sxs-lookup"><span data-stu-id="92293-103">About Memory Management</span></span>

<span data-ttu-id="92293-104">Cada proceso en Microsoft Windows de 32 bits tiene su propio espacio de direcciones virtuales que permite direccionar hasta 4 gigabytes de memoria.</span><span class="sxs-lookup"><span data-stu-id="92293-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="92293-105">Cada proceso en Windows de 64 bits tiene un espacio de direcciones virtuales de 8 terabytes.</span><span class="sxs-lookup"><span data-stu-id="92293-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="92293-106">Todos los subprocesos de un proceso pueden tener acceso a su espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="92293-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="92293-107">Sin embargo, los subprocesos no pueden tener acceso a la memoria que pertenece a otro proceso, lo que evita que otro proceso dañe un proceso.</span><span class="sxs-lookup"><span data-stu-id="92293-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="92293-108">Para obtener información sobre el espacio de direcciones virtuales y las funciones de administración de memoria, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="92293-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="92293-109">Espacio de direcciones virtuales</span><span class="sxs-lookup"><span data-stu-id="92293-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="92293-110">Grupos de memoria</span><span class="sxs-lookup"><span data-stu-id="92293-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="92293-111">Información de rendimiento de memoria</span><span class="sxs-lookup"><span data-stu-id="92293-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="92293-112">Funciones de memoria virtual</span><span class="sxs-lookup"><span data-stu-id="92293-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="92293-113">Funciones del montón</span><span class="sxs-lookup"><span data-stu-id="92293-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="92293-114">Asignación de archivos</span><span class="sxs-lookup"><span data-stu-id="92293-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="92293-115">Compatibilidad con memoria grande</span><span class="sxs-lookup"><span data-stu-id="92293-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="92293-116">Funciones globales y locales</span><span class="sxs-lookup"><span data-stu-id="92293-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="92293-117">Funciones de la biblioteca estándar de C</span><span class="sxs-lookup"><span data-stu-id="92293-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="92293-118">Comparar métodos de asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="92293-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



