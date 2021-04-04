---
title: Afinidad del procesador en WOW64
description: Windows de 32 bits admite un máximo de 32 procesadores. Por lo tanto, las funciones como GetProcessAffinityMask simulan un equipo con procesadores 32 cuando se llama bajo WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- afinidad del procesador de 64 bits programación de Windows
- WOW64 64 bits programación de Windows, afinidad del procesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792459"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="1261a-106">Afinidad del procesador en WOW64</span><span class="sxs-lookup"><span data-stu-id="1261a-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="1261a-107">Windows de 32 bits admite un máximo de 32 procesadores.</span><span class="sxs-lookup"><span data-stu-id="1261a-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="1261a-108">Por lo tanto, las funciones como [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulan un equipo con procesadores 32 cuando se llama bajo WOW64.</span><span class="sxs-lookup"><span data-stu-id="1261a-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="1261a-109">La máscara de afinidad se obtiene realizando una operación OR bit a bit de los primeros 32 bits de la máscara con los 32 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="1261a-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="1261a-110">Por lo tanto, si un subproceso tiene afinidad para los procesadores 0, 1 y 32, WOW64 informa de la afinidad como 0 y 1, ya que el procesador 32 se asigna al procesador 0.</span><span class="sxs-lookup"><span data-stu-id="1261a-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="1261a-111">Las funciones que establecen la afinidad del procesador, como [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restringen los procesadores a los primeros 32 procesadores bajo WOW64.</span><span class="sxs-lookup"><span data-stu-id="1261a-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="1261a-112">Para obtener más información acerca de la afinidad del procesador, consulte [varios procesadores](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="1261a-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 