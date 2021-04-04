---
description: Para liberar toda la memoria usada por el controlador de símbolos para un proceso, utilice la función SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpieza del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907128"
---
# <a name="symbol-handler-cleanup"></a><span data-ttu-id="4a7f1-103">Limpieza del controlador de símbolos</span><span class="sxs-lookup"><span data-stu-id="4a7f1-103">Symbol Handler Cleanup</span></span>

<span data-ttu-id="4a7f1-104">Para liberar toda la memoria usada por el controlador de símbolos para un proceso, utilice la función [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) .</span><span class="sxs-lookup"><span data-stu-id="4a7f1-104">To free all the memory used by the symbol handler for a process, use the [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) function.</span></span> <span data-ttu-id="4a7f1-105">Esta función enumera todos los módulos cargados, libera cada módulo y libera la memoria asignada para la lista de módulos.</span><span class="sxs-lookup"><span data-stu-id="4a7f1-105">This function enumerates all loaded modules, frees each module, and frees the memory allocated for the list of modules.</span></span> <span data-ttu-id="4a7f1-106">Después de llamar a **SymCleanup**, no puede usar el identificador de proceso en las funciones de control de símbolos hasta que llame a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="4a7f1-106">After you call **SymCleanup**, you cannot use the process handle in the symbol handling functions until you call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

 

 



