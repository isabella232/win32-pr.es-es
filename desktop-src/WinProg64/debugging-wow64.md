---
title: Depurar WOW64
description: Las aplicaciones que se ejecutan bajo WOW64 se pueden depurar con un depurador hospedado en x86 o un depurador nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 bits programación de Windows, depuración
- depuración de la programación de Windows en WOW64 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421274"
---
# <a name="debugging-wow64"></a><span data-ttu-id="57d27-105">Depurar WOW64</span><span class="sxs-lookup"><span data-stu-id="57d27-105">Debugging WOW64</span></span>

<span data-ttu-id="57d27-106">Las aplicaciones que se ejecutan bajo WOW64 se pueden depurar de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="57d27-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="57d27-107">Use un depurador hospedado en x86 como NTSD, WinDbg o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="57d27-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="57d27-108">El NTSD de 32 bits se instala en% systemroot% \\ SysWow64 en las instalaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="57d27-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="57d27-109">Tenga en cuenta que los depuradores x86 se pueden usar para depurar código x86, pero no se pueden usar para desensamblar o establecer puntos de interrupción dentro de la capa de código thunk de WOW64 porque es código nativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="57d27-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="57d27-110">Use un depurador nativo como CDB, NTSD o WinDbg y la extensión del depurador de WOW64 Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="57d27-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="57d27-111">Si el depurador nativo se interrumpe mientras el procesador está en modo x86, el depurador presenta el proceso como un proceso x86.</span><span class="sxs-lookup"><span data-stu-id="57d27-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="57d27-112">Si el procesador está en modo nativo, el depurador presenta el proceso como nativo.</span><span class="sxs-lookup"><span data-stu-id="57d27-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="57d27-113">CDB, NTSD y WinDbg se incluyen en herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="57d27-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="57d27-114">Para obtener más información, vea la documentación de las [herramientas de depuración para Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="57d27-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="57d27-115">La extensión del depurador Wow64exts se instala con WinDbg.</span><span class="sxs-lookup"><span data-stu-id="57d27-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="57d27-116">Use el comando! LOAD wow64exts para cargar la extensión del depurador.</span><span class="sxs-lookup"><span data-stu-id="57d27-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="57d27-117">En la tabla siguiente se enumeran los comandos de la extensión del depurador! wow64exts.</span><span class="sxs-lookup"><span data-stu-id="57d27-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="57d27-118">Get-Help</span><span class="sxs-lookup"><span data-stu-id="57d27-118">Command</span></span>                | <span data-ttu-id="57d27-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="57d27-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d27-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="57d27-120">!wow64exts.sw</span></span>          | <span data-ttu-id="57d27-121">Cambia entre el modo x86 y el modo nativo.</span><span class="sxs-lookup"><span data-stu-id="57d27-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="57d27-122">! *recuento* de wow64exts. k</span><span class="sxs-lookup"><span data-stu-id="57d27-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="57d27-123">Vuelca un seguimiento combinado de la pila de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="57d27-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="57d27-124">Si se especifica *Count* , el comando vuelca las direcciones del primer *recuento* en cada seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="57d27-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="57d27-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="57d27-125">!wow64exts.info</span></span>        | <span data-ttu-id="57d27-126">Vuelca información básica sobre el PEB del proceso, el TEB del subproceso actual y las ranuras de almacenamiento local para el subproceso (TLS) utilizadas por WOW64.</span><span class="sxs-lookup"><span data-stu-id="57d27-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="57d27-127">*Dirección* de wow64exts. r</span><span class="sxs-lookup"><span data-stu-id="57d27-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="57d27-128">Vuelca el contexto de la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="57d27-128">Dumps context for the specified address.</span></span> <span data-ttu-id="57d27-129">Si no se especifica *Address* , el comando vuelca el contexto del procesador.</span><span class="sxs-lookup"><span data-stu-id="57d27-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 