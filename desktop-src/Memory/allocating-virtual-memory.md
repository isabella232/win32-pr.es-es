---
description: Las funciones de memoria virtual manipulan páginas de memoria. Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Asignación de memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360673"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="8f603-104">Asignación de memoria virtual</span><span class="sxs-lookup"><span data-stu-id="8f603-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="8f603-105">Las funciones de memoria virtual manipulan páginas de memoria.</span><span class="sxs-lookup"><span data-stu-id="8f603-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="8f603-106">Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.</span><span class="sxs-lookup"><span data-stu-id="8f603-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="8f603-107">La función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) realiza una de las operaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f603-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="8f603-108">Reserva una o más páginas libres.</span><span class="sxs-lookup"><span data-stu-id="8f603-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="8f603-109">Confirma una o más páginas reservadas.</span><span class="sxs-lookup"><span data-stu-id="8f603-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="8f603-110">Reserva y confirma una o varias páginas libres.</span><span class="sxs-lookup"><span data-stu-id="8f603-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="8f603-111">Puede especificar la dirección de inicio de las páginas que se van a reservar o confirmar, o puede permitir que el sistema determine la dirección.</span><span class="sxs-lookup"><span data-stu-id="8f603-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="8f603-112">La función redondea la dirección especificada al límite de página adecuado.</span><span class="sxs-lookup"><span data-stu-id="8f603-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="8f603-113">No se puede acceder a las páginas reservadas, pero las páginas confirmadas se pueden asignar con el acceso **Page \_ ReadWrite**, **Page \_ ReadOnly** o **Page \_ NoAccess** .</span><span class="sxs-lookup"><span data-stu-id="8f603-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="8f603-114">Cuando se confirman páginas, se asignan cargos de memoria desde el tamaño total de la RAM y los archivos de paginación en el disco, pero cada página se inicializa y se carga en la memoria física solo en el primer intento de leer o escribir en esa página.</span><span class="sxs-lookup"><span data-stu-id="8f603-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="8f603-115">Puede utilizar referencias de puntero normales para tener acceso a la memoria confirmada por la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .</span><span class="sxs-lookup"><span data-stu-id="8f603-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
