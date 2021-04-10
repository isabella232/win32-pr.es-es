---
description: El controlador de símbolos está diseñado para realizar el seguimiento de varios conjuntos de archivos de símbolos.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inicialización del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152846"
---
# <a name="symbol-handler-initialization"></a><span data-ttu-id="612f9-103">Inicialización del controlador de símbolos</span><span class="sxs-lookup"><span data-stu-id="612f9-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="612f9-104">El controlador de símbolos está diseñado para realizar el seguimiento de varios conjuntos de archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="612f9-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="612f9-105">Para inicializar el controlador de símbolos, llame a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="612f9-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="612f9-106">El parámetro *hProcess* puede ser un número arbitrario único, un valor devuelto por la función [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o el identificador de cualquier proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="612f9-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="612f9-107">El parámetro *fInvadeProcess* indica si el controlador de símbolos debe enumerar los módulos cargados por el proceso y cargar los símbolos para cada uno de sus módulos.</span><span class="sxs-lookup"><span data-stu-id="612f9-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="612f9-108">Si *fInvadeProcess* es **true**, el parámetro *hProcess* debe ser el valor devuelto desde **GetCurrentProcess** o el identificador de un proceso existente.</span><span class="sxs-lookup"><span data-stu-id="612f9-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="612f9-109">Para actualizar esta lista, use la función [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .</span><span class="sxs-lookup"><span data-stu-id="612f9-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="612f9-110">El uso de *fInvadeProcess* es una forma sencilla de cargar todos los archivos de símbolos para un proceso.</span><span class="sxs-lookup"><span data-stu-id="612f9-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="612f9-111">Sin embargo, el controlador de símbolos no intentará cargar símbolos para los módulos cargados posteriormente por la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="612f9-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="612f9-112">En este caso, debe usar la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .</span><span class="sxs-lookup"><span data-stu-id="612f9-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
