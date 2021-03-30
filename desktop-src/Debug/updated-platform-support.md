---
description: En caso necesario, la biblioteca DbgHelp se ha ampliado para admitir Windows de 32 y 64 bits.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Actualización de la compatibilidad para plataformas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538902"
---
# <a name="updated-platform-support"></a><span data-ttu-id="05559-103">Actualización de la compatibilidad para plataformas</span><span class="sxs-lookup"><span data-stu-id="05559-103">Updated Platform Support</span></span>

<span data-ttu-id="05559-104">En caso necesario, la biblioteca DbgHelp se ha ampliado para admitir Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05559-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="05559-105">Las definiciones de la función y la estructura originales todavía están en DbgHelp. h, pero también hay versiones actualizadas de estas definiciones que son compatibles con Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05559-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="05559-106">Si usa las funciones actualizadas en el código, se puede compilar para Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05559-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="05559-107">El código también será más eficaz, ya que las funciones originales simplemente llaman a las funciones actualizadas para realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="05559-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="05559-108">Por ejemplo, DbgHelp. h contiene definiciones para **SymUnloadModule** (función original) y **SymUnloadModule64** (función actualizada).</span><span class="sxs-lookup"><span data-stu-id="05559-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="05559-109">Estas definiciones son casi idénticas, pero usan tipos diferentes para el parámetro *BaseOfDll* .</span><span class="sxs-lookup"><span data-stu-id="05559-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="05559-110">(**SymUnloadModule** usa el tipo **DWORD** , mientras que **SymUnloadModule64** usa el tipo **DWORD64** ). Si escribe el código para utilizar **SymUnloadModule64**, se puede compilar para Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05559-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="05559-111">El código también es más eficaz que si llamara a **SymUnloadModule**.</span><span class="sxs-lookup"><span data-stu-id="05559-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="05559-112">A continuación se muestra una lista de las funciones actualizadas:</span><span class="sxs-lookup"><span data-stu-id="05559-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="05559-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="05559-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="05559-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="05559-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="05559-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="05559-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="05559-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="05559-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="05559-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="05559-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="05559-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="05559-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="05559-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="05559-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="05559-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="05559-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="05559-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="05559-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="05559-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="05559-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="05559-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="05559-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="05559-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="05559-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="05559-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="05559-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="05559-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="05559-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="05559-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="05559-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="05559-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="05559-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="05559-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="05559-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="05559-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="05559-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="05559-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="05559-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="05559-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="05559-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="05559-133">A continuación se muestra una lista de las estructuras actualizadas:</span><span class="sxs-lookup"><span data-stu-id="05559-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="05559-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="05559-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="05559-135">**IMAGEHLP \_ diferido \_ Symbol \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="05559-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="05559-136">**IMAGEHLP \_ duplicado \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="05559-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="05559-137">**IMAGEHLP \_ LINE64**</span><span class="sxs-lookup"><span data-stu-id="05559-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="05559-138">**IMAGEHLP \_ MODULE64**</span><span class="sxs-lookup"><span data-stu-id="05559-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="05559-139">**IMAGEHLP \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="05559-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="05559-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="05559-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="05559-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="05559-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



