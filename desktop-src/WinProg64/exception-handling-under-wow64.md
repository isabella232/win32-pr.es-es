---
title: Control de excepciones en WOW64
description: WOW64 usa las excepciones nativas x64, ia64 o ARM64 como transporte para las excepciones x86. Por lo tanto, en una aplicación de 32 bits que se ejecuta bajo WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078232"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="ee3cb-104">Control de excepciones en WOW64</span><span class="sxs-lookup"><span data-stu-id="ee3cb-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="ee3cb-105">WOW64 usa las excepciones nativas x64, ia64 o ARM64 como transporte para las excepciones x86.</span><span class="sxs-lookup"><span data-stu-id="ee3cb-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="ee3cb-106">Por lo tanto, en una aplicación de 32 bits que se ejecuta bajo WOW64, las excepciones no detectadas se comportan como excepciones nativas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ee3cb-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="ee3cb-107">En una aplicación que se ejecuta en una versión de 32 bits de Windows, las excepciones no detectadas se pasan a los controladores de excepciones de nivel superior de la aplicación, si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee3cb-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="ee3cb-108">En la misma aplicación de 32 bits que se ejecuta bajo WOW64, el sistema puede suprimir las excepciones no detectadas.</span><span class="sxs-lookup"><span data-stu-id="ee3cb-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="ee3cb-109">**Windows Vista, Windows Server 2003 y Windows XP:** En la misma aplicación de 32 bits que se ejecuta bajo WOW64, el sistema llama a los filtros de excepción, pero puede suprimir las excepciones no detectadas sin invocar los controladores asociados.</span><span class="sxs-lookup"><span data-stu-id="ee3cb-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="ee3cb-110">Este comportamiento ha cambiado a partir de Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ee3cb-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="ee3cb-111">Para obtener más información sobre las excepciones no detectadas en los procedimientos de ventana, vea la función [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ee3cb-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 