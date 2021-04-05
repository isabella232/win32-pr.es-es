---
title: Espacio de direcciones virtuales (Guía de programación para Windows de 64 bits)
description: De forma predeterminada, las aplicaciones basadas en Microsoft Windows de 64 bits tienen un espacio de direcciones de modo de usuario de varios terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, espacio de direcciones virtuales
- espacio de direcciones virtuales 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078674"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="b43e8-105">Espacio de direcciones virtuales (Guía de programación para Windows de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="b43e8-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="b43e8-106">De forma predeterminada, las aplicaciones basadas en Microsoft Windows de 64 bits tienen un espacio de direcciones de modo de usuario de varios terabytes.</span><span class="sxs-lookup"><span data-stu-id="b43e8-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="b43e8-107">Para obtener valores precisos, consulte [límites de memoria para las versiones de Windows y Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="b43e8-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="b43e8-108">Sin embargo, las aplicaciones pueden especificar que el sistema debe asignar toda la memoria para la aplicación por debajo de 2 gigabytes.</span><span class="sxs-lookup"><span data-stu-id="b43e8-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="b43e8-109">Esta característica es útil para las aplicaciones de 64 bits si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b43e8-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="b43e8-110">Un espacio de direcciones de 2 GB es suficiente.</span><span class="sxs-lookup"><span data-stu-id="b43e8-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="b43e8-111">El código tiene muchas advertencias de truncamiento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b43e8-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="b43e8-112">Los punteros y los enteros se mezclan libremente.</span><span class="sxs-lookup"><span data-stu-id="b43e8-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="b43e8-113">El código tiene el polimorfismo usando tipos de datos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b43e8-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="b43e8-114">Todos los punteros siguen siendo punteros de 64 bits, pero el sistema garantiza que cada asignación de memoria se produce por debajo del límite de 2 GB, de modo que si la aplicación trunca un puntero, no se pierden datos significativos.</span><span class="sxs-lookup"><span data-stu-id="b43e8-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="b43e8-115">Los punteros se pueden truncar en valores de 32 bits y, a continuación, extenderse a valores de 64 bits mediante la extensión de signo o la extensión de cero.</span><span class="sxs-lookup"><span data-stu-id="b43e8-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="b43e8-116">Para especificar esta limitación de memoria, use la opción **/LARGEADDRESSAWARE: sin** enlazador.</span><span class="sxs-lookup"><span data-stu-id="b43e8-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="b43e8-117">Tenga en cuenta que **/LARGEADDRESSAWARE: no** se omite para un binario ARM64.</span><span class="sxs-lookup"><span data-stu-id="b43e8-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="b43e8-118">Sin embargo, tenga en cuenta que pueden producirse problemas al usar esta opción.</span><span class="sxs-lookup"><span data-stu-id="b43e8-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="b43e8-119">Si crea un archivo DLL que usa esta opción y una aplicación que no usa esta opción llama a la DLL, el archivo DLL podría truncar un puntero de 64 bits cuyos bits superiores 32 sean significativos.</span><span class="sxs-lookup"><span data-stu-id="b43e8-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="b43e8-120">Esto puede producir un error de la aplicación sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="b43e8-120">This can cause application failure without any warning.</span></span>

 

 
